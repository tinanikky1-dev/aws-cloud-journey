# Understanding DDoS Attacks and AWS Protection

## Overview

Today, I learned about **Distributed Denial of Service (DDoS) attacks** and how AWS helps protect networks and applications from them.

## What is a DDoS Attack?

A Distributed Denial of Service (DDoS) attack is a type of cyberattack where attackers use many infected computers or devices to send a huge amount of fake traffic to a website, application, or network.

The goal is not to steal data but to overwhelm the system, making it slow or completely unavailable for legitimate users.

### How DDoS Attacks Affect Networks

* Consume network bandwidth.
* Overload routers, firewalls, and servers.
* Prevent legitimate users from accessing services.

### How DDoS Attacks Affect Applications

* Send thousands or millions of fake requests.
* Use up CPU and memory resources.
* Cause applications to slow down or stop responding.

## How Infrastructure and Services Protect Against DDoS Attacks

Cloud providers like AWS use multiple layers of protection to defend against DDoS attacks.

Some of the AWS services that help include:

* **AWS Shield Standard** – Automatically protects AWS resources from common DDoS attacks at no extra cost.
* **AWS Shield Advanced** – Provides enhanced protection, detailed monitoring, and expert support for larger attacks.
* **AWS WAF (Web Application Firewall)** – Filters and blocks malicious web traffic before it reaches applications.
* **Amazon CloudFront** – Distributes content across multiple edge locations, helping absorb and reduce the impact of DDoS attacks.

## Key Takeaways

* A DDoS attack aims to make a service unavailable by flooding it with fake traffic.
* Networks and applications can become slow or stop responding during an attack.
* AWS provides built-in security services to help detect, filter, and mitigate DDoS attacks.
* Learning cloud security is an important part of becoming a Cloud Engineer.

## Conclusion

Today's lesson helped me understand that securing cloud applications is just as important as deploying them. As I continue my AWS Cloud journey, I am learning how AWS services work together to build secure, reliable, and highly available applications.
