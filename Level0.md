# **MARVEL Club Chronicles🔥**
------------------------------------------------------

## **Task 1: 3D Printing**
Learnt how to use 3D printer. STL file which is the real pre model file to which the printer creates model. Learnt slicing, giving appropriate adjustments, etc using Ultimaker Cura. Cura - converts the .stl file to printer readable instructions .gcode
When gcode was sent to printer, which printed the object  layer by layer.

----
## **Task 2: API Integration – CyberBhai Project**

For the second task, I created a cybersecurity-focused project named CyberBhai 🕵️. The project help to provide scanning, awareness, and chatbot-based security guidance.

<img width="1180" height="715" alt="Task 2 (1)" src="https://github.com/user-attachments/assets/74ff6809-4408-4ed5-b03b-e9b7a55c83e1" />

### **Features Implemented**

#### 1. IP Address & Nmap Scanning
- User enters an IP address.
- The project performs an Nmap scan.
- Results can be exported as PDF 📄 or printed.

<img width="1219" height="795" alt="Task 2 (3)" src="https://github.com/user-attachments/assets/9abf6ef8-205b-48ce-8aab-cd573e2081eb" />

###### Example:
- Input: `192.168.1.1`
- Output: Open ports, running services, OS detection

<img width="1214" height="808" alt="Task 2 (4)" src="https://github.com/user-attachments/assets/c9f53e5d-d2e3-40f5-b7ff-3f816bd9ea2d" />

#### 2. Security Pages Shortcut Hub
Direct links to hidden security settings of daily-use platforms:
🔒 WhatsApp Security
🔒 Facebook Security
🔒 Instagram Security
🔒 YouTube Security
🔒 X (Twitter) Security
Helps users quickly configure privacy & safety settings.
<img width="1176" height="805" alt="Task 2 (5)" src="https://github.com/user-attachments/assets/c3a959e1-cbe5-4591-a8a8-a6835275f6b8" />

#### 3. Checklist for Security
✅ System Admins: Server hardening, firewall, patch updates.
✅ Normal Users: Strong passwords, 2FA, avoiding phishing.
- [x] Enable 2FA  
- [x] Keep system updated  
- [ ] Regularly audit firewall rules


<img width="1155" height="712" alt="Task 2 (6)" src="https://github.com/user-attachments/assets/42886336-019b-4851-96dd-60526d18340b" />

#### 4. Gemini Chatbot – CyberGuard 🤖
A pre-prompted Gemini chatbot embedded as CyberGuard.
Guides users in aspects of cyber hygiene, security practices, and awareness.
Example prompt:
User: "How can I secure my WiFi?"  
CyberGuard: "Change the default router password, enable WPA3, and disable WPS."


⚙️ Tech Stack & API Usage

API:  Gemini API

Languages/Frameworks: NodeJS, html5, CSS

Output: Web app interface + PDF export

```mermaid
✨ Marvel-style Analogy

> Just like Jarvis assists Iron Man, CyberBhai assists normal users and admins by scanning, guiding, and securing their digital armor 🛡️.
```
## Task 3: GitHub

**GitHub** is a platform that allows developers to automate their software development workflows directly within the GitHub repository. GitHub enables continuous integration and continuous deployment (CI/CD) processes, making it easier for teams to collaborate and streamline their development pipelines.
<img width="712" height="624" alt="Task 3 (1)" src="https://github.com/user-attachments/assets/cf8c2a8a-f8f7-4b7f-82db-4d2279aba804" />

**Forking** refers to the process of creating a personal copy of someone else's repository (a collection of files and the entire version history of those files) in a distributed version control system like Git. When you fork a repository, you are essentially creating your own independent copy of the project, which can be modified without affecting the original repository.
<img width="674" height="588" alt="Task 3 (2)" src="https://github.com/user-attachments/assets/1dc4e852-e519-46cb-8049-bf347bc13ed5" />

A **pull request** (PR) in GitHub is a proposed code change submitted by a developer for review and integration into the main codebase.
<img width="950" height="783" alt="Task 3 (3)" src="https://github.com/user-attachments/assets/34ee7070-457e-46a3-ae07-39d4c96c9f3b" />

