# AWS-osTicket-Installation-Setup-and-Ticket-Resolution-Lab

---

# 📌 Project Overview

This project demonstrates the complete deployment, configuration, and administration of the **osTicket Help Desk System** on an **Amazon EC2 Windows Server Base 2025 instance**.

The lab begins by provisioning a Windows Server virtual machine in AWS EC2 and preparing the environment for web-based help desk software. **Internet Information Services (IIS)** is installed and configured with **Common Gateway Interface (CGI)**, followed by the installation of PHP, PHP Manager, IIS URL Rewrite Module, Microsoft Visual C++ Redistributable, MySQL Server, and HeidiSQL.

After the required components are installed, osTicket is deployed and configured as a functional help desk environment. The configuration includes **agents, users, teams, departments, Service Level Agreements (SLAs), and Help Topics**.

The project concludes by simulating a real-world IT support workflow in which an end user submits a support request through the osTicket Support Center. The ticket is then made available to the appropriate help desk agent for review and resolution.

The repository documents the lab through **22 summary step photos and a 1-hour full video demonstration**, providing an end-to-end view of the infrastructure deployment, application installation, help desk configuration, and ticket management workflow.

🎥 **Full 1-Hour Lab Demonstration:**
[AWS osTicket Installation, Setup & Ticket Resolution Lab — YouTube](https://youtu.be/pN-alKwo3I4?si=Ko-juMD-KMsDvo46)

---

# 📊 Project Summary

| Category                    | Details                                                   |
| --------------------------- | --------------------------------------------------------- |
| **Project**                 | AWS osTicket Installation, Setup & Ticket Resolution Lab  |
| **Cloud Platform**          | Amazon Web Services (AWS)                                 |
| **Infrastructure**          | Amazon EC2                                                |
| **Operating System**        | Windows Server Base 2025                                  |
| **Web Server**              | Internet Information Services (IIS)                       |
| **IIS Feature**             | Common Gateway Interface (CGI)                            |
| **Application**             | osTicket v1.15.8                                          |
| **Programming Environment** | PHP                                                       |
| **Database**                | MySQL Server                                              |
| **Database Tool**           | HeidiSQL                                                  |
| **Web Configuration**       | IIS URL Rewrite Module                                    |
| **Runtime Dependency**      | Microsoft Visual C++ Redistributable                      |
| **Remote Access**           | Remote Desktop Protocol (RDP)                             |
| **Browser Testing**         | Microsoft Edge                                            |
| **Help Desk Agents**        | Biyela Dlodlo, Makazana Ngxele & Maqoma Ngika             |
| **End User**                | Phuti Mphelo                                              |
| **Service Management**      | SLAs & Help Topics                                        |
| **Ticket Workflow**         | Ticket submission → Agent dashboard → Resolution workflow |
| **Documentation**           | 22 Summary Photos + 1-Hour Full Video                     |
| **Project Status**          | ✅ Completed                                               |

### 🔧 Key Tasks Completed

* Created and launched a Windows Server Base 2025 EC2 instance.
* Transferred osTicket installation files to the server.
* Installed and configured IIS.
* Enabled CGI as an IIS feature.
* Verified IIS functionality using the local loopback address.
* Installed PHP Manager for IIS.
* Installed IIS URL Rewrite Module.
* Installed Microsoft Visual C++ Redistributable.
* Installed MySQL Server.
* Installed and configured HeidiSQL.
* Deployed osTicket Help Desk System.
* Verified successful osTicket installation.
* Configured the osTicket administrative environment.
* Created help desk agents and users.
* Configured teams and departments.
* Created and configured Service Level Agreements.
* Configured Help Topics.
* Tested the Support Center.
* Submitted a simulated end-user support ticket.
* Demonstrated the ticket becoming available to a help desk agent for resolution.

---

# 🏗️ Lab Architecture

The lab was built around an **AWS EC2 Windows Server Base 2025 instance** hosting the complete osTicket help desk environment.

```text
                         Amazon Web Services (AWS)
                                   │
                                   ▼
                         ┌─────────────────────┐
                         │   Amazon EC2        │
                         │ Windows Server 2025 │
                         └──────────┬──────────┘
                                    │
                                    │ RDP
                                    ▼
                         ┌─────────────────────┐
                         │      IIS Web Server │
                         │                     │
                         │ CGI Enabled         │
                         └──────────┬──────────┘
                                    │
                   ┌────────────────┼─────────────────┐
                   │                │                 │
                   ▼                ▼                 ▼
             ┌──────────┐    ┌────────────┐    ┌─────────────┐
             │   PHP    │    │ URL Rewrite│    │ Visual C++  │
             │ Manager  │    │   Module   │    │ Redistribut.│
             └────┬─────┘    └────────────┘    └─────────────┘
                  │
                  ▼
          ┌─────────────────┐
          │    osTicket     │
          │  Help Desk      │
          └────────┬────────┘
                   │
          ┌────────┴───────────┐
          │                    │
          ▼                    ▼
   ┌─────────────┐      ┌─────────────┐
   │ MySQL Server│◄────►│  HeidiSQL   │
   │  Database   │      │ DB Management│
   └─────────────┘      └─────────────┘
                   │
                   ▼
        ┌────────────────────────┐
        │   osTicket Management  │
        ├────────────────────────┤
        │ Agents                 │
        │ Users                  │
        │ Teams                  │
        │ Departments            │
        │ SLAs                   │
        │ Help Topics            │
        └───────────┬────────────┘
                    │
                    ▼
             ┌───────────────┐
             │ Support Center│
             └───────┬───────┘
                     │
                     ▼
             ┌───────────────┐
             │ End User      │
             │ Phuti Mphelo  │
             └───────┬───────┘
                     │
                     │ Submit Ticket
                     ▼
             ┌───────────────┐
             │ Help Desk     │
             │ Agent         │
             │ Biyela Dlodlo │
             └───────┬───────┘
                     │
                     ▼
             Ticket Resolution
```

### 🎫 Ticket Workflow

```text
End User
   │
   ▼
Support Center
   │
   ▼
Submit Support Ticket
   │
   ▼
Ticket Created
   │
   ▼
Help Desk Agent Dashboard
   │
   ▼
Ticket Review & Assignment
   │
   ▼
Troubleshooting / Support
   │
   ▼
Ticket Resolution
```

This architecture demonstrates how a cloud-hosted Windows server can be used to provide a centralized help desk platform for managing users, support requests, service levels, and technician workflows.

---

# 🎯 Objectives

The primary objectives of this lab were to:

* Deploy a Windows Server Base 2025 virtual machine using AWS EC2.
* Access and administer the Windows Server environment using RDP.
* Transfer osTicket installation files to the EC2 instance.
* Install and configure Internet Information Services (IIS).
* Enable Common Gateway Interface (CGI) within IIS.
* Verify IIS functionality using Microsoft Edge and the local loopback address.
* Install PHP and integrate it with IIS using PHP Manager.
* Install and configure the IIS URL Rewrite Module.
* Install Microsoft Visual C++ Redistributable.
* Install and configure MySQL Server.
* Install and use HeidiSQL for database management.
* Deploy the osTicket Help Desk application.
* Configure the osTicket administrative environment.
* Create and manage help desk agents.
* Configure teams and departments.
* Register and manage end users.
* Configure Service Level Agreements (SLAs).
* Configure Help Topics for categorizing support requests.
* Test the osTicket Support Center.
* Simulate a real-world end-user support request.
* Demonstrate the process of submitting a support ticket.
* Demonstrate ticket availability on the help desk agent dashboard.
* Practice a complete help desk ticket management workflow.

---

# 🛠️ Technologies Used

* **Amazon Web Services (AWS)**
* **Amazon EC2**
* **Windows Server Base 2025**
* **Remote Desktop Protocol (RDP)**
* **Internet Information Services (IIS)**
* **Common Gateway Interface (CGI)**
* **PHP**
* **PHP Manager for IIS**
* **IIS URL Rewrite Module**
* **Microsoft Visual C++ Redistributable**
* **MySQL Server**
* **HeidiSQL**
* **Microsoft Edge**
* **osTicket Help Desk System**

---

# 🧠 Skills Demonstrated

This project demonstrates practical experience with:

* AWS EC2 virtual machine deployment
* Windows Server administration
* Remote Desktop administration
* IIS installation and configuration
* Web server troubleshooting
* CGI configuration
* PHP installation and IIS integration
* PHP Manager configuration
* IIS URL Rewrite configuration
* Microsoft Visual C++ runtime installation
* MySQL installation and configuration
* Database administration using HeidiSQL
* Web application deployment
* osTicket installation and configuration
* Help desk system administration
* Agent account management
* User account management
* Team and department configuration
* Service Level Agreement configuration
* Help Topic management
* Support ticket creation
* Ticket workflow management
* End-user support simulation
* Help desk troubleshooting
* IT service management concepts
* Cloud-based infrastructure administration
* Real-world IT support workflow simulation

---

## 📸 Summary Lab Step-by-Step Guide

Since you have **22 photos that serve as a high-level visual summary**, I would keep this section concise, just like your other repositories. The **full 1-hour video** can provide the detailed walkthrough beyond the summary images. Your other repos use this distinction between summary documentation and the full practical demonstration. ([GitHub][1])

### Step 1: Creating AWS EC2 Windows Server Base 2025 Instance

An Amazon EC2 Windows Server Base 2025 instance was configured as the foundation for the osTicket help desk environment.

### Step 2: Successful Creation of Instance

The AWS EC2 instance was successfully created and provisioned.

### Step 3: Instance Successfully Launched

The Windows Server EC2 instance was successfully launched and made available for remote administration.

### Step 4: Transferring osTicket Installation Files

The required osTicket installation files and supporting software packages were transferred to the server's Desktop directory.

### Step 5: Installing Internet Information Services (IIS)

IIS was installed using Windows Server Manager to provide the web server environment required by osTicket.

### Step 6: Installing Common Gateway Interface (CGI)

CGI was enabled as an IIS application development feature to support communication between the web server and application components.

### Step 7: Verifying IIS with Microsoft Edge

The local loopback address was accessed through Microsoft Edge to confirm that IIS was successfully installed and operational.

### Step 8: Opening the osTicket Installation Files

The osTicket installation package and supporting components were opened to begin the application deployment process.

### Step 9: Installing PHP Manager

PHP Manager for IIS was installed to assist with configuring and managing PHP within the IIS environment.

### Step 10: Installing IIS URL Rewrite Module

The IIS URL Rewrite Module was installed as part of the osTicket web application environment.

### Step 11: Installing Microsoft Visual C++

The required Microsoft Visual C++ Redistributable package was installed to provide supporting runtime components.

### Step 12: Installing MySQL

MySQL Server was installed to provide the database backend required by the osTicket application.

### Step 13: Installing and Configuring HeidiSQL

HeidiSQL was installed and used as a database management tool for working with the MySQL environment.

### Step 14: Successful osTicket Launch

The osTicket Help Desk System was successfully launched following the installation and configuration process.

### Step 15: osTicket Dashboard Portal

The osTicket administrative dashboard was accessed successfully, confirming that the help desk platform was operational.

### Step 16: Configuring Help Desk Agents

Help desk agents **Biyela Dlodlo, Makazana Ngxele and Maqoma Ngika** were configured within the osTicket environment.

### Step 17: Configuring End User

The test end user **Phuti Mphelo** was registered within the osTicket system.

### Step 18: Configuring Service Level Agreements

Multiple SLA plans were configured to establish different service response expectations for support requests.

### Step 19: Configuring Help Topics

Help Topics were configured to categorize different types of support requests, including access issues, password resets, equipment requests and other support scenarios.

### Step 20: Support Center

The osTicket Support Center was accessed to demonstrate the end-user interface used for submitting and tracking support requests.

### Step 21: Submitting a Support Ticket

The test user **Phuti Mphelo** submitted a simulated support request through the Support Center.

### Step 22: Ticket Available for Agent Resolution

The submitted ticket became available within the help desk agent environment, allowing **Biyela Dlodlo** to review and begin the ticket resolution workflow.

---

### 🎥 Full Video Demonstration

The **22 photos provide a visual summary of the major stages**, while the accompanying **1-hour video demonstrates the actual practical process in greater detail**, from AWS EC2 deployment and IIS configuration through to osTicket installation, help desk configuration and ticket submission.

[▶️ Watch the Full 1-Hour AWS osTicket Lab Demonstration](https://youtu.be/pN-alKwo3I4?si=Ko-juMD-KMsDvo46)


[1]: https://github.com/SyberGrind/Microsoft-365-Set-Up-and-Administration-Lab "GitHub - SyberGrind/Microsoft-365-Set-Up-and-Administration-Lab: Hands-on Microsoft 365 administration lab for Tugela Cloud Solutions, covering user and department setup, Microsoft Entra ID configuration, shared mailboxes, authentication, password resets, account blocking and restoration, deleted-user recovery, and Outlook mailbox testing through realistic administration scenarios. · GitHub"
