---
title: "Event 2: FCAJ Community Day"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---


# Harvest Report: "FCAJ Community Day (23-05-2026)"

### General Event Information
*   **Event Name:** FCAJ Community Day
*   **Date:** May 23, 2026 (Weekend Morning)
*   **Location:** 36th Floor, Bitexco Financial Tower, 02 Hai Trieu Street, Saigon Ward, Ho Chi Minh City
*   **Organizers:** AWS Study Group in collaboration with the FCAJ Community
*   **Role:** Attendee

---

### Event Objectives
*   **Program Goal:** Not just a standard technical seminar, the event serves as a platform for connection, networking, and mutual inspiration among IT professionals.
*   **Core Message:** Covering themes ranging from AI and Cloud to real-world experiences from industry experts. Key discussions explored Prompt optimization, AWS services application (such as CloudFront), Hackathon journeys, and Enterprise-grade AI architecture design.
*   **Value for Attendees:** Help participants understand job market dynamics under the influence of AI, prepare strong technical foundations to avoid obsolescence, and equip themselves with problem-solving mindsets for real-world enterprise scenarios.

---

### Speaker List
*   **Quynh Mai:** MC and host of the event.
*   **Nguyen Gia Hung:** Head of Solution Architecture at AWS Vietnam and Founder of the FCAJ community.
*   **Tinh:** Platform Engineer at Gotam X.
*   **Hai Anh:** Pacific Vietnam, previously presented at AWS Singapore Summit and Silicon Valley.
*   **Thinh:** DevOps Engineer at UTM Group, presenting the team's Hackathon project.
*   **Duc:** LLM Optimization Specialist.
*   **Vy:** VPBank, presenting on Enterprise Multi-Agent systems.

---

### Key Highlights

#### 1. Analysis of Current Realities
*   **New Job Demand:** AI decreases software development costs, which in turn increases the aggregate demand for software products. This shifts job creation towards infrastructure management (Platform Engineering) and AI code auditing/debugging.
*   **AI Limitations:** Generating code via AI without system architecture context leads to low-quality codebases prone to LLM hallucinations.

#### 2. Solutions Presented
*   **Contextual Prompting:** Always supply clear context (Context/System Prompts) using structure: *Goal, Persona, Format* instead of general open-ended questions.
*   **Multi-Agent Architectures:** Implement Multi-Agent Systems to divide and conquer complex workflows (e.g., startup credit analysis) instead of routing all instructions to a single model.

#### 3. Technology, Services, and Tools
*   **AWS Services:** CloudFront (Flat-rate pricing, content compression, DDoS protection), AWS Bedrock, EC2, Lambda, VPC.
*   **AI/LLM:** Amazon Agent platform, Obsidian (Second Brain knowledge management), Model Context Protocol (MCP).
*   **Infrastructure:** Terraform (Infrastructure as Code - IaC).

#### 4. Demos and Case Studies
*   **UTM Morpo Project:** Demoed a tool using 3 AI agents to convert UI sketches into HTML code, allowing users to edit via drag-and-drop (a Hackathon winning project).
*   **LLM Parameter Demo:** Compared LLMs set to Temperature = 0 running locally versus Bedrock on the Cloud. Proved that Cloud endpoints still show small variances due to backend inference optimizations.
*   **Enterprise Requirements:** In enterprise settings, compliance, security, and guardrails take priority over the quantity of AI integrations.

---

### Key Takeaways

#### 1. Design Mindset
*   Remember that LLM is a **Probabilistic Engine**; do not assume it will always yield identical answers even with Temperature = 0.
*   Do not leave systems on full auto-pilot; implement human oversight (**Human in the loop**).

#### 2. Infrastructure Knowledge
*   Learned how AWS CloudFront optimizes delivery costs through Flat-rate pricing, helping enterprises avoid billing shocks from traffic spikes or DDoS attacks.

#### 3. Best Practices
*   Avoid the **"Internet Puller"** syndrome (blindly copying online code snippets/tools without understanding their context and system compatibility).
*   For Hackathons, tightly manage project scope and limit over-generation of ideas. Focus on solving a singular core problem within the 36-hour timeframe.

---

### Applying to Work
*   **Project Applications:** Design multi-agent AI workflows assigning specific duties to dedicated agents (e.g., financial analyst agent, market researcher agent). Configure mTLS and VPC Origins for enhanced backend security.
*   **Technologies to Experiment with:** Use Terraform for Infrastructure as Code (IaC) to manage environment versioning. Utilize AWS CloudFront edge security features (geo-blocking, bot blocking).
*   **Workflow Optimization:** Automate meeting summaries and dashboard updates using AI Agents integrated with libraries (such as MCP connecting Excel) instead of manual data pulling.

---

### Event Experience
*   **Career Growth:** Gained insights into the 5 pillars of hiring: *Salary, Experience, Network, Knowledge, and Profile*.
*   **Security awareness:** Understood warnings regarding copy-pasting raw ChatGPT code directly into enterprise systems, which can compromise coding standards and open security vulnerabilities.

---

### Lessons Learned
*   **Foundational Knowledge:** Core engineering concepts, university degrees, and Software Engineering basics remain essential. AI is a productivity multiplier, not a replacement for fundamental engineering skills.
*   **Business Justification:** When pitching AI projects to leadership, always present the return on investment (ROI) and cost-savings statistics.
*   **System Integrity:** When building systems, ensure that they are not only functional but also *"secure, reliable, and serve the user's actual needs"*.

---

### Event Photos

![Speaker presenting Agenda](/images/4-EventParticipated/fcaj_community_day_2305_1.jpg)
*Figure 1: Speaker introducing the event agenda and session outlines*

![Context is Everything Slide](/images/4-EventParticipated/fcaj_community_day_2305_2.jpg)
*Figure 2: Slide on "Context is Everything - Making AI Actually Work for You"*

![Hackathon Project Presentation](/images/4-EventParticipated/fcaj_community_day_2305_3.jpg)
*Figure 3: Speaker sharing the 36-hour journey of building UTM Morpo*

![Group photo with FCAJ community](/images/4-EventParticipated/fcaj_community_day_2305_4.jpg)
*Figure 4: Group photo with experts and FCAJ community members*
