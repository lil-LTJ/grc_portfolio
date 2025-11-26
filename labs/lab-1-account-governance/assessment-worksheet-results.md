# Lab 1: AWS Account Governance - Assessment Worksheet

Use this worksheet to evaluate your implementation of the AWS Account Governance controls and reflect on your experience. This will help you document your work for your GRC portfolio.

## Implementation Assessment

### Core Security Controls

Check off each control as you verify its implementation:

| Security Control | Implemented | Notes/Evidence |
|------------------|-------------|---------------|
| IAM Password Policy | success | ![after](https://github.com/lil-LTJ/grc_portfolio/blob/14caf216719f8ca13d1b92ed51ecab9f2afc84b3/Screenshots/after%20password%20remediation.JPG) |
| Multi-Factor Authentication (MFA) | success |*MFA enabled root user*![image alt](https://github.com/lil-LTJ/grc_portfolio/blob/14caf216719f8ca13d1b92ed51ecab9f2afc84b3/Screenshots/MFA%20-Root%20verif.JPG);*MFA enanled Identity center user(s)*![image alt](https://github.com/lil-LTJ/grc_portfolio/blob/14caf216719f8ca13d1b92ed51ecab9f2afc84b3/Screenshots/MFA%20is%20enabled%20for%20Identity%20Center%20user.JPG) |
| CloudTrail with Multi-Region Logging | success | <img src="https://github.com/lil-LTJ/grc_portfolio/blob/14caf216719f8ca13d1b92ed51ecab9f2afc84b3/Screenshots/CloudTrail%20is%20enabled%20with%20proper%20settings.JPG" width="400" alt="CloudTrail Logging" >*CloudTrail enabled with proper settings* |
| CloudTrail S3 Bucket (encrypted, access-controlled) | success |<img src= "https://github.com/lil-LTJ/grc_portfolio/blob/e8014cc01e2baf580a33dd76126ead5be4152586/Screenshots/CloudTrail%20S3%20Bucket%20(encrypted%2C%20access-controlled).JPG" width="400" alt="CloudTrail S3 Bucket (encrypted, access-controlled)"> |
| AWS Config Recorder | success |<img src= "https://github.com/lil-LTJ/grc_portfolio/blob/e8014cc01e2baf580a33dd76126ead5be4152586/Screenshots/AWS%20Config%20is%20enabled%20with%20proper%20settings.JPG" width="400" alt="CloudTrail Logging" >   |
| AWS Config Rules | success | <img width="199" height="105" alt="image" src="https://github.com/user-attachments/assets/d086ed38-e1c3-40e5-a26a-f3ac4cedc169" /> <img width="176" height="678" alt="image" src="https://github.com/user-attachments/assets/9e63c6dd-f06c-4079-99ef-94993f2d96a2" /> |
| Security Hub | success |<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/e9142c1d-d6d8-49a4-a805-253232769164" />|
| IAM Access Analyzer | success |<img width="203" height="877" alt="image" src="https://github.com/user-attachments/assets/8afd66f3-8865-4e9b-8357-f76afd78e1ec" />|
| CloudWatch Alarms for Security Events | success |<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/34b1fcc4-2ea1-4f63-8a8e-42c16cf92adc" />|
| SNS Topic for Alerts | success |<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/4046e4bd-c09a-4463-8bf8-09d07e6194cf" />|
| AWS Budget with Notifications | success |<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/762025d5-8f83-4adb-9432-eb73ebcf566d" />|

### AWS Config Rule Compliance

List the AWS Config rules you've implemented and their compliance status:

| Rule Name | Compliance Status | Non-Compliant Resources |
|-----------|-------------------|-------------------------|
|IAM Password Policy check |success |corrected |
|Root account MFA check |success | n/a |
|IAM User MFA check |success | n/a |
|CloudTrail enabled check |success |n/a|
|S3 bucket public write protection check |success | n/a |


### Security Hub Standards

List the Security Hub security standards you've enabled and their current scores:

| Security Standard | Current Score | Critical/High Findings |
|-------------------|---------------|------------------------|
| AWS Foundational Security Best Practices | 44%|<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/92f3557a-ef15-4dc4-b850-1a0bce7cff0c" /> |
| CIS AWS Foundations Benchmark |38% |<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/8aca6bd0-9e49-4d3e-a392-2c736a5da095" />|
| PCI DSS |56% |<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/729829b9-53d2-47da-8d26-72ef0ca704e7" />|

## Open-Ended Reflection Questions

Take time to reflect on the following questions. Your answers will demonstrate your understanding of cloud security concepts and help build your GRC portfolio.

### 1. Security Posture Evaluation

```
How would you characterize the overall security posture achieved by implementing these controls? What are the strongest elements and what gaps remain?
 The posture of the organisation improved and was able to get data on breaches as and when testing was being conducted. The passwrod policy which was non compliant was corrected to enusure a stonger one. Enabling security hub (guardduty etc) allowed me to see configuration gaps in my account. The sns notification on my budget also prompted me to ensure all cleanup were done to avoid going beyoud budget limit.

The security posture however can be improved as the current scores and less than average

```

### 2. Alignment with Security Frameworks

How do the controls implemented in this lab align with industry security frameworks (such as NIST CSF, ISO 27001, or CIS Controls)? Identify specific domains or control families.

```
|Framework	  |Primary Domain/Control Family Addressed	|Key Controls Implemented                         |
|NIST CSF 	  |Protect, Detect, Respond	                |MFA, Logging & Monitoring, IAM, Security Baseline|
|CIS Controls |v8	CIS CSC 1, 4, 5, 6, 8	            |Account Hardening, MFA, Monitoring, Audit Logging    |
|ISO 27001	  |A.5, A.8, A.9, A.12, A.16	            |Access Control, Asset Management, Operations Security|
|PCI DSS	  |Req 1, 2, 7, 8, 10	                    |Network & System Security, Access Control, Logging   |
|GDPR	      |Art. 5, 25, 32	                        |Data Protection by Design, Security of Processing    |
|HIPAA	      |§164.308, §164.312                       |Administrative & Technical Safeguards            |

```

### 3. Business Risk Reduction

Identify 3-5 specific business risks that are mitigated by the security controls you've implemented. How would you explain the value of these controls to non-technical executives?

```
1. Risk: Unauthorized Access and Data Breach (Mitigated by Modules 1 & 4)
Mitigating Data Breach & Reputational Harm
"We've installed a digital bodyguard on every door to our data, backed up by a 24/7 alarm system. 
This set of controls significantly reduces the chance of a costly data breach—the single biggest financial risk we face in the cloud. 
By requiring Multi-Factor Authentication (MFA) and constantly scanning for data that is accidentally made public, 
we are protecting our customers' privacy and our company's reputation and brand integrity from being damaged by a major security incident."

2. Risk: System Downtime and Business Interruption (Mitigated by Module 2 & 3)
"Our new monitoring system, CloudTrail and CloudWatch Alarms, is like a flight recorder and a fast-response team combined. 
It records every action taken in our cloud environment. If someone—whether a malicious actor or an employee making an honest mistake—tries 
to shut down a critical service or delete important data, the system instantly creates an audit trail and triggers a high-priority alert. 
This capability ensures that we can detect major issues within minutes, recover quickly, and maintain continuous service availability, 
protecting our revenue stream from unexpected outages."

3. Risk: Non-Compliance and Audit Failure (Mitigated by Modules 3 & 4)
"The AWS Config and Security Hub tools give us a unified, real-time score card on compliance with standards like PCI DSS or HIPAA. 
Instead of scrambling for a manual audit every year, the system continuously verifies that our configurations meet mandatory regulations. 
This proactive approach ensures we pass compliance audits the first time, 
avoiding penalties and ensuring we can continue to operate in regulated markets and handle sensitive data like credit card information without interruption."

4. Risk: Uncontrolled Spending ("Cloud Bill Shock")
"By setting up AWS Budgets, we're not just managing costs, we're managing risk. 
Uncontrolled spikes in our cloud bill can indicate a security event, 
such as a denial-of-service attack leveraging our infrastructure or a misconfigured process running out of control. 
Our budget alerts act as an early warning system for financial anomalies, 
allowing us to investigate and shut down potentially harmful activity before it causes significant and unauthorized expense."

```

### 4. Advanced Security Architecture

If you were designing a more advanced security architecture for an enterprise, what additional services or features would you incorporate? Why?

```
Security Domain	    | Additional Services/Features	                            | Primary Business Rationale
Network Security	  | AWS Network Firewall, VPC Design, PrivateLink	            | Isolate critical systems and prevent data exfiltration
Data Protection	    | AWS Shield, Macie, KMS (Advanced)	                        | Protect against direct attacks and classify/protect sensitive data
Identity & Access	  | IAM Roles Anywhere, Control Tower, Permissions Boundaries	| Secure hybrid workloads and enforce guardrails at scale
Threat Detection	  | GuardDuty, Detective	                                    | Find active threats and accelerate investigations
Incident Response	  | Incident Response Playbooks (using Lambda, SSM)	          | Automate containment to reduce "dwell time" and impact
```

### 5. Automation Opportunities

Which aspects of the security implementation could benefit most from automation? How would you approach automating these controls for a large-scale deployment?

```
1. Centralized Remediation and Configuration Deployment
This approach focuses on Governance-as-Code (GaC) and automated self-healing.
   #Service: AWS Config Rules with Automatic Remediation
     How to Automate: For rules like S3 bucket public write protection check (deployed in Step 3.2), 
     configure the rule to trigger a Systems Manager Automation document or a Lambda function when a resource is marked NON_COMPLIANT.
     Example Remediation: If a new S3 bucket is created with public read access, 
     the Lambda function is triggered and immediately modifies the bucket policy to block public access, effectively self-healing the environment.
   
   #Service: AWS CloudFormation/AWS CDK (Infrastructure-as-Code)
     How to Automate: Instead of deploying CloudTrail (Step 2.1) and Config (Step 3.1) manually in each account, use a multi-account deployment tool like AWS              CloudFormation StackSets or AWS Organizations' Custom Configuration to deploy the required resources 
     (CloudTrail, Config Recorder, IAM Access Analyzer) consistently across all accounts in the Organization from a central "Management" or 
     "Security Tooling"account.

2. Security Orchestration, Automation, and Response (SOAR)
This focuses on automating the response to the alarms created in Module 2 and 4.
#Service: AWS Security Hub and Amazon EventBridge
How to Automate: Configure an EventBridge rule in the central security account to subscribe to high-severity 
findings from Security Hub (Module 4) or specific CloudWatch Alarms (Module 2).

SOAR Workflow: The EventBridge rule forwards the finding to an AWS Step Functions workflow. This workflow:
1. Enriches: Calls AWS APIs to pull associated logs and metadata (e.g., who the user was, the resource owner).
2. Contains: If the finding involves a compromised IAM user, the workflow automatically attaches a Deny/Quarantine policy to the user or role.
3. Notifies: Creates a ticket in the external ticketing system (e.g., Jira, ServiceNow) and notifies the relevant team in Slack/email.

3. Identity and Access Management (IAM) Lifecycle
This aims to automate user management and access provisioning (Module 1).
#Service: AWS IAM Identity Center with SCIM Provisioning
   How to Automate: Link IAM Identity Center (Step 1.2) to an external corporate Identity Provider (IdP) like Okta or 
   Azure AD using the System for Cross-domain Identity Management (SCIM) protocol.

Automation Benefit: When a new employee is hired, creating their account in the IdP automatically provisions them in 
Identity Center and assigns them to the correct group. When an employee leaves, their account is immediately de-provisioned and access is revoked, 
solving the high-risk manual de-provisioning problem.

```

### 6. Custom Approach to Challenges

Did you take any unique approaches to solving the challenges in this lab? What motivated your approach?

```
I followed the step by step procedure. However some steps i had to do a little more research ie creating custom metrics for rootlogin etc to complete the task.

```

### 7. Cost-Security Tradeoffs

What tradeoffs between security and cost did you identify during this implementation? How would you optimize these tradeoffs in different contexts (e.g., startup vs. enterprise)?

```
The security implementation involved several direct tradeoffs between security posture and operational cost, 
as well as indirect costs associated with operational complexity. 
A GRC engineer must deliberately manage these tradeoffs based on the organization's risk appetite and context.

```
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/56903386-3f59-4466-983c-b6553f1e60be" />


## Implementation Evidence

Document evidence of your implementation here. Include:

### Screenshots
- [ ] IAM Password Policy configuration
- [ ] CloudTrail configuration
- [ ] AWS Config rule compliance dashboard
- [ ] Security Hub summary screen
- [ ] CloudWatch Alarms configuration
- [ ] Budget configuration

### Command Line Output

Include the output from the `verify-compliance.sh` script:

```
[Paste script output here]
```

Include the output from the `security-posture-report.sh` script:

```
[Paste script output here]
```

### Architecture Diagram

- [ ] I've created an architecture diagram showing the security controls implemented
- [ ] Location of diagram file: _______________________

## Next Steps and Improvements

Based on your implementation and assessment, what would be your next priorities for improving the security posture of this AWS account? List at least three specific enhancements.

1. Implement Network-Level Monitoring and Protection (GuardDuty & VPC Flow Logs)
The current implementation focused heavily on Identity, Configuration, and API activity (CloudTrail) but has a significant gap in Network Visibility.

Specific Enhancement: Enable and Tune Amazon GuardDuty and ensure VPC Flow Logs are enabled for all VPCs.

2. Implement Container and Compute Vulnerability Management (Amazon Inspector)
The current AWS Config rules check the security configuration of resources but do not check the security content (operating systems, application code, and dependencies) within those resources.

Specific Enhancement: Enable and Integrate Amazon Inspector to continuously scan Amazon EC2 instances, Amazon ECR container images, and AWS Lambda functions.

3. Establish and Enforce Security Service Control Policies (SCPs)
While the lab used AWS Config to detect non-compliance, a stronger security posture requires preventing high-risk configurations from being deployed in the first place.

## Personal Learning Outcomes

What are the most important insights or skills you gained from completing this lab?

```
In setting up your AWS account(s), the security posture implemented must take into account the risk appetite of the organisation, consider implementation trade offs whiles putting in measures to optimise the secure posture of the organisation.
Automation is also key to avoid burdening the team in manually checking for compliance status of environment.

```

## Additional Notes

Use this space for any additional thoughts, observations, or lessons learned:

```
Additional task is to create mitigation plan for all critical and high findings in the account.
``` 
