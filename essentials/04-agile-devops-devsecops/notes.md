# Agile, DevOps & DevSecOps — Revision Notes

**Category:** Essentials · **Focus Area:** Security Compliance · **Level:** Intermediate

---

## Table of Contents

1. [Introduction to Agile](#1-introduction-to-agile)
2. [Business Analytics and Design Thinking](#2-business-analytics-and-design-thinking)
3. [DevOps](#3-devops)
4. [DevSecOps](#4-devsecops)

---

## 1. Introduction to Agile

### 1.1 What is Agile?

An approach to software development that advocates the following central tenets:

- Early, periodic delivery of software
- Adaptive planning
- High level of customer collaboration
- Self-organized teams

### 1.2 The Agile Manifesto

> "Individuals and interactions over processes and tools. Working software over comprehensive documentation. Customer collaboration over contract negotiation. Responding to change over following a plan."

### 1.3 Principles and Benefits of Agile

| Principle | Benefits |
|---|---|
| **1. Working software is the primary measure of progress** | Customers can see working software periodically; customer feedback is received early and continuously; requirements elaboration is strengthened |
| **2. Early, frequent, and continuous delivery of software** | Quality is truly part of the process; testing is continuous as small features are frequently delivered; testing becomes an essential practice |
| **3. Welcome and incorporate changing requirements** | Responds to market realities; responds to changing requirements from customers; quickens time-to-market |
| **4. Trust people — give them the environment and support they need** | Autonomy and collaboration improve morale; the best teams are self-organized; work atmosphere creates a sense of shared ownership; retention challenges are addressed |
| **5. Customers work alongside developers daily throughout the project** | Customers and developers work toward a common goal — building software of value; customers get a transparent view of the process |
| **6. As a team, reflect periodically to become more effective and efficient** | Learnings are implemented right away; highlights impediments; encourages thinking over learnings; finds ways to improve |
| **7. Aim for sustainable development** | — |

---

## 2. Business Analytics and Design Thinking

### 2.1 Business Analytics Introduction

| Type | Description |
|---|---|
| **Descriptive Analytics** | Analysis of historical data to determine how a unit may respond to a set of variables |
| **Predictive Analytics** | Analysis of historical data to determine the likelihood of particular future outcomes |
| **Prescriptive Analytics** | Combines the descriptive analytics process, which provides insight on what happened |
| **Predictive Analytics Process** | Provides insight on what might happen |

### 2.2 Enterprise Analytical Capabilities

- The infrastructure is created for enterprise-wide analytics
- Analytics are key to business success, and transformation is brought about by opportunity or necessity

### 2.3 A Fact-Based Decision Making Culture

**Scientific Method:**

```
Hypotheses → Procedures (Experiments) → Data (Results) → Findings (Conclusions)
```

### 2.4 The 5 Analytics Layers

| Layer | Guiding Question | Focus Areas |
|---|---|---|
| **Information Layer** | How is data managed and used? | Data Governance, Data Management, Education Data Models |
| **Descriptive Layer** | What is happening or what has happened? | Education Reporting, Financial Performance, Compliance and Risk |
| **Predictive Layer** | What could happen? | Decision Management, Text Analytics, Statistical Analysis |
| **Prescriptive Layer** | How can we achieve the best outcomes? | Student Analytics, Student Retention, Budgeting and Finance |
| **Cognitive Layer** | Tell me the best course of action | Tutoring and Mentoring, Curriculum Development, Early Warning Systems |

### 2.5 Business Analytics Capabilities

- Business Intelligence
- Performance Management
- Predictive Analytics
- Analytical decision management techniques
- Risk Analysis
- Operational Analytics

### 2.6 Business Performance Management

Allows decision makers at virtually all levels of the organization to gain insights into business performance and data, to support and guide actions.

### 2.7 Impact of BAO (Business Analytics & Optimization) on Diverse Industries

Business analytics software and solutions enable organizations to perform various new and important capabilities:

- Foresee, identify, and analyze trends and anomalies
- Compare with "what-if" scenarios
- Gather relevant data and interact with it
- Evaluate and monitor the outcome of the business
- Plan, budget, and predict resources
- Predict possible threats and opportunities
- Automate decision-making wherever needed
- Engage in social interactions with customers
- Estimate and manage risk
- Set operational and strategic decisions

### 2.8 Business Analytics Architecture

- A reference architecture defines the checklist of components that typically make up a BAO solution
- It provides a common solution framework for BAO across all sectors, industries, and solution areas

### 2.9 Introduction to Knowledge Management

- Data is transformed into **information** by including context
- Information is transformed into **knowledge** when an individual interprets it based on their existing knowledge

**Knowledge Creation Process:**

```
Socialization → Externalization → Combination → Externalization
```

### 2.10 Data Mining Process

```
State Problem
      ↓
Collect the Data
      ↓
Preprocessing
      ↓
Estimate Model (Mine Data)
      ↓
Interpret Model & Draw Conclusions
```

### 2.11 Developing and Using KPIs

**KPIs (Key Performance Indicators)** are measurable values that show how well a person, team, or business achieves important goals.

**Main types of KPIs:**

| Type | Description |
|---|---|
| **Leading Indicators** | Predict future results and trends before they happen |
| **Lagging Indicators** | Measure past results and final outcomes |
| **Quantitative Indicators** | Use exact numbers and hard data |
| **Qualitative Indicators** | Track feelings, opinions, and experiences |

**Key qualities of good KPIs:**

- **Accurate** — builds trust in information provided for managerial decision making
- **Consistent** — all concepts and definitions need to be consistent to support comparability and understandability of occurrences and their performance

**KPI Benefits:** Clarifies expectations, improves execution, promotes consistency, gives clear feedback, improves decision-making, promotes understanding.

**Visual Presentation (Status Colors):**

| Color | Meaning | Action |
|---|---|---|
| 🟢 **Green** | Good — exceeds the target level of performance | Praise and recognize the responsible person |
| 🟡 **Yellow** | OK — minimum acceptable threshold | Get an explanation and keep close monitoring |
| 🔴 **Red** | Bad — unacceptable performance | Urgent attention required |

### 2.12 Balanced Scorecard

- Managing and deploying organizational resources to deliver and fulfill organizational objectives is a vital role of senior finance and management professionals
- **Scorecard** — the vision and mission of an organization can be translated into a scorecard representing long-term and short-term goals

### 2.13 Analytics Metrics Lifecycle Process

```
Define → Measure → Analyze → Action → Improve and Eliminate
```

### 2.14 Categorizing Dashboards

A **dashboard** is a visual display of the most important information needed to achieve one or more objectives.

**Types of dashboard data:**

- Dashboards for Strategic purposes
- Dashboards for Analytical purposes
- Dashboards for Operational purposes

### 2.15 Dashboard Design — Rules

| Rule | Description |
|---|---|
| Rule 1 | Who are you trying to impress? |
| Rule 2 | Select the right type of dashboard |
| Rule 3 | Strategic / Executive Dashboards |
| Rule 4 | Make the data relevant to the audience |
| Rule 5 | Don't clutter your dashboard — present the most important metrics only |
| Rule 6 | How often does the data really need to be refreshed |

### 2.16 Design Thinking

Design Thinking is an iterative process in which we seek to:

- Understand the user
- Challenge assumptions
- Redefine problems in an attempt to identify alternative strategies and solutions that might not be instantly apparent with our initial level of understanding

**Life Cycle of Design Thinking:**

```
Materialize → Understand → Explore
```

---

## 3. DevOps

### 3.1 CI/CD Introduction

- **DevOps** — a set of practices to automate and integrate processes between Software Development and IT Teams
- Flow: `Build → Test → Release` — releasing software in a fast and reliable manner
- DevOps adopts agile software delivery methodologies (CI/CD)

**CI/CD Pipeline:**

```
Build → Integration → Testing → Delivery → Deployment
```

| Term | Meaning |
|---|---|
| **Continuous Integration** | Automated builds & tests |
| **Continuous Deployment** | Automatically deploys each validated build to production (a failed test prevents a new change from being deployed) |

**CI/CD Tools:** CircleCI, Jenkins, Bamboo, TeamCity, GitLab

**CI/CD Pipeline flow (tool-agnostic):**
```
Source → Build → Test → Deploy
```

### 3.2 What is DevOps?

It is a set of practices that works to automate and integrate the processes between software development and IT teams, so they can build, test, and release software faster and more reliably.

- DevOps was formed by combining the words "Development" and "Operations"
- It bridges the gap between development and operations teams

### 3.3 Need for DevOps

- Initially, software is developed, tested, and then sent to the operations team
- Before DevOps, there was a significant delay between development and operations
- Developers had to wait for bugs to be reported by the operations department or end users before they could rectify them
- This delayed developers' valuable time, slowing project progress
- **This is where DevOps came into the picture**
- With DevOps, developers need not wait for feedback — notifications are sent to developers for their committed code
- Development and Operations teams collaborate to minimize effort and risk involved in releasing software
- DevOps tools can easily point out the code which leads to failure during the build

### 3.4 Development and Operations

**Without DevOps:**

| Gap | Fixed By |
|---|---|
| Business ↔ Development | Agile fixes this |
| Development ↔ Operations | DevOps fixes this |

| Development | Operations |
|---|---|
| Planning | Infrastructure Management |
| Development | Security & Compliance |
| Testing | Database Admin |
| Quality Assurance | Network Technician |

### 3.5 DevOps Principles

- Incremental Release
- Automation
- DevOps Pipeline
- Continuous Integration
- Continuous Delivery
- Continuous Monitoring
- Feedback Sharing
- Version Control
- Collaboration

### 3.6 DevOps Phases

```
Plan → Code → Build → Test → Release → Deploy → Operate → Monitor
```

### 3.7 Benefits of DevOps

- Faster delivery time
- High collaboration between teams
- Greater customer experience
- Early defect detection
- Continuous release and deployment
- Innovative mindset

### 3.8 DevOps Practices

**Microservices:**
- A design approach to build a single application as a set of small services
- Each service runs in its own process and communicates with other services through a well-defined interface
- Different frameworks or programming languages can be used to write and deploy each microservice

**Continuous Integration** — covered in 3.1

**Continuous Delivery:**
- An extension of continuous integration — it automatically deploys all code changes to a testing and/or production environment after the build stage

**Continuous Deployment** — automatic deployment to production

### 3.9 CI/CD Tools

| Tool | Description |
|---|---|
| **Jenkins** | Open source automation server with many plugins to support building, deploying, and automating any project. Server-based application requiring a web server like Apache Tomcat |
| **CircleCI** | Supports Windows, Linux, Docker, and macOS; runs in the cloud or behind the firewall. Easily readable YAML configuration. Does not require a dedicated server to run. Suitable for small projects. Integrates with code version control — every push creates a pipeline to process and test the code |
| **TeamCity** | A commercial, Java-based build management and CI server by JetBrains. Known for ease of setup, out-of-the-box usability, and a beautiful UI. Installable on Windows and Linux servers. Supports .NET framework and integrates into IDEs like Visual Studio and Eclipse. Build agents can be launched in a Kubernetes cluster. Integrates with Azure DevOps and Jira |
| **Bamboo** | A CI server developed by Atlassian. Has built-in Git branching workflows and integrations with other Atlassian software. Two agent types: **Local agents** (run as part of the Bamboo server process) and **Remote agents** (run on other servers/computers) |
| **GitLab** | GitLab CI/CD was integrated into the main GitLab software from GitLab 8.0. Written in Ruby and Go, launched under an MIT license. Accessible via APIs. GitLab Runner processes builds. A GitLab CI/CD server can manage more than 25,000 users |

**Why GitLab?**
- Dev and Ops teams work together
- Only a single application for the entire DevOps cycle
- Security is built in
- Transparency by default
- Everyone can contribute

### 3.10 CI/CD as a Service

- Azure Pipelines
- AWS Pipelines
- Bitbucket Pipelines
- GitLab Pipelines

> **CI/CD Pipelines** facilitate the software delivery process via stages like Build, Test, Merge, and Deploy.

**Azure DevOps:**
- A collection of services provided by Microsoft Azure
- Provides development services for a team to support, plan, collaborate, build, and deploy
- Provides integrated features in a browser or an IDE
- Key services: Azure Repos, Azure Pipelines, Azure Boards, Azure Test Plans, Azure Artifacts (Azure Pipelines is especially useful)

**AWS CodePipeline:**
- A fully managed continuous delivery service that helps automate release pipelines for fast and reliable application and infrastructure updates
- Lets you model the full release process: building code, deploying to pre-production environments, testing the application, and releasing to production
- You can integrate partner tools and custom tools into any stage of the release process

**Bitbucket Pipelines:**
- An integrated CI/CD service built into Bitbucket
- Automatically builds, tests, and deploys code based on a configuration file in your repository
- Commands run inside containers
- Enables building powerful, automated CI/CD pipelines

**Pipes:**
- Provide a simple way to configure a pipeline
- Especially powerful when working with third-party tools
- A pipe uses a script that lives in a Docker container

**GitLab Pipelines:**
- GitLab is a fully integrated software development platform
- A lifecycle tool that provides a vast repository on web-based DevOps
- With GitLab CI/CD, you can test, build, and publish software with no third-party application or integration needed

### 3.11 CI/CD Pipeline Structure

- Pipelines are the top-level component of continuous integration, delivery, and deployment
- Pipelines comprise:
  - **Jobs** — define **what** to do
  - **Stages** — define **when** to run the jobs
- Jobs are executed by **runners**

---

## 4. DevSecOps

### 4.1 Why DevOps? (Recap)

- Shorter development cycles, faster innovation
- Improved communication and collaboration
- Reduced deployment failures, rollbacks, and time to recover
- Reduced costs and IT headcount

### 4.2 DevOps Principles — CAMS

**CAMS** is a framework/model that assesses a company's ability to adopt DevOps processes.

**CAMS stands for:** **C**ulture, **A**utomation, **M**easurement, **S**haring

CAMS is a set of values used by many DevOps engineers.

### 4.3 CI/CD Recap

| Term | Flow |
|---|---|
| **Continuous Integration** | Build → Test → Merge |
| **Continuous Delivery** | Automatically release to repository |
| **Continuous Deployment** | Automatically deploy to production |

**General Workflow of CI/CD Pipeline:**

```
Version Control → Build → Unit Test → Deploy → Auto Test → Deploy to Production
```

### 4.4 What is DevSecOps?

**DevSecOps** — short for Development, Security, and Operations — automates the integration of security at every phase of the software development lifecycle, from initial design through integration, testing, deployment, and software delivery.

| Model | Components |
|---|---|
| **DevOps** | Development, IT Operations, Application Delivery |
| **DevSecOps** | Development, IT Operations, Application Delivery, **Security** |

### 4.5 DevSecOps Best Practices

- Vulnerability scanning
- Runtime protection
- Adherence to your cloud service provider's standards and policies
- Container and service management

### 4.6 DevSecOps Pipeline Phases

```
Threat Modeling → Scan → Analyze → Remediate → Monitor
```

### 4.7 Secure SDLC and CI/CD Pipeline

- Secure SDLC is a collection of best practices focused on adding security to the standard SDLC
- Security issues can be addressed in the SDLC pipeline well before deployment to production

### 4.8 Embedding Security as Part of the CI/CD Pipeline

Security tooling embedded into the CI/CD pipeline:

| Tool | Full Name |
|---|---|
| **SAST** | Static Application Security Testing |
| **DAST** | Dynamic Application Security Testing |
| **IAST** | Interactive Application Security Testing |
| **SCA** | Software Composition Analysis |

### 4.9 What is Software Component Analysis?

- **Component analysis** is the process of identifying potential areas of risk from the use of third-party and open-source software and hardware components
- Component analysis is a function within an overall **Cyber Supply Chain Risk Management (C-SCRM)** framework

### 4.10 What is Static Application Security Testing (SAST)?

Static Application Security Testing (SAST) is also known as **"white box testing."**

### 4.11 What is Infrastructure as Code (IaC) and Its Benefits?

**Infrastructure as Code (IaC)** automates the provisioning of infrastructure, enabling an organization to develop, deploy, and scale cloud applications with greater speed, less risk, and reduced cost.

### 4.12 Introduction to Ansible

- Ansible is an open source automation platform
- Ansible helps with configuration management, application deployment, and task automation

### 4.13 Tools and Services That Help Achieve IaC

| Tool | Description |
|---|---|
| **Terraform** | A tool from HashiCorp that allows users to write, plan, and create infrastructure as code |
| **Ansible** | An infrastructure automation tool created by Red Hat, the enterprise open source technology provider |
| **CFEngine** | An IT infrastructure tool that allows automation of essential large-scale infrastructure of any complexity while maintaining speed, security, stability, and scalability |
| **Chef** | IaC / configuration management tool |
| **Puppet** | IaC / configuration management tool |
| **SaltStack** | IaC / configuration management tool |
| **Vagrant** | IaC / environment provisioning tool |

---

## Quick Revision Checklist

- [ ] Can state the 4 central tenets of Agile
- [ ] Can recite the 4 values of the Agile Manifesto
- [ ] Can list all 7 Agile principles with at least one benefit each
- [ ] Can differentiate Descriptive vs Predictive vs Prescriptive Analytics
- [ ] Can list all 5 Analytics layers in order, with their guiding question
- [ ] Can list the 4 types of KPIs and the Green/Yellow/Red status meaning
- [ ] Can state the Data Mining Process steps in order
- [ ] Can state the Design Thinking life cycle
- [ ] Can explain why DevOps was needed (the gap it fixes)
- [ ] Can list all 8 DevOps phases in order
- [ ] Can name at least 4 CI/CD tools and one distinguishing fact about each
- [ ] Can differentiate Continuous Integration vs Continuous Delivery vs Continuous Deployment
- [ ] Can expand the CAMS framework
- [ ] Can define DevSecOps and how it differs from DevOps
- [ ] Can list the DevSecOps pipeline phases in order
- [ ] Can expand SAST, DAST, IAST, SCA
- [ ] Can define Infrastructure as Code and name at least 3 IaC tools