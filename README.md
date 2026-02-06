# **Lab Project – Web Application Security with OWASP Juice Shop**

**CYBR 3050 – Principles of Cyber Operations and Defense**

---

## Background

Modern cyber defense requires a deep understanding of how real-world web applications fail. Many high-impact vulnerabilities today do not involve malware or low-level exploits, but rather **logic flaws, insecure authentication, broken access control, and unsafe input handling** in web applications.

In this lab project, you will work with **OWASP Juice Shop**, an intentionally vulnerable web application designed to teach web application security concepts through hands-on challenges. Unlike traditional labs with a single “correct” path, this project emphasizes **process, exploration, documentation, and communication**—skills essential for both defensive and offensive cyber roles.

This lab project spans multiple sessions and includes **four graded deliverables**:

1. Guided installation and introductory challenges
2. Independent challenge technical write-up
3. Video walkthrough of a solved challenge
4. Peer feedback on a classmate’s walkthrough

---

## Lab Deliverables Overview

| Deliverable       | Description                                    | Format              |
| ----------------- | ---------------------------------------------- | ------------------- |
| **Deliverable 1** | Installation + guided challenges + reflections | Written document    |
| **Deliverable 2** | Independent challenge technical write-up       | Written walkthrough |
| **Deliverable 3** | Video walkthrough of a challenge               | 5–7 minute video    |
| **Deliverable 4** | Peer feedback on classmate’s video             | Discussion post     |

This is a **process-focused** lab. Partial progress, thoughtful troubleshooting, and clear documentation are valued.

---

# **Task 1 – Environment Setup and Guided Challenges**

*(Deliverable 1)*

## Task 1 Background

OWASP Juice Shop is typically deployed using container technology. Containers allow security teams to quickly deploy, reset, and isolate vulnerable applications—an industry-standard practice.

In this task, you will:

* Install Node.js and NPM on your Kali VM
* Clone and install OWASP Juice Shop
* Complete two guided challenges
* Reflect on the vulnerabilities involved

---

## Step 1: Install Docker on Kali Linux

1. Open a terminal.
2. Update your system:

   ```bash
   sudo apt update
   ```
3. Install Node.js and NPM:

   ```bash
   sudo apt install -y nodejs
   sudo apt install -y npm
   ```
4. Clone Juice-Shop Code:

   ```bash
   git clone https://github.com/juice-shop/juice-shop.git --depth 1
   ```
5. Install Juice Shop:
   **This takes a long time but you only need to do it once.**
   ```bash
   cd juice-shop
   npm install
   ```
### Reflection Questions:
- Look at the Juice Shop documentation: [https://github.com/juice-shop/juice-shop](https://github.com/juice-shop/juice-shop)
- We could have used Docker rather than cloning our own version. What is the difference?

---

## Step 2: Run Juice Shop

1. Navigate to the juice-shop folder (you may already be there):

   ```bash
   npm start
   ```

2. Open a browser and navigate to:

   ```
   http://localhost:3000
   ```

You should see the OWASP Juice Shop homepage.

---

## Step 3: Guided Challenge 1 – *Score Board* (Easy)

### Background

The Score Board reveals all available challenges and tracks progress. In real applications, exposing internal functionality or debugging features can give attackers valuable reconnaissance.

### Guided Steps

1. Explore the site menu and UI.
2. Locate and access the **Score Board**.
3. Confirm the challenge is marked as solved.

### Reflection Questions

* Why is exposing internal challenge or debug information risky in real applications?
* What type of attacker benefit does this provide during reconnaissance?

---

## Step 4: Guided Challenge 2 – *Login Admin* (Slightly More Difficult)

### Background

Authentication flaws are among the most exploited web vulnerabilities. This challenge demonstrates how improper input handling can allow authentication bypass.

### Guided Steps

1. Navigate to the login page.
2. Attempt logging in with invalid credentials.
3. Use common testing techniques (e.g., manipulating input fields) to bypass authentication.
4. Confirm the challenge is marked as solved.

### Reflection Questions

* What type of vulnerability was exploited in this challenge?
* Why are login mechanisms a high-value target for attackers?
* How could this vulnerability be prevented?

---

## Deliverable 1 Submission Requirements

Submit **one document** containing:

* Confirmation of successful installation
* Answers to all reflection questions
* Any issues encountered and how you resolved them

---

# **Task 2 – Independent Challenge Exploration**

*(Deliverable 2)*

## Task 2 Background

Cybersecurity professionals must often work independently with minimal guidance. In this task, you will select **one challenge** to explore on your own and produce a technical write-up detailed enough for another student to reproduce your steps.

---

## Step 1: Select One Challenge

Choose **one** challenge from the list below (do **not** select challenges used in Task 1):

**Available Challenge Options**

* DOM XSS
* Reflected XSS
* Stored XSS
* Confidential Document
* Forged Review
* Admin Registration
* Password Strength
* Reset Password Weak Link
* Manipulate Basket
* View Basket

---

## Step 2: Solve the Challenge

* Document **everything you try**, including failed attempts.
* Take notes as you go—do not rely on memory later.

---

## Step 3: Write the Technical Walkthrough

Your write-up must include:

* Challenge name and category
* What the challenge is testing
* Step-by-step actions taken
* Screens or command output (optional but helpful)
* Final result and confirmation of success

A technically competent reader should be able to follow your write-up and solve the same challenge.

---

## Deliverable 2 Submission Requirements

Submit a **written technical walkthrough** (PDF or Markdown preferred).

---

# **Task 3 – Video Walkthrough**

*(Deliverable 3)*

## Task 3 Background

Clear communication is a critical cyber skill. Security findings often need to be explained to teammates, leadership, or clients.

---

## Step 1: Select Any Juice Shop Challenge

* You may reuse the challenge from Task 2 **or** select a different one.
* Ensure the challenge is fully solved before recording.

---

## Step 2: Record Your Walkthrough

Requirements:

* **5–7 minutes**
* Screen recording (browser + terminal if used)
* Narration describing *what* you are doing
* No need to explain theory in depth
* Use a tool such as **OBS Studio**

---

## Step 3: Upload Video

* Upload your video to **YUJA** via Canvas
* Post the video link to the designated discussion board
* Please find the **Embedded Code** link that you can put directly in the discussion board.

---

## Deliverable 3 Submission Requirements

* Video link posted to Canvas discussion board

---

# **Task 4 – Peer Review and Feedback**

*(Deliverable 4)*

## Task 4 Background

Security work is collaborative. Reviewing others’ findings helps identify gaps, unclear steps, and environmental assumptions.

---

## Step 1: Select a Classmate’s Video

* Choose **any** classmate’s video walkthrough
* Preferably select a challenge you did *not* solve yourself

---

## Step 2: Attempt the Challenge

* Follow the video walkthrough as closely as possible
* Take notes on clarity and reproducibility

---

## Step 3: Provide Feedback

Post a response that includes:

* What worked well in the walkthrough
* Any steps that were unclear or missing
* Whether you successfully reproduced the solution
* Any unexpected challenges you encountered

---

## Deliverable 4 Submission Requirements

* One discussion post providing thoughtful peer feedback

---

## Final Notes

* This is a **process-focused** lab project.
* Honest documentation of failures and troubleshooting is encouraged.
* Do not share solution details outside approved class discussions.

