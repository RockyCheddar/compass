---
icon: fingerprint
---

# Privacy Regulations & Compliance

### Privacy Regulation & Compliance

#### Overview

EdEHR operates in alignment with **British Columbia's Freedom of Information and Protection of Privacy Act (FOIPPA)**. As a cloud-based educational tool simulating an electronic health record (EHR), it collects limited student and instructor data, ensuring all practices meet privacy requirements for public educational institutions.

#### Why a Privacy Impact Assessment (PIA)?

A PIA is required under Section 69(5.3) of FOIPPA. It ensures:

* Compliance with privacy law.
* Transparency around data collection and use.
* Risk mitigation strategies are in place.
* Institutional privacy officers and the Office of the Information and Privacy Commissioner (OIPC) are consulted when needed.

Even if no personal information is collected, PSI must still complete **Part 1 of the PIA** to confirm and document that assessment.



### What Data Is Collected?

EdEHR collects minimal personal data necessary for its function:

* **Student**: Name, LMS role, LMS user ID, submitted assignments.
* **Instructor**: Name, LMS role, LMS user ID, comments on student work.

No email addresses, dates of birth, or other personally identifiable information (PII) are stored.

***

### Data Storage & Transmission

* **Storage Location**: Toronto, Canada (DigitalOcean servers).
* **In Transit**: All communications are encrypted via HTTPS (SHA-256 with RSA).
* **At Rest**: All data is encrypted on the server.

***

### Security Measures

* **Access Control**: Only accessible through institutional LMS integration (no separate EdEHR login).
* **Admin Access**: Limited to one or two vetted individuals via SSH using SSL keys—no password-based access.
* **Firewalls**: Dual firewall protection (DigitalOcean + Debian OS).
* **Infrastructure Transparency**: EdEHR is an open-source platform. Code is publicly available via GitHub.

> 🔗 [EdEHR GitHub Repository](https://github.com/edehr/edehr)

***

### Key FOIPPA Justifications for Data Collection

* **Section 26(c)** – Collection authorized when necessary for operational programs.
* **Section 33.2(a)** – Permits use by instructors for assessment and feedback.

***

### Data Lifecycle & Retention

* Student assignments may be deleted after a course ends at the institution’s discretion.
* Schools are expected to download and retain records as they see fit.
* EdEHR updates user data from the LMS on each interaction—ensuring accuracy.

***

### ❗ Risk Mitigation Summary

<table><thead><tr><th width="177.01171875">Risk</th><th width="297.140625">Mitigation</th><th width="138.5625">Likelihood</th><th>Impact</th></tr></thead><tbody><tr><td>Data breach</td><td>Minimal data collected, encrypted in transit and at rest</td><td>Low</td><td>Low</td></tr><tr><td>Server compromise</td><td>Dual firewall + restricted SSH access</td><td>Low</td><td>Low</td></tr><tr><td>Unauthorized admin access</td><td>LMS authentication + unique, non-stored high-entropy passwords</td><td>Low</td><td>Medium</td></tr></tbody></table>

***

### Student Privacy Notice (Sample)

Students must be informed upon enrolment in LMS-integrated courses using EdEHR:

* Data is stored in Canada and only minimally collected.
* EdEHR is a third-party learning tool and not managed by the institution’s servers.
* No direct contact from EdEHR.
* The tool supports the development of nursing informatics competencies.

***

### Common or Integrated Programs & Data-Linking

EdEHR **does not qualify** as a “common or integrated program” or a “data-linking initiative” under FOIPPA because:

* It doesn’t involve new purposes for existing data.
* It is not shared across multiple public bodies.
* It is institutionally contained.

***

### Next Steps for New PSIs

1. Review and understand FOIPPA compliance expectations.
2. Complete Part 1 (and others if personal info is involved) of the PIA form.
3. Confirm with your institutional privacy officer whether full or partial PIA is required.
4. Use the sample collection notice for all student-facing communications.
5. Refer to your LMS admin for internal data security policies.
6. For changes to EdEHR usage or integration, initiate a **PIA Update**.