**Issue** in github. It lets viewer to raise  any concerns related to current repository.
<img width="803" height="682" alt="Task 3 (4)" src="https://github.com/user-attachments/assets/7ec1bd49-db61-4aa7-beb5-39d1c785e703" />


--------------------
## **Task 4: Getting Familiar with Linux/Unix Kernal**
I choose **Kali Linux** for this task. The tasks are as followed:
- mkdir - Creating a folder.
- cd - changing directory to that folder.

  <img width="672" height="424" alt="Task 4 (1) " src="https://github.com/user-attachments/assets/f004696a-12bc-4308-b4a9-620462dec443" />

- touch - Creating the blank file without any text editor.
- Creating 2600 folder in this folder where each named as B1..B2600
- cat - and Concatinating them 

<img width="1592" height="783" alt="Task 4 (2)" src="https://github.com/user-attachments/assets/8f306a5a-8896-4021-8464-7cbb0099399b" />
--------------

## **Task 5: Linear Reggression**
For this experiment, I trained a regression model using Gradient descent on the **California Housing dataset** and Compared the results between my **Custom implementations** and **Scikit-Learn's built-in model**
### **Evaluation Metrics**
##### To measure performance, the following metrics were used:

**MSE (Mean Squared Error)** -> average squared difference between predictions and actual values.  
- **MAE (Mean Absolute Error)** → average absolute difference between predictions and actual values.  
- **R² (Coefficient of Determination)** → proportion of variance explained by the model (higher is better).  
- **RMSE (Root Mean Squared Error)** → square root of MSE, bringing error back to original target units.  

###  Results: Custom vs Scikit-learn

| Metric | Custom | Sklearn |
|--------|--------|---------|
| *MSE*  | 0.2788 | 0.2491 |
| *MAE*  | 0.4159 | 0.3902 |
| *R²*   | 0.7212 | 0.7599 |
| *RMSE* | 0.5279 | 0.4991 |

###  Interpretation
- Both implementations give **very close results**, which validates that the custom model is working correctly.  
- The **Scikit-learn model** performs slightly better across all metrics (lower errors, higher R²).  
- The small differences arise from optimizations in Scikit-learn’s algorithms.


<iframe src="https://www.kaggle.com/embed/shrihari6/marveltask5?kernelSessionId=260599274" height="800" style="margin: 0 auto; width: 100%; max-width: 950px;" frameborder="0" scrolling="auto" title="MarvelTask5"></iframe>

------------------

## Task 6:The Matrix Puzzle - Decoding and Reveling image with NumPy and Matplotlib

Gained confidence with NumPy operations like reshaping, slicing, flipping, and transposing.
Learned to visualize 2D arrays using Matplotlib.
debugging and puzzle-solving.

<iframe src="https://www.kaggle.com/embed/shrihari6/marveltask-6?kernelSessionId=260789678" height="800" style="margin: 0 auto; width: 100%; max-width: 950px;" frameborder="0" scrolling="auto" title="MarvelTask-6"></iframe>


---------------------

## Task 7: Creating Portfolio webpage

I have created  a basic portfolio webpage using html5 and CSS.

[link](https://portfolio-git-dachatbot-shrihari-jawalgis-projects.vercel.app/)

---------------------

## Task 8: Writting Resource Article

I have writen an article on secure Cloud computing and Azure administration
[Link](https://portfolio-git-dachatbot-shrihari-jawalgis-projects.vercel.app/)


## Task 9: TinkedCad
Tinkercad Circuits is a free, browser-based electronic circuit simulator that allows users to design, test, and program electronic circuits online without needing physical hardware.
It supports popular microcontrollers like the Arduino Uno, Micro, and ATtiny chips, and enables users to create code using either a block-based editor similar to Scratch or a traditional text-based editor. 

I have made a DC motor speed controller in tinkerCAD with using - Arduino Uno R3, DC Motor, 9V battery, Potentiometer, BreadBoard and some Jumper wires.

<img width="1038" height="622" alt="Task 9 (1)" src="https://github.com/user-attachments/assets/fb36155f-5381-481e-924e-990c5f7f82ff" />

--------------

## Task 10: 

