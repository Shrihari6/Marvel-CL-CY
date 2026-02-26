Level 1:

# Marvel Chronicles !!!
----------



## TASK 1: Git Commands for Version Control

#### Basics:
- git branch 'name' creates it;
- git checkout 'name' switches the branch.
- git merge, combines both branches if they've have progressed, Git creates a new commit that ties the two histories together.
- git rebase , it creates a new commit to join two branches, rebase moves the entire feature branch so that it begins from the tip of the main branch.
> Git does not track "file changes" in the way traditional CVs (Concurrent Versions) do. Instead, it uses a Content-Addressable Filesystem.


![Image1](https://github.com/Shrihari6/Marvel-CL-CY/blob/DA_chatbot/marvel/Screenshot%202025-10-29%20101915.png?raw=true)
----------------------


[![Git Info](https://github.com/Shrihari6/Marvel-CL-CY/blob/DA_chatbot/marvel/git.png?raw=true)](https://notebooklm.google.com/notebook/f441e402-4b33-4cfe-9c67-df4daa782d46)
---------------------------

![Image2](https://github.com/Shrihari6/Marvel-CL-CY/blob/DA_chatbot/marvel/Screenshot%202025-10-29%20104522.png?raw=true)


----------

## TASK 3: Application on EC2 instance
I've used a virtual machine provisioned within  AWS Elastic Compute Cloud {EC2} ecosystem to host a Jenkins instance for CI & CD automation.
This Deployment utilizes a IAAS model 

#### Standard networking is often too slow for high-performance applications (like Big Data or ML).

**Enhanced Networking (ENA)**: Uses Single Root I/O Virtualization (SR-IOV) to provide higher I/O performance and lower CPU utilization. Essential for applications requiring high packet-per-second (PPS) performance.

**Elastic Fabric Adapter (EFA)**: A network interface for Amazon EC2 instances that enables you to run applications requiring high levels of inter-node communication (like High-Performance Computing) at scale.

![Image3](https://github.com/Shrihari6/Marvel-CL-CY/blob/DA_chatbot/marvel/Screenshot%202025-10-30%20230549.png?raw=true)
![Image5](https://github.com/Shrihari6/Marvel-CL-CY/blob/DA_chatbot/marvel/Screenshot%202025-10-30%20233247.png?raw=true)

![Image4](https://github.com/Shrihari6/Marvel-CL-CY/blob/DA_chatbot/marvel/Screenshot%202025-10-30%20233834.png?raw=true)

---------------------------

## TASK 2 & TASK 4: AWS CloudFront & Dynomo DB 









## TASK 5: KALI Linux - 
**Infrastructure as Code**: The live-build Engine
Kali is not "installed" like Windows; it is "composed." The engineers use a framework called live-build.

**The Build Pipeline**: Instead of manually configuring a system, engineers define the OS in a Git repository (live-build-config). When they trigger a build, a script pulls the Debian core, overlays Kali-specific configurations, and "chroots" (changes root) into the environment to install 600+ tools.

**Metapackages**: To manage the massive toolset, Kali uses Metapackages (e.g., kali-linux-top10, kali-linux-headless). These are "empty" packages that contain a list of dependencies. Installing one metapackage triggers the logic to pull every tool required for that specific engineering role.

Social Engineering Attacks: 
![SET](https://github.com/Shrihari6/Marvel-CL-CY/blob/DA_chatbot/marvel/Screenshot%202026-02-25%20235957.png?raw=true)

## TASK 6: Socket.IO

**Socket.IO** is more than just WebSockets. It is a management layer that sits on top of two sub-layers:

**Engine.IO**: The low-level engine that handles the connection. It first tries to connect via HTTP Long Polling for safety, then "upgrades" the connection to WebSockets for maximum speed.

**Packet Buffering**: If a user’s connection drops (e.g., they go through a tunnel), Socket.IO automatically buffers messages and sends them the moment they reconnect.

**Multiplexing** (Namespaces/Rooms): You can split one connection into multiple channels. For a chat app, "Rooms" allow you to isolate conversations so that User A and User B don't see User C's messages.

![Socket.io](https://github.com/Shrihari6/Marvel-CL-CY/blob/DA_chatbot/marvel/Screenshot%202026-01-31%20175347.png?raw=true)

![Socket io](https://github.com/Shrihari6/Marvel-CL-CY/blob/DA_chatbot/marvel/Screenshot%202026-02-27%20010554.png)

## TASK 7: OSI

The OSI reference model
The OSI model is used to connect to the open systems—these are the systems that are open and communicate with other systems. By using this model, we do not depend on an operating system anymore, so we are allowed to communicate with any operating system on any computer. This model contains seven layers, where each layer has a specific function and defines the way data is handled on certain different layers. The seven layers that are contained in this model are the Physical layer, Data Link layer, Network layer, Transport layer, Session layer, Presentation layer, and the Application layer.

![osi](https://github.com/Shrihari6/Marvel-CL-CY/blob/DA_chatbot/marvel/Screenshot%202026-02-27%20011317.png)

## TASK 8: IaaS, PaaS and SaaS

[![saas, paas, iaas](https://github.com/Shrihari6/Marvel-CL-CY/blob/DA_chatbot/marvel/OIP.jpg)](https://stackoverflow.com/questions/16820336/what-is-saas-paas-and-iaas-with-examples)


## TASK 9: 


## TASK 10: WEB SCRAPPING
Beautiful Soup is a Python library designed for parsing HTML and XML documents. It creates parse trees that make it straightforward to extract data from HTML documents you’ve scraped from the internet. Beautiful Soup is a useful tool in your web scraping toolkit, allowing you to conveniently extract specific information from HTML, even from complex static websites.

![webscraping](https://github.com/Shrihari6/Marvel-CL-CY/blob/DA_chatbot/marvel/Screenshot%202026-02-27%20015742.png)







