# **TASK 1: CI/CD (Continuous Integration & Continuous Delivery) – Introduction to Jenkins**

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



# **TASK 2: Hashing**

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


# TASK 3: NMap

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
# TASK 4: Docker

## What I Learned

Docker is a platform used to **package, distribute, and run applications in isolated environments called containers**. It helps ensure that an application works consistently across different machines and avoids the common “it works on my machine” problem.

### Docker Analogy

Imagine I have a **Python application** that requires Python, certain libraries, and other dependencies. Instead of installing everything manually on every system, Docker packages the application and its dependencies into a container. This container can then run on another developer's machine, a server, or the cloud with the same setup.


![docker](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQWwqi7vttCIgGmYl8JUU6eW1O4Wr7XUqQlrlLVwXxqwQ&s=10)

### VM vs Containers

* **VMs** contain a complete operating system and their own kernel, making them heavier.
* **Containers share the host OS kernel**, making them lightweight and faster to start.
* Containers generally require **less memory and CPU** compared to VMs.

### Images vs Containers

* **Docker Image** → A read-only blueprint/template used to create containers. It contains the application, dependencies, runtime, and required configuration.
* **Docker Container** → A running instance of an image. It has a writable layer and runs the application in an isolated environment.

### Dockerfile

A **Dockerfile** is a text file containing instructions to build a Docker image. It makes the application environment reproducible and portable.

### Docker Compose

I also learned about **Docker Compose**, which is used to manage multiple containers using a YAML configuration file. It allows services, networks, and volumes to be defined and managed together.

## Commands I Practiced

```bash
docker --version
docker pull hello-world
docker run hello-world
docker images
docker ps
docker ps -a
docker build -t my-nginx .
docker run -d -p 8080:80 --name my-nginx-container my-nginx
docker stop my-nginx-container
docker start my-nginx-container
docker logs my-nginx-container
docker rm my-nginx-container
docker rmi my-nginx
```

I also created a **Dockerfile** containing:

```dockerfile
FROM nginx:latest
```

Then I built an image from it and ran it as a container.

### Key Takeaway

The main concept I understood is:

**Dockerfile → Image → Container**

Docker makes applications easier to **package, share, and run consistently** across different environments.

