# Incident Response, Business Continuity, and Disaster Recovery

## Cybersecurity Study Notes

## 1. Components of an Incident Response Plan

An **Incident Response Plan (IRP)** documents the procedures employees and response teams must follow when a security incident occurs. It supports the organization's incident response policy and translates organizational goals, strategy, and mission into practical actions.

An incident response plan may include technical procedures, checklists, tools, communication protocols, standards, and role-specific responsibilities. It should be treated as a living document and updated as the organization, its systems, and its risks change.

### 1.1 Preparation

Preparation establishes the people, processes, and resources required to respond effectively.

Key activities include:

- Develop an incident response policy approved by management.
- Identify critical data, systems, and single points of failure.
- Train staff to recognize and report incidents.
- Establish an incident response team.
- Practice incident identification and first-response procedures.
- Define roles and responsibilities.
- Plan communication and coordination among stakeholders.
- Establish alternative communication methods in case the primary method is unavailable.

**Example:** An organization prepares an emergency contact list that includes an alternative communication channel in case email becomes unavailable during a cyberattack.

### 1.2 Detection and Analysis

This phase identifies suspicious activity, determines whether an incident has occurred, and assesses its significance.

Key activities include:

- Monitor possible attack vectors.
- Analyze events using available data and threat intelligence.
- Determine whether an event qualifies as a security incident.
- Prioritize incidents according to severity, impact, and urgency.
- Standardize incident documentation.

**Example:** Security monitoring detects unusual administrator activity. Analysts investigate the logs, compare the activity with expected behavior, and determine whether an account may have been compromised.

### 1.3 Containment, Eradication, and Recovery

This phase limits the incident's impact, removes the cause where possible, and restores secure operations.

The supplied course identifies these activities:

- Gather evidence.
- Choose an appropriate containment strategy.
- Identify the attacker, where possible.
- Isolate the attack.

The phases can be understood as follows:

- **Containment:** Limit the spread or impact of the incident.
- **Eradication:** Remove malicious artifacts, unauthorized access, or the underlying cause.
- **Recovery:** Restore systems and services to reliable operation and verify that they are functioning securely.

**Example:** If a workstation is suspected of running malware, the response team may isolate it from the network, preserve relevant evidence, remove the malicious software, and restore the system after validating its security.

### 1.4 Post-Incident Activity

Post-incident work helps the organization understand what happened and improve future response.

Activities include:

- Identify evidence that must be retained.
- Document lessons learned.
- Review the effectiveness of the response.
- Record relevant findings and corrective actions.

A retrospective should examine the preparation, detection and analysis, containment, eradication and recovery, and post-incident activities.

**Example:** After an incident, the organization discovers that an alert was missed because a monitoring rule was incorrectly configured. The team documents the issue and improves the detection process.

### 1.5 Incident Response Lifecycle Summary

| Phase | Main purpose | Typical activities |
|---|---|---|
| Preparation | Establish readiness | Policies, training, team formation, communication planning |
| Detection and Analysis | Identify and understand incidents | Monitoring, investigation, threat intelligence, prioritization |
| Containment, Eradication, and Recovery | Limit damage and restore secure operations | Evidence collection, isolation, removal of malicious activity, recovery |
| Post-Incident Activity | Learn and improve | Evidence retention, documentation, lessons learned |

**Reference named in the course:** NIST SP 800-61 Rev. 2, *Computer Security Incident Handling Guide*.

---

## 2. Incident Response Team

An **incident response team** is a group of trained individuals responsible for coordinating the investigation, containment, recovery, and improvement activities associated with security incidents.

Organizations may use a dedicated team, leverage existing employees, or combine these approaches depending on their size and requirements.

### 2.1 IT Professionals as First Responders

IT professionals are often the first people to encounter suspicious system behavior. They need training to distinguish routine technical problems from potential security incidents.

For example:

- A normal application failure may require standard troubleshooting.
- Unexpected administrator activity, unexplained data transfers, or suspected malware may require security incident reporting and escalation.

The first responder should follow organizational procedures rather than making unapproved changes that could destroy evidence or increase the damage.

### 2.2 Potential Incident Response Team Members

The supplied course identifies the following potential team members:

- **Senior management representatives:** Provide organizational direction and decisions.
- **Information security professionals:** Investigate security events, assess threats, and coordinate technical response.
- **Legal representatives:** Advise on legal obligations, evidence handling, and relevant legal issues.
- **Public affairs or communications representatives:** Coordinate appropriate internal and external communications.
- **Engineering representatives:** Provide system and network expertise.

The precise team composition depends on the organization's structure and the nature of the incident.

### 2.3 Responsibilities of the Team

Team members should be trained in incident response and the organization's incident response plan.

Their activities may include:

- Investigating the incident.
- Assessing the damage.
- Collecting and preserving evidence.
- Reporting the incident.
- Initiating recovery procedures.
- Supporting remediation.
- Conducting root-cause analysis.
- Participating in lessons-learned reviews.

### 2.4 Four Primary Responsibilities

According to the supplied course, an incident response team has four primary responsibilities:

1. Determine the amount and scope of damage caused by the incident.
2. Determine whether confidential information was compromised.
3. Implement necessary recovery procedures to restore security and recover from incident-related damage.
4. Supervise additional security measures intended to improve security and prevent recurrence.

### 2.5 CIRT and CSIRT

Organizations may establish a dedicated team known as a:

- **Computer Incident Response Team (CIRT)**
- **Computer Security Incident Response Team (CSIRT)**

These terms refer to teams that handle computer or cybersecurity incidents. Exact organizational names and responsibilities vary.

### 2.6 Incident Response Team Checklist

- [ ] Team membership and responsibilities are documented.
- [ ] Team members have appropriate training.
- [ ] Escalation procedures are defined.
- [ ] Contact details and backup communication methods are available.
- [ ] Evidence-handling procedures are documented.
- [ ] Recovery responsibilities are assigned.
- [ ] Lessons-learned activities are included in the process.

---

## 3. Business Continuity Planning

**Business Continuity (BC)** consists of actions, processes, and tools intended to help an organization continue critical operations during a contingency.

A **Business Continuity Plan (BCP)** documents the predetermined instructions and procedures used to sustain business processes during and after a significant disruption.

Business continuity is primarily concerned with maintaining critical business functions. Technology must support business requirements, but continuity planning also involves people, facilities, suppliers, communications, and operational processes.

### 3.1 Components of a Business Continuity Plan

A comprehensive BCP commonly includes:

1. **BCP team information**
   - Team members.
   - Multiple contact methods.
   - Backup personnel.

2. **Immediate response procedures**
   - Security and safety procedures.
   - Fire-suppression procedures.
   - Notifications to appropriate emergency-response agencies.

3. **Notification systems**
   - Alerting procedures.
   - Call trees for informing employees and stakeholders that the plan has been activated.

4. **Management guidance**
   - Decision-making responsibilities.
   - Designation of authority for specific managers.

5. **Plan activation criteria**
   - Conditions under which the plan should be enacted.
   - Procedures for activating the plan.

6. **Critical external contacts**
   - Vendors.
   - Customers.
   - Supply-chain partners.
   - Third-party service providers.
   - External emergency providers.

### 3.2 Business Impact Analysis (BIA)

A **Business Impact Analysis (BIA)** examines business functions, system requirements, and dependencies to establish priorities for disruption planning.

It helps the organization understand:

- Which business functions are most important.
- Which systems and resources support those functions.
- How disruption affects other departments and customers.
- Which dependencies must be restored first.
- What level of interruption the organization can tolerate.

The BIA supports continuity and recovery decisions. The course emphasizes that a recent BIA can help identify dependencies and establish priorities before a disruption occurs.

### 3.3 Business Continuity Example: Billing Department Fire

Consider a company whose billing department is destroyed by a fire overnight.

A BIA completed four months earlier identified billing as important, but determined that a short interruption would not immediately stop other business functions.

The company has a prior agreement for an alternative workspace that can be made available in less than one week. Until that workspace is ready, customer service staff handle billing inquiries. Billing employees temporarily work at the alternative location and remain there until a permanent facility is available.

#### Why the plan works

- The organization identified the billing function's importance in advance.
- The company understood the dependencies between billing inquiries and revenue.
- Alternative workspace arrangements had already been made.
- Customer service could temporarily handle inquiries.
- The company had sufficient cash reserves to tolerate the short delay.

**Lesson:** Business continuity planning is proactive. It establishes alternatives and responsibilities before a disruption happens.

### 3.4 Business Continuity Checklist

- [ ] Critical business functions have been identified.
- [ ] A BIA has been completed and reviewed.
- [ ] Primary and backup team members are listed.
- [ ] Contact details include alternative methods.
- [ ] Plan activation conditions are defined.
- [ ] Emergency procedures are documented.
- [ ] Alternative facilities or working arrangements are identified where needed.
- [ ] Critical vendors and external partners can be contacted.
- [ ] Temporary operating arrangements are defined.
- [ ] The plan is reviewed and tested periodically.

---

## 4. Disaster Recovery Planning

**Disaster Recovery (DR)** focuses on restoring IT and communications services and systems during and after an outage, disruption, or disaster.

A **Disaster Recovery Plan (DRP)** documents the processes, policies, and procedures used to recover critical technology infrastructure, systems, applications, and related services.

The goal described in the course is to restore the business to full, last-known reliable operations.

### 4.1 Business Continuity versus Disaster Recovery

Business continuity and disaster recovery are related, but they have different primary objectives.

