<img width="1600" height="897" alt="11" src="https://github.com/user-attachments/assets/7a769e10-5a26-46eb-9b33-95a00a854c4b" />


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

## 📸 Summary of the Lab Steps Guide

**Step 1: Creating AWS An Amazon EC2 Windows Server Base 2025 instance which was configured as the foundation for the osTicket help desk environment.**
<br>
<img width="1600" height="740" alt="Step 1  Instance Portal - Creating EC2 Windows Server Base 2025 Instance" src="https://github.com/user-attachments/assets/740f36ad-507b-47e5-8184-b917afd0fd68" />
>
<br>

**Step 2:The AWS EC2 instance was successfully created and provisioned.**
<br>
<img width="1600" height="740" alt="Step 2  Successful creation of Instance" src="https://github.com/user-attachments/assets/4f3990e6-85a0-4d4a-b8c7-df8e291d7c91" />
>
<br>

**Step 3:The Windows Server EC2 instance was successfully launched and made available for remote administration.**
<br>
<img width="1600" height="740" alt="Step 3  Instance successfully launched" src="https://github.com/user-attachments/assets/da1deac1-393e-4650-aa7b-8dea41559b39" />
>
<br>

**Step 4: Transferring osTicket Installation Files and supporting software packages were to the server's Desktop directory.**
<br>
<img width="1600" height="740" alt="Step 4  Pasting osTicket installation files on instance Desktop directory" src="https://github.com/user-attachments/assets/ad453ee8-66de-4ea2-ba68-5f9cf5bc96c3" />
>
<br>

**Step 5: Installing Internet Information Services (IIS) to provide the web server environment required by osTicket.**
<br>
<img width="1600" height="740" alt="Step 5  Installing Internet Information Services (IIS) using Server Manager" src="https://github.com/user-attachments/assets/4508b8af-b3c7-426b-bcca-e9c21d22e25a" />
>
<br>

**Step 6: Installing Common Gateway Interface (CGI) enabled as an IIS application development feature to support communication between the web server and application components.**
<br>
<img width="1600" height="740" alt="Step 6  Installing Common Gateway Interface (CGI) as a feature" src="https://github.com/user-attachments/assets/76f5a0bf-ca18-48c2-a87b-a065bac96dd0" />
>
<br>

**Step 7: Verifying IIS with Microsoft Edge using the local loopback address "127.0.0.1" to confirm that IIS was successfully installed and operational.**
<br>
<img width="1600" height="740" alt="Step 7  Successful prompt of loopback address on Microsoft Edge to verify IIS is working" src="https://github.com/user-attachments/assets/9d997498-a444-4237-9e36-56c9aa9e1f91" />
>
<br>

**Step 8: Opening the osTicket Installation Files with the supporting components were opened to begin the application deployment process.**
<br>
<img width="1600" height="740" alt="Step 8  Opening my osTicket Installations File to proceed installing osTicket Helpdesk Service" src="https://github.com/user-attachments/assets/f6e767a8-db29-49bb-92c2-bd2b3d213ad8" />
>
<br>

**Step 9: PHP Manager for IIS was installed to assist with configuring and managing PHP within the IIS environment.**
<br>
<img width="1600" height="740" alt="Step 9  Installing PHP Manager" src="https://github.com/user-attachments/assets/44e0eeed-0ff7-46c2-be62-7aeb085ca511" />
>
<br>

**Step 10: Installing IIS URL Rewrite Module.**
<br>
<img width="1600" height="740" alt="Step 10  Installing REWRITE Module" src="https://github.com/user-attachments/assets/33cb3d2a-2d4b-452d-b8fa-f94a8b82d1a7" />
>
<br>

**Step 11: Installing Microsoft Visual C++ package was installed to provide supporting runtime components.**
<br>
<img width="720" height="403" alt="Step 11  Installing Microsoft Visual C" src="https://github.com/user-attachments/assets/37820d0f-4773-499f-919f-9510db572364" />
>
<br>

**Step 12: Installing MySQL to provide the database backend required by the osTicket application.**
<br>
<img width="1600" height="740" alt="Step 12  Installing MYSQL" src="https://github.com/user-attachments/assets/8e471bcd-14ee-4351-9e5f-cc0bd18e857d" />
>
<br>

**Step 13: HeidiSQL was installed and used as a database management tool for working with the MySQL environment.**
<br>
<img width="1600" height="740" alt="Step 13  Installing HeidiSQL" src="https://github.com/user-attachments/assets/2c80ecdc-165a-41f6-98e0-f06832f7a4c5" />
>
<br>

**Step 14: Successful osTicket Launch - The osTicket Help Desk System was successfully launched following the installation and configuration process.**
<br>
<img width="1600" height="740" alt="Step 14  Successful launch of osTicket Helpdesk Service" src="https://github.com/user-attachments/assets/9e1a3ef1-42a9-4c8e-9607-62652940fb71" />
>
<br>

**Step 15: osTicket Dashboard Portal - The osTicket administrative dashboard was accessed successfully, confirming that the help desk platform was operational.**
<br>
<img width="1600" height="740" alt="Step 15   Successful launch of osTicket Helpdesk Service - dashboard portal" src="https://github.com/user-attachments/assets/6bada74f-2d08-4589-8f4d-2cfbab79e97a" />
>
<br>