![docker](https://github.com/yasmeen-taj111/images/blob/main/docker1.jpeg?raw=true)
![docker](https://github.com/yasmeen-taj111/images/blob/main/docker2jpeg.jpeg?raw=true)
![docker](https://github.com/yasmeen-taj111/images/blob/main/docker3.jpeg?raw=true)

---

# TASK 5: Dockerize — Without Using YAML File

## Problem

The task was to containerize the **Level 0 Resource Library web application** without using a YAML/Compose file.

The main focus was to understand **Docker networking and volumes** while running the backend and database in separate containers.

## What I Did

* Created a `Dockerfile` for the Express backend.
* Pulled the official **PostgreSQL** Docker image.
* Created a custom bridge network: `resource-library-net`.
* Created a Docker volume: `resource-library-data`.
* Ran the backend and PostgreSQL containers manually using `docker run`.
* Connected both containers to the same network.
* Used the PostgreSQL container name as the database host instead of `localhost`.



### Dockerfile

The backend Dockerfile was created to package the Express application along with its required dependencies.

```
dockerfile
FROM node:alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "start"]

```

#### What each part does:

* `FROM node:alpine` → Uses a lightweight Node.js image as the base.
* `WORKDIR /app` → Sets `/app` as the working directory inside the container.
* `COPY package*.json ./` → Copies the package files.
* `RUN npm install` → Installs the required dependencies.
* `COPY . .` → Copies the application code into the container.
* `EXPOSE 3000` → Documents that the application uses port 3000.
* `CMD ["npm", "start"]` → Starts the Express application.

---

### 1. Web Application Running

The Resource Library application running successfully in the browser.

* **URL:** `http://localhost:3000`

![docker](https://github.com/yasmeen-taj111/images/blob/main/dockerize1.jpeg?raw=true)


### 2. Docker Images

This shows the images available locally, including the backend application image and PostgreSQL image.

```bash
docker images

```

![docker](https://github.com/yasmeen-taj111/images/blob/main/dockerize2.jpeg?raw=true)
![docker](https://github.com/yasmeen-taj111/images/blob/main/dockerize3.jpeg?raw=true)



### 3. Running Containers

This shows both the backend and database containers running.

```bash
docker ps

```
![docker](https://github.com/yasmeen-taj111/images/blob/main/dockerize4.jpeg?raw=true)
![docker](https://github.com/yasmeen-taj111/images/blob/main/dockerize5.jpeg?raw=true)




### 4. Docker Volume

The PostgreSQL volume can be checked using:

```bash
docker volume ls

```

or:

```bash
docker volume inspect resource-library-data

```
![docker](https://github.com/yasmeen-taj111/images/blob/main/dockerize6.jpeg?raw=true)
![docker](https://github.com/yasmeen-taj111/images/blob/main/dockerize7.jpeg?raw=true)


> This confirms that the database has persistent storage.

### 5. Project Files

The project folder showing the Dockerfile and application files.

![docker](https://github.com/yasmeen-taj111/images/blob/main/dockerize8.jpeg?raw=true)

---

### Docker Networking — What I Learned

Docker provides networking so that containers can communicate with each other while remaining isolated from the host system.

Some common Docker network types are:

| Network | Use |
| --- | --- |
| **Bridge** | Containers communicate on the same Docker host |
| **Host** | Container uses the host's network stack |
| **None** | Container has no network |
| **Overlay** | Used for communication across multiple Docker hosts |

For this task, I used a custom bridge network:

```bash
docker network create resource-library-net

```

This allowed my backend and PostgreSQL containers to communicate using the container name.

---

### Docker Volumes — What I Learned

Containers are generally treated as temporary environments. If a container is removed, data stored only inside that container can be lost.

Docker volumes provide persistent storage.

For example:

```bash
docker volume create mydata

```

and:

```bash
docker run -d -v mydata:/app/data myapp

```

In my project, the PostgreSQL data was stored using:
`resource-library-data:/var/lib/postgresql/data`

So the database storage is not dependent on the lifetime of the PostgreSQL container.

---

### Common Docker Commands I Used

| Command | Purpose |
| --- | --- |
| `docker --version` | Check Docker installation |
| `docker pull postgres` | Pull PostgreSQL image |
| `docker images` | List Docker images |
| `docker build -t myapp .` | Build an image |
| `docker ps` | Show running containers |
| `docker ps -a` | Show all containers |
| `docker run` | Create and start a container |
| `docker stop <container>` | Stop a container |
| `docker rm <container>` | Remove a container |
| `docker logs <container>` | View container logs |
| `docker network create <name>` | Create a network |
| `docker network ls` | List networks |
| `docker network inspect <name>` | Inspect a network |
| `docker volume create <name>` | Create a volume |
| `docker volume ls` | List volumes |
| `docker volume inspect <name>` | Inspect a volume |
| `docker exec -it <container> bash` | Access a running container |

---


## Outcome

The Resource Library application successfully runs in Docker with the **backend and PostgreSQL in separate containers**, connected through a custom bridge network, with database data stored using a Docker volume.


**Github** [click here](https://github.com/yasmeen-taj111/Dockerize_resource_library)

---

# TASK 6: Wireshark

### Problem

Network problems such as **packet loss, latency, retransmissions, and duplicate acknowledgments** can be difficult to identify because they are not always visible to the user.

![docker](https://github.com/yasmeen-taj111/images/blob/main/wireshark.png?raw=true)

### How is it solved?

**Wireshark** captures and analyzes network packets. By applying filters and using the Statistics tools, we can identify protocols, monitor traffic, and detect issues such as **TCP retransmissions**.

### What did I do?

* Captured network traffic on the `eth0` interface in Kali Linux.
* Used filters such as `icmp` and `tcp.analysis.retransmission`.
* Analyzed ICMP echo request/reply packets generated through ping.
* Checked the **I/O Graph** to observe network traffic over time.
* Used the retransmission filter to identify a suspected TCP retransmission.



**Wireshark I/O Graph showing packet traffic over time along with captured ICMP, DNS, and other network packets.**


![docker](https://github.com/yasmeen-taj111/images/blob/main/wireshark4.jpeg?raw=true)


![docker](https://github.com/yasmeen-taj111/images/blob/main/wireshark1.jpeg?raw=true)



**Wireshark filters showing a suspected TCP retransmission and ICMP echo request/reply packets.**

![docker](https://github.com/yasmeen-taj111/images/blob/main/wireshark2.jpeg?raw=true)

![docker](https://github.com/yasmeen-taj111/images/blob/main/wireshark3.jpeg?raw=true)

### What did I learn?

* Wireshark can capture and analyze network traffic at the packet level.
* Display filters make it easier to investigate specific protocols or network issues.
* `icmp` can be used to analyze ping traffic.
* `tcp.analysis.retransmission` helps identify possible TCP retransmissions.
* I/O Graphs help visualize traffic patterns and detect unusual activity.
* Wireshark can be useful for troubleshooting **packet loss, latency, and network communication problems**.

### Conclusion

Wireshark provides a detailed view of network communication and helps diagnose problems by analyzing individual packets, protocols, and traffic patterns.

---

# TASK 7: Web Scraping and Automation - Flight Ticket Price Analysis

## Problem

Finding and comparing flight prices manually takes time, especially when there are many flights with different timings, airlines, and prices.

## Solution

I developed a **Flight Price Analyzer** that automatically searches Google Flights and extracts important flight information such as:

* Airline
* Departure and arrival time
* Duration
* Number of stops
* Price
* Cheapest flight

It can also send the cheapest flight details through email.

## Technologies Used

* **Python** – Main programming language used to build the project.
* **Selenium** – A Python tool used to control a web browser automatically. Here, it opens Google Flights, enters the search details, and reads the results.
* **Google Flights** – Website from which flight information is collected.
* **SMTP** – A standard protocol used to send emails. It connects the program to Gmail.
* **`.env`** – A file used to store sensitive information such as email credentials without putting them directly in the code.
* **Web Scraping** – Automatically collecting information from a website using a program.

##  How It Works

```text
User enters
Origin + Destination + Date
          ↓
     Selenium opens
      Google Flights
          ↓
     Searches flights
          ↓
   Extracts flight details
          ↓
 Finds the cheapest flight
          ↓
    Sends details by email
```

## What I Learned

* How **Selenium automation** works.
* How to identify and extract elements from a webpage.
* How to handle dynamic webpages and changing elements.
* How to work with **environment variables** using `.env`.
* How **SMTP and Gmail App Passwords** are used for sending emails.
* How to structure a Python project into separate files.


![docker](https://github.com/yasmeen-taj111/images/blob/main/SCRAPING1.jpeg?raw=true)

![docker](https://github.com/yasmeen-taj111/images/blob/main/SCRAPING2.jpeg?raw=true)

![docker](https://github.com/yasmeen-taj111/images/blob/main/SCRAPING3.jpeg?raw=true)




##  Result

The project successfully searches flights and displays results like:

```text
Airline   : IndiGo
Departure : BLR at 3:45 AM
Arrival   : BOM at 5:30 AM
Duration  : 1 hr 45 min
Stops     : Nonstop
Price     : ₹13,352

Cheapest Price: ₹12,977
```
![docker](https://github.com/yasmeen-taj111/images/blob/main/SCRAPINGMAIL.jpeg?raw=true)


**Github** [click here](https://github.com/yasmeen-taj111/FLIGHT-PRICE-ANALYZER)

---

# Task 8: SSH 

### Objective 
The aim of this task was to practise working with SSH keys and securely transferring test files between two Linux servers. I used two AWS EC2 Ubuntu instances, created a test SSH key pair, archived the test files, encrypted the archive, and transferred it to the second server. 

### Work carried out 
1. **Created test SSH keys:** On Server A, I generated an Ed25519 key pair for the lab and prepared a test authorized_keys file. 

2. **Set up SSH access:** I configured SSH authentication from Server A to Server B using a separate transfer key. 

3. **Archived and encrypted the files:** I used a Bash script to create a compressed archive of the lab directory and encrypted it with AES-256-CBC using PBKDF2. 

4. **Transferred and restored the archive:** The script copied the encrypted archive to Server B using SCP. I then decrypted and extracted it on Server B. 

5. **Verified file integrity:** I calculated SHA-256 checksums for the test private and public key files on both servers. The values matched, confirming that the transferred test files were unchanged. 

### Screenshots 

#### 1. Test SSH key generation on Server A 
The terminal shows generation of the lab Ed25519 key pair. Only test keys were used. 
![ssh](https://github.com/yasmeen-taj111/images/blob/main/ssh1.jpeg?raw=true) 

#### 2. SSH connection to Server B 
This shows the successful SSH login from Server A to Server B using the transfer key. 
![ssh](https://github.com/yasmeen-taj111/images/blob/main/ssh2.jpeg?raw=true) 

#### 3. Bash script execution and transfer 
The script created the archive, encrypted it, and transferred the encrypted file successfully. 
![ssh](https://github.com/yasmeen-taj111/images/blob/main/ssh3.jpeg?raw=true) 

#### 4. Decryption and extracted files on Server B 
The encrypted archive was decrypted and extracted. The test key files and test_user directory are visible. 
![ssh](https://github.com/yasmeen-taj111/images/blob/main/ssh4.jpeg?raw=true) 

#### 5. SHA-256 integrity verification 
The SHA-256 values for lab_key and lab_key.pub matched on both servers. 
![ssh](https://github.com/yasmeen-taj111/images/blob/main/ssh5.jpeg?raw=true) 

### Result 
The test files were successfully archived, encrypted, transferred, decrypted, and extracted. Matching SHA-256 checksums on both servers confirmed the integrity of the transferred files. After completing the practical, I terminated both EC2 instances to avoid leaving the lab servers running.

---

# TASK 9: TERRAFORM

Building, Modifying and Destroying AWS Infrastructure

## 1. Objective

The objective of this task was to learn how to use Terraform to create, modify and delete cloud resources on AWS. I used Terraform commands to manage an EC2 instance and understand how Infrastructure as Code works.

## 2. Tools Used

* Terraform

* AWS

* AWS CLI

* Visual Studio Code

* macOS Terminal

## 3. Introduction

Terraform is an Infrastructure as Code (IaC) tool that helps create and manage cloud resources using code instead of manually setting them up. In this task, I used Terraform to create an AWS EC2 instance, make changes to it and finally delete it.

## 4. Steps Performed

### Step 1: Initialize Terraform

First, I created a project folder named `terraform-aws-task` and added the Terraform configuration files. I used the `terraform init` command to initialize the project and download the AWS provider.

Figure 1: Successful Terraform initialization

![tf](https://github.com/yasmeen-taj111/images/blob/main/tf1.jpeg?raw=true)

### Step 2: Validate and Plan the Configuration

I used the `terraform validate` command to check whether my configuration was correct. It returned a success message.

Next, I ran `terraform plan` to see what changes Terraform would make. It showed that one EC2 instance would be created.

Figure 2: Terraform validation and plan

![tf](https://github.com/yasmeen-taj111/images/blob/main/tf2.jpeg?raw=true)
![tf](https://github.com/yasmeen-taj111/images/blob/main/tf3.jpeg?raw=true)



### Step 3: Create an EC2 Instance

I created an EC2 instance on AWS using Terraform. I configured it with Ubuntu 24.04 and the `t2.micro` instance type in the US West (Oregon) region.

I used the `terraform apply` command and confirmed the operation. The instance was successfully created and was visible in the AWS Console.

Figure 3: Terraform plan showing the EC2 instance to be created

![tf](https://github.com/yasmeen-taj111/images/blob/main/tf4.jpeg?raw=true)

Figure 4: EC2 instance running in AWS

![tf](https://github.com/yasmeen-taj111/images/blob/main/tf5.jpeg?raw=true)

### Step 4: Modify the EC2 Instance

After creating the instance, I changed its name from `terraform-task-server` to `terraform-task-server-updated` in the configuration file.

I then used `terraform plan` to preview the change and `terraform apply` to update the instance. Terraform successfully modified the instance without creating a new one.

Figure 5: Successful modification of the EC2 instance
![tf](https://github.com/yasmeen-taj111/images/blob/main/tf6.jpeg?raw=true)



### Step 5: View Instance Details

I used the `terraform output` command to display the details of the EC2 instance, including its instance ID and instance type.

Figure 6: Terraform output

![tf](https://github.com/yasmeen-taj111/images/blob/main/tf7.jpeg?raw=true)


### Step 6: Destroy the EC2 Instance

After completing the creation and modification steps, I used the `terraform destroy` command to delete the EC2 instance.

I confirmed the operation by entering `yes`. Terraform successfully destroyed the instance.

Figure 7: Successful destruction of the EC2 instance

![tf](https://github.com/yasmeen-taj111/images/blob/main/tf8.jpeg?raw=true)

### Step 7: Verify the Cleanup

Finally, I checked the AWS Console to confirm that the EC2 instance had been terminated. I also used the `terraform show` and `terraform state list` commands to verify the final Terraform state and check that no managed resources remained.

Figure 8: EC2 instance terminated in AWS Console

![tf](https://github.com/yasmeen-taj111/images/blob/main/tf10.jpeg?raw=true)


Figure 9: Terraform state verification

![tf](https://github.com/yasmeen-taj111/images/blob/main/tf9.jpeg?raw=true)

## 5. Result

Successfully created an AWS EC2 instance using Terraform, modified its name, viewed its details and destroyed it. I also verified that the instance was terminated and that no managed resources remained in the Terraform state.

## 6. Conclusion

Through this task, I learned how to use Terraform to manage AWS resources. I gained practical experience in creating, modifying and deleting an EC2 instance using simple commands. I also understood how Terraform helps manage cloud infrastructure through code and keeps track of resources using its state file.

---

# TASK 10:AWS LAMBDA

## 1. Objective

To develop a simple serverless chat application using **AWS Lambda, Amazon API Gateway, Python, HTML, CSS and JavaScript**.

The application accepts a message from the user through a web interface. The message is sent to an AWS Lambda function through an API Gateway endpoint. Lambda processes the message and returns a predefined response, which is displayed back on the web page.

---

## 2. Technologies Used

| Technology         | Purpose                                          |
| ------------------ | ------------------------------------------------ |
| AWS Lambda         | Serverless backend for processing messages       |
| Amazon API Gateway | Provides an HTTP API for the frontend            |
| Python             | Programming language used for Lambda             |
| HTML               | Structure of the chat interface                  |
| CSS                | Styling the chat interface                       |
| JavaScript         | Sends messages to the API and displays responses |
| cURL               | Testing the API endpoint                         |

---

# 3. Creating the HelloWorldLambda Function

An AWS Lambda function named **HelloWorldLambda** was created using the Python runtime.

The function contains a Lambda handler that prints a message and returns an HTTP success response.

### Code

```python
def lambda_handler(event, context):
    print("Hello from AWS Lambda!")

    return {
        "statusCode": 200,
        "body": "Hello World! My first Lambda function is working."
    }
```

The function was deployed successfully from the AWS Lambda console.

**Figure 1: HelloWorldLambda function code**

![lambda](https://github.com/yasmeen-taj111/images/blob/main/lambda1.jpeg?raw=true)

---

# 4. Testing the Lambda Function

A test event named **HelloWorldTest** was created to verify whether the Lambda function executes correctly.

The function returned:

```text
StatusCode: 200
Hello World! My first Lambda function is working.
```

The execution log also showed that the Lambda function was successfully invoked.

**Figure 2: Successful execution of HelloWorldLambda**

![lambda](https://github.com/yasmeen-taj111/images/blob/main/lambda2.jpeg?raw=true)

---

# 5. Creating the Chat Application

A web-based chat interface was developed using **HTML, CSS and JavaScript**.

The interface contains:

* A chat header
* Message display area
* Text input field
* Send button
* Separate user and bot message styles

The frontend was designed to provide a simple interface for communicating with the Lambda backend.

---

# 6. Creating the ChatAppLambda Function

A second Lambda function named **ChatAppLambda** was created to process messages received from the chat application.

The function performs the following operations:

1. Receives the incoming request.
2. Extracts the message from the request body.
3. Converts the message to lowercase.
4. Checks for predefined keywords.
5. Generates an appropriate response.
6. Returns the response in JSON format.

For example:

| Input          | Response                               |
| -------------- | -------------------------------------- |
| `hello` / `hi` | Hello! How can I help you today?       |
| `name`         | I'm an AWS Lambda chat assistant.      |
| `help`         | Sure! Tell me what you need help with. |
| `how are you`  | I'm doing great! Thanks for asking.    |
| `bye`          | Goodbye! Have a great day!             |
| Other input    | Default chatbot response               |

**Figure 3: ChatAppLambda source code**

![lambda](https://github.com/yasmeen-taj111/images/blob/main/lambda3.jpeg?raw=true)

---

# 7. Testing ChatAppLambda

A test event named **ChatTest** was created with the following input:

```json
{
    "message": "Hello"
}
```

The function successfully processed the input and returned:

```json
{
    "message": "Hello",
    "reply": "Hello! How can I help you today?"
}
```

The execution status was **Succeeded**, confirming that the chatbot Lambda function was working correctly.

**Figure 4: Successful ChatAppLambda test**

![lambda](https://github.com/yasmeen-taj111/images/blob/main/lambda4.jpeg?raw=true)

---

# 8. Creating API Gateway

To connect the web application with Lambda, an **HTTP API** named `ChatAppAPI` was created using Amazon API Gateway.

A POST route was configured:

```text
POST /chat
```

This route was connected to the `ChatAppLambda` function.

The communication flow is:

```text
User
 ↓
Chat Web Page
 ↓
JavaScript fetch()
 ↓
API Gateway
 ↓
POST /chat
 ↓
ChatAppLambda
 ↓
Response
 ↓
API Gateway
 ↓
Chat Web Page
```

The API endpoint used by the application is:

```text
https://75xh04rqjk.execute-api.ap-south-1.amazonaws.com/chat
```

---

# 9. Configuring CORS

CORS was configured in API Gateway to allow the browser-based frontend to communicate with the API.

The configuration used:

```text
Allowed Origin: *
Allowed Method: POST
Allowed Header: Content-Type
```

This allows the frontend application to send HTTP requests to the API Gateway endpoint.

---

# 10. Testing the API Using cURL

Before connecting the API with the frontend, the endpoint was tested using the terminal.

### Command

```bash
curl -X POST "https://75xh04rqjk.execute-api.ap-south-1.amazonaws.com/chat" \
-H "Content-Type: application/json" \
-d '{"message":"Hello"}'
```

The API returned:

```json
{
    "message": "Hello",
    "reply": "Hello! How can I help you today?"
}
```

This confirmed that **API Gateway was successfully connected to Lambda**.

**Figure 5: Testing API Gateway using cURL**

![lambda](https://github.com/yasmeen-taj111/images/blob/main/lambda5.jpeg?raw=true)

---

# 11. Connecting the Frontend to API Gateway

The JavaScript code was updated to send the user's message to the API Gateway endpoint using the `fetch()` method.

The request uses the HTTP `POST` method and sends the message in JSON format.

```javascript
const API_URL =
    "https://75xh04rqjk.execute-api.ap-south-1.amazonaws.com/chat";
```

The message is sent using:

```javascript
fetch(API_URL, {
    method: "POST",
    headers: {
        "Content-Type": "application/json"
    },
    body: JSON.stringify({
        message: message
    })
});
```

The response returned by Lambda is then displayed as a bot message on the webpage.

---

# 12. Final Testing

The complete application was tested through the browser.

Different messages were entered to verify the predefined responses.

For example:

```text
User: hi
Bot: Hello! How can I help you today?

User: who r u
Bot: Thanks for your message! I'm a simple chatbot.

User: help me
Bot: Sure! Tell me what you need help with.
```

Messages that do not match the predefined keywords receive the default chatbot response.

**Figure 6: Final working AWS Lambda Chat Application**

![lambda](https://github.com/yasmeen-taj111/images/blob/main/lambda6.jpeg?raw=true)

---

# 13. Lambda Functions Created

The AWS Lambda console contains the two functions created for this task:

1. `HelloWorldLambda`
2. `ChatAppLambda`

**Figure 7: Lambda functions created**

![lambda](https://github.com/yasmeen-taj111/images/blob/main/lambda7.jpeg?raw=true)

---

# 14. Result

The serverless chat application was successfully implemented.

The application was able to:

* Create and execute AWS Lambda functions.
* Process user messages using Python.
* Provide a web-based chat interface.
* Connect the frontend with Lambda through API Gateway.
* Send messages using HTTP POST requests.
* Return responses in JSON format.
* Display Lambda responses in the browser.
* Handle predefined keywords and unknown messages.

---

# 15. Conclusion

This task demonstrated the implementation of a **serverless web application using AWS Lambda**.

AWS Lambda was used as the backend without requiring a continuously running server. Amazon API Gateway provided the communication layer between the frontend and Lambda. The final application successfully accepted user messages, processed them using Lambda, and displayed the corresponding responses in the browser.

---

