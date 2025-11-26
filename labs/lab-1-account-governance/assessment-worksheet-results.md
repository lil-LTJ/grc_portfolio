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
| Security Hub | success |<img width="1693" height="1032" alt="image" src="https://github.com/user-attachments/assets/e9142c1d-d6d8-49a4-a805-253232769164" />|
| IAM Access Analyzer | success |<img width="203" height="877" alt="image" src="https://github.com/user-attachments/assets/8afd66f3-8865-4e9b-8357-f76afd78e1ec" />|
| CloudWatch Alarms for Security Events | success |<img width="203" height="597" alt="image" src="https://github.com/user-attachments/assets/34b1fcc4-2ea1-4f63-8a8e-42c16cf92adc" />|
| SNS Topic for Alerts | success |<img width="173" height="312" alt="image" src="https://github.com/user-attachments/assets/4046e4bd-c09a-4463-8bf8-09d07e6194cf" />|
| AWS Budget with Notifications | success |<img width="1431" height="595" alt="image" src="https://github.com/user-attachments/assets/762025d5-8f83-4adb-9432-eb73ebcf566d" />|

### AWS Config Rule Compliance

List the AWS Config rules you've implemented and their compliance status:

| Rule Name | Compliance Status | Non-Compliant Resources |
|-----------|-------------------|-------------------------|
|IAM Password Policy check |success |corrected |
|Root account MFA check |success | |
|IAM User MFA check |success | |
|CloudTrail enabled check |success | |
|S3 bucket public write protection check |success | |
| | | |
| | | |
| | | |

### Security Hub Standards

List the Security Hub security standards you've enabled and their current scores:

| Security Standard | Current Score | Critical/High Findings |
|-------------------|---------------|------------------------|
| AWS Foundational Security Best Practices | 44%|<img width="136" height="297" alt="image" src="https://github.com/user-attachments/assets/92f3557a-ef15-4dc4-b850-1a0bce7cff0c" /> |
| CIS AWS Foundations Benchmark |38% |<img width="138" height="297" alt="image" src="https://github.com/user-attachments/assets/8aca6bd0-9e49-4d3e-a392-2c736a5da095" />|
| PCI DSS |56% |<img width="139" height="290" alt="image" src="https://github.com/user-attachments/assets/729829b9-53d2-47da-8d26-72ef0ca704e7" />|

## Open-Ended Reflection Questions

Take time to reflect on the following questions. Your answers will demonstrate your understanding of cloud security concepts and help build your GRC portfolio.

### 1. Security Posture Evaluation

How would you characterize the overall security posture achieved by implementing these controls? What are the strongest elements and what gaps remain?

```
[Your answer here]
```

### 2. Alignment with Security Frameworks

How do the controls implemented in this lab align with industry security frameworks (such as NIST CSF, ISO 27001, or CIS Controls)? Identify specific domains or control families.

```
[Your answer here]
```

### 3. Business Risk Reduction

Identify 3-5 specific business risks that are mitigated by the security controls you've implemented. How would you explain the value of these controls to non-technical executives?

```
[Your answer here]
```

### 4. Advanced Security Architecture

If you were designing a more advanced security architecture for an enterprise, what additional services or features would you incorporate? Why?

```
[Your answer here]
```

### 5. Automation Opportunities

Which aspects of the security implementation could benefit most from automation? How would you approach automating these controls for a large-scale deployment?

```
[Your answer here]
```

### 6. Custom Approach to Challenges

Did you take any unique approaches to solving the challenges in this lab? What motivated your approach?

```
[Your answer here]
```

### 7. Cost-Security Tradeoffs

What tradeoffs between security and cost did you identify during this implementation? How would you optimize these tradeoffs in different contexts (e.g., startup vs. enterprise)?

```
[Your answer here]
```

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

1. 
2. 
3. 

## Personal Learning Outcomes

What are the most important insights or skills you gained from completing this lab?

```
[Your answer here]
```

## Additional Notes

Use this space for any additional thoughts, observations, or lessons learned:

```
[Your notes here]
``` 