| Business Continuity (BC) | Disaster Recovery (DR) |
|---|---|
| Focuses on maintaining critical business functions during a disruption. | Focuses on restoring IT and communications services and systems. |
| Includes people, processes, facilities, suppliers, and operational arrangements. | Includes technology recovery procedures, backup systems, infrastructure, and applications. |
| May use temporary work locations or alternative workflows. | May restore services from backups or alternative technical environments. |
| Helps the organization continue operating despite disruption. | Helps return technology services to reliable operation. |

The recovery of a business function can sometimes occur independently of IT recovery. However, IT and communications are often essential to sustaining business operations.

### 4.2 Components of a Disaster Recovery Plan

The supplied course identifies several document types that may be maintained for different audiences.

#### Executive summary

Provides a high-level overview of the disaster recovery plan.

#### Department-specific plans

Describe recovery activities relevant to individual departments.

#### Technical guides

Provide instructions for IT personnel responsible for implementing and maintaining backup systems and restoring technical services.

#### Full plan copies

Provide critical disaster recovery team members with the detailed plan they need to carry out their responsibilities.

#### Role-specific checklists

- Disaster recovery team members use checklists to guide actions during a disruption.
- IT personnel use technical guides to bring alternative sites or systems online.
- Managers and public relations personnel use high-level documents to communicate accurate information without unnecessarily interrupting technical recovery teams.

### 4.3 Disaster Recovery Checklist

- [ ] Critical IT systems and communications services are identified.
- [ ] Backup systems and recovery procedures are documented.
- [ ] Technical restoration guides are available.
- [ ] Department-specific recovery requirements are documented.
- [ ] Disaster recovery team members know their responsibilities.
- [ ] Role-specific checklists are available.
- [ ] Alternative recovery arrangements are documented where applicable.
- [ ] Recovery procedures are tested and updated.

---

## 5. How Incident Response, Business Continuity, and Disaster Recovery Work Together

These plans address different but related problems.

### Incident Response (IR)

Responds to security incidents by identifying, analyzing, containing, and addressing them while limiting their impact.

### Business Continuity (BC)

Helps the organization maintain critical business functions during a crisis or significant disruption.

### Disaster Recovery (DR)

Restores IT and communications systems and services to reliable operation after disruption.

### Comparison Table

| Feature | Incident Response | Business Continuity | Disaster Recovery |
|---|---|---|---|
| Primary focus | Security incidents | Continued business operations | Restoration of IT and communications |
| Main concern | Detecting, analyzing, and managing incidents | Keeping critical functions operating | Recovering technology services |
| Typical trigger | Suspected or confirmed security incident | Disruption threatening business operations | Loss or interruption of technology services |
| Typical activities | Investigation, containment, evidence handling, remediation | Alternative workflows, communications, temporary facilities | Backup restoration, system recovery, technical validation |
| Key planning output | Incident Response Plan (IRP) | Business Continuity Plan (BCP) | Disaster Recovery Plan (DRP) |

These plans should be coordinated. A security incident may trigger all three: the incident response team investigates and contains the threat, business continuity procedures sustain critical services, and disaster recovery procedures restore affected technology.

The course summary describes DR as stepping in when normal operations cannot be maintained through incident response and business continuity measures. In practice, the plans may be activated concurrently rather than strictly one after another.

---

## 6. Key Terms and Definitions

The definitions below follow the supplied course material, with wording clarified where needed for readability.

| Term | Definition |
|---|---|
| **Adverse Event** | An event with a negative consequence, such as a system crash, network packet flood, unauthorized use of privileges, webpage defacement, or execution of malicious code that destroys data. |
| **Breach** | An occurrence involving loss of control, compromise, unauthorized disclosure, unauthorized acquisition, or similar access to personally identifiable information, including access by an authorized user for an unauthorized purpose. The supplied course cites NIST SP 800-53 Rev. 5. |
| **Business Continuity (BC)** | Actions, processes, and tools used to help an organization continue critical operations during a contingency. |
| **Business Continuity Plan (BCP)** | Predetermined instructions and procedures describing how business processes will be sustained during and after a significant disruption. |
| **Business Impact Analysis (BIA)** | Analysis of system requirements, functions, and dependencies used to characterize contingency requirements and priorities. |
| **Disaster Recovery (DR)** | Activities needed to restore IT and communications services during and after an outage, disruption, or disturbance. |
| **Disaster Recovery Plan (DRP)** | Documented processes, policies, and procedures for recovering critical business functions, technology infrastructure, systems, and applications after a disaster. |
| **Event** | An observable occurrence in a network or system. |
| **Exploit** | A method or attack that takes advantage of a vulnerability. |
| **Incident** | An event that actually or potentially jeopardizes the confidentiality, integrity, or availability of an information system or the information it processes, stores, or transmits. |
| **Incident Handling** | Activities intended to mitigate violations of security policies and recommended practices. |
| **Incident Response (IR)** | Actions used to manage and mitigate security incidents and their consequences. |
| **Incident Response Plan (IRP)** | Predetermined instructions or procedures for detecting, responding to, and limiting the consequences of security incidents or cyberattacks. |
| **Intrusion** | A security event, or combination of events, involving an intruder gaining or attempting to gain unauthorized access to a system or resource. |
| **Security Operations Center (SOC)** | A centralized organizational function that monitors, detects, and analyzes security events to help prevent and resolve issues before they cause business disruption. |
| **Vulnerability** | A weakness in an information system, security procedure, internal control, or implementation that could be exploited or triggered by a threat source. |
| **Zero-day** | A vulnerability that is unknown to, or not yet adequately addressed by, the parties responsible for developing or defending the affected system. The term is commonly associated with exploitation before an effective fix is available. |

