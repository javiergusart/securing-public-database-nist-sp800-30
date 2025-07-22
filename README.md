# Securing a Public Database Using NIST SP 800-30

## Table of Contents
1. [Overview](#overview)
2. [System Description and Scope](#system-description-and-scope)
3. [Purpose](#purpose)
4. [Risk Assessment](#risk-assessment)
   - [Risk Assessment Table](#risk-assessment-table)
5. [Approach](#approach)
6. [Remediation Strategy](#remediation-strategy)
7. [Conclusion](#conclusion)
8. [References](#references)

---

## Overview

This portfolio project was completed as part of the Google Cybersecurity Professional Certificate. It demonstrates practical risk analysis using NIST SP 800-30 Rev. 1 to secure a public database server in an e-commerce scenario, with actionable security recommendations.


The project documents the process of identifying and mitigating risks associated with a publicly accessible database server for an e-commerce company. The assessment follows the NIST SP 800-30 Rev. 1 risk management framework and demonstrates how to communicate technical risks and actionable recommendations to business stakeholders.

---

## System Description and Scope

- **System Description:**

The company’s remote database server is a critical asset, running on a modern Linux OS with MySQL, 128GB RAM, and SSL/TLS encryption. Employees worldwide access the server to query customer and business data. The server has been open to the public since launch, allowing unrestricted access from any location.

- **Scope:**
  
This assessment focuses on the confidentiality, integrity, and availability of the data on the database server. Physical security and other IT systems are out of scope.

---

## Purpose

The database server stores sensitive business and customer information essential for daily operations and strategic decision-making. Securing this data is vital to maintain customer trust, comply with regulations, and protect the company’s reputation. If the server were compromised or disabled, it could disrupt business operations, result in data breaches, and cause significant financial and reputational harm. This analysis aims to identify and communicate the risks associated with the current server configuration and recommend effective security controls.

---

## Risk Assessment

### Risk Assessment Table

| Threat Source         | Threat Event                                 | Likelihood | Severity | Risk (L × S) |
|----------------------|----------------------------------------------|:----------:|:--------:|:------------:|
| Competitor           | Obtain sensitive information via exfiltration |     3      |    3     |      9       |
| Outsider (Hacker)    | Conduct Denial of Service (DoS) attack        |     2      |    3     |      6       |
| Privileged User      | Alter or delete critical information          |     2      |    2     |      4       |

**Legend:**  
- Likelihood: 1 (Low), 2 (Moderate), 3 (High)  
- Severity: 1 (Low), 2 (Moderate), 3 (High)  
- Risk: Likelihood × Severity (Range: 1–9)

---

## Approach

The risks identified were selected based on the server’s public exposure, the types of users with access, and the business impact of potential incidents. A competitor could target the server to steal valuable data, which is a high-likelihood, high-severity risk due to the server’s open configuration. Hackers may attempt Denial of Service attacks, which could disrupt business operations and customer access. Privileged users, if compromised or acting maliciously, could alter or delete critical data, impacting business continuity. The likelihood and severity scores were determined using NIST SP 800-30 Rev. 1 guidance, expert judgment, and the system’s operational context.

---

## Remediation Strategy

To mitigate these risks, the following security controls are recommended:

- **Restrict Public Access:** Limit database access to authorized users and trusted networks using firewalls and network access controls.
- **Principle of Least Privilege:** Ensure users have only the minimum permissions necessary to perform their roles.
- **Multi-Factor Authentication (MFA):** Require MFA for all remote and privileged access to the server.
- **Regular Monitoring and Auditing:** Implement logging and real-time monitoring to detect unauthorized access or suspicious activity.
- **Data Encryption:** Encrypt sensitive data at rest and in transit to protect against exfiltration.
- **Incident Response Plan:** Develop and test a response plan for potential breaches or service disruptions.

Implementing these controls will significantly reduce the likelihood and impact of the identified risks, improving the overall security posture of the company’s information system.

---

## Conclusion

This project demonstrates how to apply the NIST SP 800-30 Rev. 1 framework to identify and mitigate risks associated with a publicly accessible database server. By systematically assessing threats, evaluating their likelihood and impact, and recommending targeted security controls, organizations can protect sensitive data, ensure business continuity, and maintain stakeholder trust.

---

## References

- [NIST SP 800-30 Rev. 1: Guide for Conducting Risk Assessments](https://csrc.nist.gov/publications/detail/sp/800-30/rev-1/final)
