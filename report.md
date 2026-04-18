## **TASK 2: CI/CD (Continuous Integration & Continuous Delivery) – Introduction to Jenkins**

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

## **TASK 9: Hashing**

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