### Important distinction: Event versus Incident

- An **event** is something observable that happens in a system or network.
- An **incident** is an event—or combination of events—that actually or potentially threatens the confidentiality, integrity, or availability of systems or information.

Not every event is a security incident. Analysis is needed to determine its significance.

---

## 7. Practical Scenario: Ransomware Incident

Imagine that an employee reports that several files have become inaccessible and a ransom message appears on the computer.

### Incident Response

1. The employee reports the suspicious activity.
2. The response team investigates and determines whether a security incident has occurred.
3. The affected device may be isolated to limit the spread.
4. Relevant evidence and logs are preserved.
5. The team assesses the scope and whether confidential information may have been compromised.
6. The team removes the threat and restores systems through approved procedures.
7. Lessons learned are documented.

### Business Continuity

1. Identify which business functions are affected.
2. Prioritize critical services.
3. Use approved alternative workflows where possible.
4. Notify relevant personnel and stakeholders.
5. Maintain essential business operations while affected systems are unavailable.

### Disaster Recovery

1. Identify which systems and services require restoration.
2. Use appropriate recovery procedures and backups.
3. Restore systems in a planned priority order.
4. Validate that restored systems are reliable and secure.
5. Return services to normal operation according to organizational procedures.

**Important:** Restoring a system from backup alone does not necessarily resolve the incident. The organization must also address the cause of the compromise and verify that restored systems can be operated securely.

---

## 8. Revision Questions

Try answering these questions without looking at the notes.

1. What is the purpose of an Incident Response Plan?
2. Name the four main phases of the incident response lifecycle in the supplied course.
3. What activities belong to the preparation phase?
4. Why should organizations establish alternative communication methods?
5. How does detection and analysis differ from containment?
6. What is the difference between containment, eradication, and recovery?
7. What is the purpose of post-incident activity?
8. Why must IT professionals be trained as incident first responders?
9. Name five types of representatives who may participate in an incident response team.
10. What are the four primary responsibilities of an incident response team?
11. What is the difference between a CIRT and the general IT support team?
12. What is the purpose of business continuity planning?
13. What is a Business Impact Analysis?
14. How did the alternative workspace help the billing department in the course scenario?
15. What is the primary focus of disaster recovery planning?
16. Name five components or document types that may be included in a DRP.
17. Compare IR, BC, and DR.
18. What is the difference between an event and an incident?
19. What is a vulnerability?
20. What is an exploit?
21. What is a Security Operations Center?
22. Why should incident response, business continuity, and disaster recovery plans be coordinated?

---

## 9. Self-Assessment Checklist

- [ ] I can explain the purpose of an Incident Response Plan.
- [ ] I can describe preparation, detection and analysis, containment, eradication and recovery, and post-incident activity.
- [ ] I can explain the role of an incident response team.
- [ ] I can identify the team's primary responsibilities.
- [ ] I can explain the purpose of business continuity planning.
- [ ] I understand how a Business Impact Analysis supports continuity planning.
- [ ] I can describe the purpose and common components of a disaster recovery plan.
- [ ] I can distinguish incident response from business continuity and disaster recovery.
- [ ] I can define the key terms in the glossary.
- [ ] I can apply IR, BC, and DR concepts to a realistic cybersecurity scenario.

---

## 10. Source and Accuracy Notes

These notes are based primarily on the course material supplied for this topic.

- The incident response lifecycle in the supplied material references **NIST SP 800-61 Rev. 2**.
- The supplied glossary references NIST publications and other sources for certain definitions.
- The notes preserve the course's core concepts while clarifying wording and organizing the material for revision.
- The course's statement that disaster recovery follows when incident response and business continuity fail is best understood as a simplified teaching model. In real organizations, IR, BC, and DR activities can overlap or be activated in parallel.
- For legal, regulatory, or operational use, consult the applicable current standards, policies, and official guidance rather than relying only on study notes.
