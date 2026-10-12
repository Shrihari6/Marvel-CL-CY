# LEVEL-2 Report
## TASK 1: AWS Lambda: Two-Person Chat Application
For this task, I built a lightweight, two-person chat application powered by AWS Lambda and DynamoDB,
with a single HTML and JS file serving as the browser-based frontend.
I tested everything locally using LocalStack first to make sure the logic was solid before deploying it to actual AWS infrastructure via an HTTPS Lambda Function URL.

Under the hood, the Lambda function handles two main actions: 
saving incoming messages when a user sends them, and returning the latest 100 sorted messages when the frontend polls. 
To keep things secure and prevent injection attacks, user inputs are safely handled using textContent rather than innerHTML. 
While it works great as a demo, I noted a few production limitations like the fact that table.scan() reads the entire table on every poll and that CORS is currently left wide open.

## TASK 2: CI/CD with Jenkins
To automate the build, test, and deployment lifecycle of a password manager web app, I set up a Jenkins pipeline running inside a local container. The underlying application stack consists of three distinct services working together: 
- a MySQL 8.0 database,
- a PHP 8.2 with Apache backend REST API,
- an Nginx frontend that serves the UI and proxies API requests.

The Jenkinsfile orchestrates a comprehensive pipeline that checks out the code, builds the Docker images, brings up the stack with docker compose, and dynamically resolves frontend ports. It then continuously polls the login endpoint until it responds with a 200 OK, executes API functional tests to verify authentication and vault items, runs health checks, and finally tags and pushes the image if registry credentials are provided.

## TASK 3: SSH: Key Discovery and Transfer
This task involved writing a robust Bash script to automate the discovery and migration of SSH keys between servers. To test it safely, I set up two Docker containers running real SSH daemons on ports 2222 and 2223, pre-seeded with various key types like RSA, Ed25519, PEM files, and authorized keys.

The script executes in clear stages: it uses sudo find over SSH to scan the source filesystem while skipping system directories, packages the discovered paths into a compressed tar archive, downloads it locally, uploads it to the destination container, and safely unpacks and cleans up. I verified the entire transfer by comparing MD5 checksums before and after, ensuring that file contents and strict permissions were perfectly preserved.

## TASK 4: Terraform: Infrastructure as Code on AWS
I used Terraform to manage the complete lifecycle—building, modifying, and destroying—an 11-resource AWS infrastructure stack by running it against LocalStack. The defined architecture included a VPC, public subnets, internet gateways, route tables, security groups, an EC2 t3.micro instance, an S3 bucket, a DynamoDB table, an SQS queue, and an SNS topic.

After initializing and applying the configuration, I tested infrastructure changes such as performing in-country instance type updates and forcing resource replacements for immutable components like S3 bucket names. Finally, I executed a complete teardown using terraform destroy, verifying through the AWS CLI that all components were successfully and cleanly removed in reverse dependency order.

## TASK 5: Wireshark: Traffic Analysis and Fault Diagnosis
While working through the Level 3 tasks, I captured my network traffic using Wireshark to analyze protocol behavior and troubleshoot a live networking fault. The capture contained thousands of packets dominated by encrypted TLS traffic and a heavy preference for IPv6 over IPv4 on my machine.

The primary fault I diagnosed was why the LocalStack emulator on port 4566 was completely unreachable. Wireshark revealed massive TCP retransmissions heading toward a NAT64 address (64:ff9b::7f00:1), which happened because the hostname resolved to an IPv6 record that routed through the gateway loopback instead of staying local. The fix was simply pointing configuration endpoints to the direct IPv4 loopback literal.

## TASK 6: Docker: Containers, Images, and Dockerfiles
I reviewed core Docker concepts covering the distinction between immutable images and running containers, layer caching mechanics, and effective Dockerfile structuring. By grouping package manager commands like apt-get update and install into single RUN instructions, I avoided stale cache issues and optimized build performance.

Working with Podman under the hood via the standard Docker CLI, I also explored container networking and storage. I utilized read-only bind mounts to protect critical configuration and schema files, and deployed named volumes to ensure that database contents safely survive container restarts and rebuilds across sessions.

## TASK 7: Dockerize the Web Application (No Compose File)
I containerized the password manager web application using standalone docker run commands and a custom bridge network named pm-net instead of relying on a compose file. This involved setting up stock images for MySQL and Nginx alongside a custom-built Apache-PHP backend image.

Along the way, I navigated a few environment hurdles—such as ensuring --load was passed during builds in Podman, substituting Dockerfile health checks with explicit command-line flags, and mapping ports away from privileged port 80. I also made sure to use named volumes to avoid the silent data loss trap associated with anonymous volumes when rebuilding containers.

## TASK 8: Web Scraping: Flight Price Analysis
I built a command-line Python tool using Selenium and headless Chromium to automate flight searches on KAYAK, extract pricing data, and email out structured reports. Because standard form-filling workflows ran into cookie popups and geolocation pre-fill issues, I implemented a reliable direct URL construction mode.

The tool handles various edge cases, such as warning when cabin classes are silently ignored, filtering out irrelevant train results, and validating IATA airport codes and dates. For testing purposes, I verified email generation and delivery successfully using a local fake SMTP server script that captured outbound messages.

## TASK 9: Hashing: Secure Password Storage & Verification
To practice secure authentication, I built a terminal password manager that replaces fast hashing algorithms like SHA-256 with hashlib.scrypt. Scrypt introduces significant memory and computational costs, making brute-force attacks computationally expensive and slow for attackers.

The tool implements secure engineering practices, including atomic file writes via temporary files and strict permission controls (600) to eliminate race conditions. It also utilizes constant-time string comparisons via secrets.compare_digest and equalized response timings to successfully prevent timing attacks and username enumeration.

## TASK 10: Nmap: Network Discovery and Port Scanning
I performed an Nmap subnet scan (--privileged) across a /24 network range to discover active hosts and analyze their exposed services. Out of 256 probed IP addresses, 6 hosts responded online, revealing a mix of heavily firewalled infrastructure, perimeter defense gateways, and standard servers.

A detailed review of host .98 highlighted a broad and high-risk attack surface, with multiple exposed HTTP ports, an active MySQL database instance, and open RDP and remote management ports. This exercise underscored the importance of perimeter hardening and restricting administrative services from broad network exposure.
