# Cloud Concepts Reflection

## Goal

I reviewed the Cloud Concepts lecture (U1-04a) and reflected on what cloud computing means and how it connects to IT work and cybersecurity.

## Findings

### 1. Cloud in my own words

Instead of buying and taking care of your own powerful computers and storage, you can rent them from a company over the internet. You are basically paying for computing power, storage, software, or other IT services when you need them. The main difference is that you don't have to own and maintain all the physical hardware yourself.

### 2. Traditional IT -> Virtualization -> Cloud -> Containers

The main pattern is that IT has become more flexible and less connected to physical hardware. Traditional IT needed physical servers for different workloads, virtualization allowed one physical computer to run several virtual computers, and cloud made it possible to rent these resources when needed. Containers took this further by making applications easier and faster to move and run in different environments.

### 3. Deployment vs Service Models

A deployment model answers **where the technology is hosted**, while a service model answers **how much of the technology the customer has to manage**. For example, public cloud means the infrastructure is provided by a cloud company, while SaaS means I mainly use finished software instead of managing the servers behind it. Microsoft 365 is an example of public cloud + SaaS because I use the software through the internet without managing the servers myself.

### 4. Shared Responsibility Model

The Shared Responsibility Model means that the cloud provider and the customer both have security responsibilities. The provider is responsible for protecting the infrastructure, but the customer is still responsible for things like their data, user accounts, passwords, permissions, and configuration. A real example is the **2019 Capital One data breach**, where a configuration vulnerability in its AWS environment was exploited and customer information was accessed. This shows that moving to the cloud does not mean the customer can stop thinking about security.

> **Source:** Capital One, *Capital One Announces Data Security Incident* (2019)

### 5. Why organisations still hesitate

One reason an organisation might not move everything to the cloud is **privacy and regulation**, especially when dealing with sensitive information and requirements about where data can be stored. Another reason is **cost**, because a company may already have invested a lot of money in its own servers and equipment. Moving everything immediately could therefore be expensive even if cloud services have other benefits.

### 6. Cloud in an Entry-Level Tech Role

A helpdesk technician could get a ticket from a user who cannot log into their Microsoft 365 account, so they might need to check the account or help with authentication. A junior sysadmin could also receive an alert about a suspicious login to a cloud account and need to investigate it or report it to the security team. This shows that cloud services can be part of normal IT support even if the person's job title is not **cloud engineer**.

### 7. My Personal Takeaway

My main takeaway is that the cloud is not really something mysterious or separate from normal IT. There are still physical computers and data centres behind it, but someone else is managing the hardware for you. I also understand better now why security is still my responsibility when using an online service, especially things like passwords, MFA, permissions, and data.

---

## Source

- Capital One. (2019). *Capital One Announces Data Security Incident.*
