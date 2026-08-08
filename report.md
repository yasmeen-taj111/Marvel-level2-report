# **TASK 2: CI/CD (Continuous Integration & Continuous Delivery) – Introduction to Jenkins**

### **Introduction**

In this task, I learned about different software development methods and how modern practices have improved the process. First, I studied older methods like the Waterfall model and Agile method. In these methods, if there are new client requirements or changes, it can take a lot of time to update everything. This makes the process slow and sometimes inefficient.

To solve these problems, modern approaches like **Continuous Integration (CI)** and **Continuous Delivery/Deployment (CD)** are used.

---

### **Understanding CI/CD**

**Continuous Integration (CI)** means developers regularly add their code to a shared repository, and the code is automatically built and tested. This helps in finding errors early.

**Continuous Delivery (CD)** means the application is always ready to be deployed.
**Continuous Deployment** means the application is automatically deployed after successful testing.

CI/CD helps connect the development team and operations team. Because of this, the feedback is faster, there is less delay, and the work becomes more efficient.

![CI/CD](https://github.com/yasmeen-taj111/images/blob/main/CICD.jpeg?raw=true)

---

### **Introduction to Jenkins**

To implement CI/CD, I used **Jenkins**, which is an open-source tool used for automation.

Jenkins allows us to create a pipeline using a file called a **Jenkinsfile**. This file contains all the steps needed for building, testing, and deploying the application.

---

### **Pipeline Implementation**

I created a **Jenkinsfile** in my GitHub repository. In this file, I defined different stages of the pipeline. Each stage has specific tasks that are executed one by one.

The stages I used are:

1. **Checkout Stage**

   * It takes the code from the GitHub repository.

2. **Install Dependencies Stage**

   * It installs required packages using `npm install`.

3. **Build Stage**

   * It prepares the application.

4. **Test Stage**

   * It runs testing (in my case, it is a basic placeholder).

5. **Run Application Stage**

   * It tries to start the application.

6. **Deploy Stage**

   * It shows deployment (simulated in this task).

---

### **Execution Process**

After creating the Jenkinsfile, I:

* Installed Jenkins on my Mac
* Started Jenkins and opened it in the browser
* Created a new pipeline job
* Connected my GitHub repository
* Selected the Jenkinsfile from the repository
* Ran the pipeline using **Build Now**

The pipeline ran successfully, and I was able to see the output in the Jenkins console.

---

![CI/CD](https://github.com/yasmeen-taj111/images/blob/main/CICD1.jpeg?raw=true)
![CI/CD](https://github.com/yasmeen-taj111/images/blob/main/CICD2.jpeg?raw=true)
![CI/CD](https://github.com/yasmeen-taj111/images/blob/main/CICD3.jpeg?raw=true)

### **Outcome**

From this task, I learned:

* Basics of CI/CD
* How automation helps in development
* How to create and use a Jenkins pipeline
* How to write a Jenkinsfile
* How different stages like build, test, and deploy work

---

### **Conclusion**

This task helped me understand how CI/CD makes the development process faster and easier. By using Jenkins, I was able to automate different steps of the project. It also helped me understand how real-world projects use automation to improve efficiency.

**Github** [click here](https://github.com/yasmeen-taj111/web-app)
---

Here’s a **short, clean task report** you can submit 👇

---

# **TASK 9: Hashing**

**Objective:**
To implement a secure system for storing and verifying user passwords using hashing techniques.

---

**Description:**
In this task, a simple authentication system was developed using Python and Flask. Instead of storing plain text passwords, the passwords were converted into hashed values using the `hashlib` library. This ensures better security, as hashed passwords cannot be easily reversed.

---
![sha256](https://cheapsslsecurity.com/p/wp-content/uploads/2025/06/sha256.png)

**Implementation:**

* Used **SHA-256 hashing** to encrypt user passwords.
* Stored user credentials (username and hashed password) in a **SQLite database**.
* Created a **registration system** to add new users.
* Built a **login system** to verify users by comparing hashed passwords.
* Developed a basic UI using HTML for user interaction.

---

![welcome](https://raw.githubusercontent.com/yasmeen-taj111/images/bf074633ff9c023932060b7418e6a5f4af7d340f/WhatsApp%20Image%202026-04-18%20at%2014.37.44.jpeg)
![register](https://github.com/yasmeen-taj111/images/blob/main/WhatsApp%20Image%202026-04-18%20at%2014.37.44%20(1).jpeg?raw=true)
![login](https://raw.githubusercontent.com/yasmeen-taj111/images/f51054c5a4b877d3af6975ae567b352b05ed3824/WhatsApp%20Image%202026-04-18%20at%2014.37.44%20(2).jpeg)
![success](https://github.com/yasmeen-taj111/images/blob/main/WhatsApp%20Image%202026-04-18%20at%2014.37.44%20(3).jpeg?raw=true)




**Outcome:**

* Successfully implemented secure password storage.
* Understood the concept of one-way hashing.
* Learned how authentication systems work in real-world applications.

---

![hash](https://github.com/yasmeen-taj111/images/blob/main/WhatsApp%20Image%202026-04-18%20at%2014.37.44%20(4).jpeg?raw=true)

**Conclusion:**
This task helped in understanding the importance of password security and how hashing protects user data. It also provided practical experience in backend development and database integration.



**Github** [click here](https://github.com/yasmeen-taj111/Hashing-)



---


# TASK 10: NMap

## What did I learn?

* Nmap (**Network Mapper**) is a network scanning tool used to understand what is available on a network.
* It can help us find **active hosts, open ports, running services, service versions, and the probable operating system** of a target.
* I learned that an **open port usually means some service is listening on that port**, while a closed port means there is no service accepting connections there.
* Nmap works by sending different types of network requests/packets to a target and analyzing the responses.
* I also learned that scanning `localhost` checks the same machine, while scanning an IP address checks the machine through its network interface.
* During my testing, the default scan initially showed all 1000 scanned ports as closed. I then started a simple Python HTTP server on port **8000** and scanned it again. Nmap was then able to detect the port as open and identify the service.
* OS detection is not always 100% accurate. Nmap gives its best estimate based on the responses it receives.

---

## Basic Nmap Commands and Their Use Cases

| **Command**                    | **Description**                                                | **Use Case**                                                                   |
| ------------------------------ | -------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| `nmap <target>`                | Performs a basic scan of the target's commonly used TCP ports. | Used to get a quick idea of the target's open ports.                           |
| `nmap -sn <network>`           | Performs host discovery without doing a normal port scan.      | Used to find which hosts are active on a network.                              |
| `nmap -p 8000 <target>`        | Scans a specific port.                                         | Useful when we want to check whether a particular service is accessible.       |
| `nmap -p 1-1000 <target>`      | Scans ports from 1 to 1000.                                    | Used to check a specific range of commonly used ports.                         |
| `nmap -p- <target>`            | Scans all TCP ports from 1 to 65535.                           | Used when a more complete port scan is required.                               |
| `nmap -sV <target>`            | Detects the services and attempts to identify their versions.  | Helps understand what software is running on open ports.                       |
| `nmap -O <target>`             | Attempts to identify the target's operating system.            | Useful for understanding the type of system being scanned.                     |
| `nmap -sV -O <target>`         | Performs service/version detection along with OS detection.    | Gives more detailed information about the target.                              |
| `nmap -Pn <target>`            | Skips host discovery and treats the target as online.          | Useful when normal host discovery is blocked.                                  |
| `nmap -T4 <target>`            | Increases the scan speed.                                      | Useful when a faster scan is required on an authorized network.                |
| `nmap -sC <target>`            | Runs Nmap's default NSE scripts.                               | Useful for gathering additional information about services and configurations. |
| `nmap --traceroute <target>`   | Attempts to show the network path to the target.               | Useful for understanding routing and troubleshooting network connectivity.     |
| `nmap -oN output.txt <target>` | Saves the scan in normal text format.                          | Useful for keeping scan results for later analysis and reporting.              |
| `nmap -oX output.xml <target>` | Saves the scan in XML format.                                  | Useful when scan results need to be processed by other tools.                  |

---

## My Nmap Scan Results

During the practical, I first scanned my Kali machine and found that the host was **up**, but the default 1000 TCP ports were closed.

To demonstrate an open port, I started a temporary Python HTTP server on port **8000** and scanned the port using Nmap.

The scan detected:

```text
8000/tcp   open   http
```

Using service detection, Nmap identified the service as:

```text
SimpleHTTPServer 0.6 (Python 3.11.4)
```

I also performed OS detection. Nmap identified the target as a **Linux-based system**, although OS detection can sometimes be approximate depending on the available network information.

---

![nmap](https://github.com/yasmeen-taj111/images/blob/main/nmap1.jpeg?raw=true)
![nmap](https://github.com/yasmeen-taj111/images/blob/main/nmap2.jpeg?raw=true)
![nmap](https://github.com/yasmeen-taj111/images/blob/main/nmap3.jpeg?raw=true)


## Analysis

From this task, I understood why open ports are important during network scanning. An open port tells us that a service is listening and accepting connections. By identifying the service and its version, we can understand what is exposed on the system.

I also understood that **having an open port is not automatically a security problem**. The important thing is whether the service is required and properly secured.

The scan also showed that Nmap cannot always identify the operating system with complete accuracy. Its result depends on the responses received from the target.

---

## Conclusion

This task helped me understand the practical use of Nmap for **host discovery, port scanning, service detection and OS detection**. I also learned how the result changes when a service is started on a particular port. Overall, Nmap can give a quick picture of what services are exposed on a system and can be useful for network administration and security auditing.

---