**Step 16: Configuring Help Desk Agent **Biyela Dlodlo, Makazana Ngxele and Maqoma Ngika** were configured within the osTicket environment.**
<br>
<img width="1600" height="740" alt="Step 16  Agents Portal with Agents Biyela Dlodlo, Makazana Ngxele   Maqoma Ngika" src="https://github.com/user-attachments/assets/d75c2565-2ece-466e-879e-33ae23f2c17e" />
>
<br>

**Step 17: Configuring the test user **Phuti Mphelo** was registered within the osTicket system.**
<br>
<img width="1600" height="740" alt="Step 17  Users Portal with user Phuti Mphelo" src="https://github.com/user-attachments/assets/27adaf2e-08b0-41f7-b5b9-36af86e3f3e9" />
>
<br>

**Step 18: Configuring Service Level Agreements - Multiple SLA plans were configured to establish different service response expectations for support requests.**
<br>
<img width="1600" height="740" alt="Step 18  SLA (Service Level Agreement) portal" src="https://github.com/user-attachments/assets/0ed4d49d-52f3-4987-a49d-42889096300f" />
>
<br>

**Step 19: Help Topics were configured to categorize different types of support requests, including access issues, password resets, equipment requests and other support scenarios.**
<br>
<img width="1600" height="740" alt="Step 19  Helptopics Portal" src="https://github.com/user-attachments/assets/b1e6a31c-e643-4827-a0dc-3ce60920771f" />
>
<br>

**Step 20: The osTicket Support Center was accessed to demonstrate the end-user interface used for submitting and tracking support requests.**
<br>
<img width="1600" height="740" alt="Step 20  Support Center for submitting a ticket" src="https://github.com/user-attachments/assets/e119d3ff-37c1-4db9-a046-445be6c88d84" />
>
<br>

**Step 21: Submitting a Support Ticket - The test user **Phuti Mphelo** submitted a simulated support request through the Support Center.**
<br>
<img width="1600" height="740" alt="Step 21  Submitting Ticket with user Phuti" src="https://github.com/user-attachments/assets/fab3fc89-66eb-4dcb-a4b0-49dd3d50d34c" />
>
<br>

**Step 22: Ticket Available for Agent Resolution - The submitted ticket became available within the help desk agent environment, allowing **Biyela Dlodlo** to review and begin the ticket resolution workflow.**
<br>
<img width="1600" height="740" alt="Step 22  Ticket successfully submitted   now is available for resolution on Helpdesk Agent Biyela’s dashboard" src="https://github.com/user-attachments/assets/14ba6fb8-dfdb-46ee-8b33-163c2ff5fec9" />
>
<br>

---

### 🎥 Full Video Demonstration

The **22 photos provide a visual summary of the major stages**, while the accompanying **1-hour video demonstrates the actual practical process in greater detail**, from AWS EC2 deployment and IIS configuration through to osTicket installation, help desk configuration and ticket submission.

[▶️ Watch the Full 1-Hour AWS osTicket Lab Demonstration](https://youtu.be/pN-alKwo3I4?si=Ko-juMD-KMsDvo46)

---

# 🌍 Real-World Relevance

In a real-world IT environment, help desk technicians rely on centralized ticketing systems to receive, organize, prioritize, assign, track, and resolve technical support requests. osTicket provides a practical example of how these workflows can be implemented within an organization, with tickets moving from end-user submission through technician assignment and troubleshooting.

This lab demonstrates how an IT technician can deploy and support a web-based help desk application within a cloud-hosted Windows Server environment. The project combines **AWS EC2 infrastructure, Windows Server administration, IIS web services, PHP, MySQL, database management, application deployment, user administration, SLAs, Help Topics, and ticket management**.

The simulated environment reflects common responsibilities found in Help Desk and IT Technician roles, including:

* Deploying and remotely administering Windows-based infrastructure.
* Installing and configuring server-side applications and prerequisites.
* Troubleshooting web-server and application dependencies.
* Managing help desk agents and end users.
* Organizing support requests through departments, teams, and Help Topics.
* Establishing Service Level Agreements (SLAs) for support requests.
* Receiving and reviewing end-user support tickets.
* Assigning tickets to the appropriate support personnel.
* Following a structured ticket workflow from submission through resolution.
* Maintaining an organized and centralized record of support activity.

The project also demonstrates how cloud infrastructure can provide a platform for hosting internal IT services. AWS EC2 provides the underlying compute environment, while IIS, PHP, MySQL, and osTicket work together to deliver the help desk application.

Overall, this lab bridges the gap between **technical infrastructure administration and day-to-day IT support operations**, demonstrating how a technician can work across both the underlying Windows environment and the help desk platform used by end users.

---

# 🏁 Conclusion

This AWS osTicket Installation, Setup & Ticket Resolution Lab provided a complete hands-on demonstration of deploying and administering a functional help desk environment from the ground up.

The project began with the creation of a **Windows Server Base 2025 EC2 instance** and continued through the installation and configuration of IIS, CGI, PHP, PHP Manager, URL Rewrite Module, Microsoft Visual C++, MySQL, and HeidiSQL. Once the required environment was prepared, osTicket was successfully deployed and configured as the organization's help desk platform.

The lab then moved beyond installation into practical help desk administration by configuring **agents, users, teams, departments, Service Level Agreements (SLAs), and Help Topics**. A simulated end-user support request was submitted through the Support Center and made available to the appropriate help desk agent, demonstrating the transition from **ticket intake to technician handling and resolution**.

This project demonstrates practical skills across **AWS cloud infrastructure, Windows Server administration, IIS web services, application deployment, database management, help desk administration, user management, SLA configuration, troubleshooting, and ticket lifecycle management**.

