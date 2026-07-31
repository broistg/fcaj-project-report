---
title: "Event 2"
date: 2026-06-13
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Technical Summary Report: FCAJ Technical Meetup #2

### Event Overview

* **Event Name:** FCAJ Technical Meetup #2 – Cloud Solutions, Security & Migration Best Practices
* **Date & Time:** Saturday, June 13, 2026 (09:00 – 12:00)
* **Location:** AWS Vietnam Office / Community Meetup
* **Role:** Attendee

---

### Featured Speakers & Technical Presentations

1. **Hoàng Trọng – *AWS Cloud Architecture Patterns & System Resilience***
   * Analyzed high-availability architecture patterns spanning multiple Availability Zones (Multi-AZ).
   * Discussed disaster recovery strategies (Backup & Restore, Pilot Light, Warm Standby) and auto-scaling practices to ensure business continuity.

2. **Cường Nguyễn & Đạt Phạm – *Modern Application Development & Cloud Integration***
   * Shared architectural design patterns for building RESTful microservices and integrating AWS SDKs into containerized applications.
   * Detailed data decoupling strategies separating high-speed hot storage (DynamoDB) from long-term cold analytical storage (Amazon S3).

3. **Nghi Danh (Hiếu Nghị) – *Cloud Security, Governance & Identity Management***
   * Presented IAM role delegation principles, attribute-based access control (ABAC), and secrets management using AWS Secrets Manager.
   * Emphasized logging and compliance auditing using AWS CloudTrail and Amazon CloudWatch to maintain strict governance.

4. **Kiên & Thọ – *Cloud Migration & Infrastructure Automation Strategies***
   * Covered cloud migration methodologies (7Rs Framework: Rehost, Replatform, Refactor, etc.) for enterprise workloads.
   * Demonstrated automated infrastructure provisioning using Infrastructure as Code (IaC) tools and continuous delivery deployment pipelines.

---

### Key Takeaways & Work Application

* **Decoupled Storage Architecture:** Directly applied the hot/cold data segregation principles shared by Cường Nguyễn & Đạt Phạm to design our project's dual storage architecture (DynamoDB for hot interaction data, S3 for cold datasets and ML model artifacts).
* **IAM & Governance Control:** Implemented strict IAM execution roles for EC2 instances and SageMaker processing jobs to enforce least-privilege security controls.
* **Cost Efficiency & Resilience:** Incorporated Multi-AZ deployment considerations and AWS Budgets cost guardrails to prevent unbudgeted resource charges.

---

### Participation Proof

![Check-in Proof - Meetup 13/06/2026](/images/4-EventParticipated/Event_6-6-2026_13-6-2026.png)

> **Attendance Verification:** Check-in confirmation for FCAJ Technical Meetup #2 on June 13, 2026.
