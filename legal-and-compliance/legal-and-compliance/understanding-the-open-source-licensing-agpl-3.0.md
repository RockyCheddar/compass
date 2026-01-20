---
icon: file-signature
---

# Understanding the open source licensing (AGPL-3.0)

## GNU Affero General Public License v3.0 (AGPL-3.0)

### Overview

The **GNU Affero General Public License v3.0 (AGPL-3.0)** is a copyleft open-source license designed to ensure that users who interact with the software over a network can access its source code. It is an extension of the GNU General Public License (GPL-3.0) but includes additional provisions to cover software that is run as a service.

This license is particularly relevant for cloud-hosted and web-based applications, ensuring that modifications to the software remain open and available to the community.



### Key Terms and Conditions

* **Copyleft License**: Any modified versions of the software must be distributed under the same AGPL-3.0 license.
* **Network Use Disclosure**: If the software is modified and made available over a network (e.g., as a web service or SaaS platform), the modified source code must be provided to users upon request.
* **No Proprietary Forks**: Organizations cannot take the software, modify it, and keep those modifications private if they provide it as a service.
* **Compatibility with Other Licenses**: The AGPL-3.0 is compatible with the GPL-3.0 but not with non-copyleft licenses.

### Implications for Use

#### **1. Deployment and Usage**

* Post-secondary institutions can freely deploy and use the software without paying for a license.
* If hosting the software internally without external access, there are no additional obligations beyond the standard GPL-3.0 terms.
* If the software is modified and provided as a service (e.g., a student-facing application), the source code of those modifications must be made available.

#### **2. Intellectual Property (IP) Considerations**

* Institutions **do not own** exclusive rights to any modifications they make to the software.
* Any customizations or improvements made to the software must be shared under the same license, meaning they **cannot be commercialized as proprietary software**.
* Institutions can, however, charge for hosting, support, and implementation services around the software.

#### **3. Compliance Requirements**

* If modifications are made, the institution must make the **full modified source code** available upon request.
* It is recommended to maintain a **repository of changes** (e.g., GitHub, GitLab) to track modifications and ensure compliance.
* Any external vendor or IT team providing services must also comply with AGPL-3.0, meaning they cannot develop and keep changes private.

### **Relation to Open Source Standards**

The **AGPL-3.0 license** aligns with the [**Open Source Definition (OSD)**](https://opensource.org/osd), as defined by the Open Source Initiative (OSI). This ensures:

* **Freedom to use, modify, and distribute** the software.
* **No discrimination against any user group, institution, or purpose**.
* **Source code availability and transparency** are enforced.

Below is a breakdown of how **AGPL-3.0** adheres to **OSD principles**:

| **OSD Principle**                                   | **How AGPL-3.0 Complies**                                                                               |
| --------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| **1. Free Redistribution**                          | AGPL-3.0 allows unlimited redistribution of the software.                                               |
| **2. Source Code Availability**                     | AGPL-3.0 requires that the source code is always made available.                                        |
| **3. Derived Works Allowed**                        | Institutions can modify the software and distribute their versions, provided they use the same license. |
| **4. Integrity of the Author’s Source Code**        | Modifications must be marked as such, but original licenses cannot be altered.                          |
| **5. No Discrimination Against Persons or Groups**  | Anyone can use and modify the software, including post-secondary institutions.                          |
| **6. No Discrimination Against Fields of Endeavor** | The software can be used for educational, commercial, or research purposes without restrictions.        |
| **7. Distribution of License**                      | The rights attached to the software apply to all users without additional conditions.                   |
| **8. License Must Not Be Specific to a Product**    | AGPL-3.0 is not tied to any specific software product.                                                  |
| **9. License Must Not Restrict Other Software**     | AGPL-3.0 does not impose restrictions on other software that is used alongside it.                      |
| **10. License Must Be Technology-Neutral**          | The license applies regardless of platform, programming language, or technology stack.                  |

By following AGPL-3.0, institutions can be confident that the software remains **fully open-source, compliant with OSD, and free from licensing ambiguity**.



### Frequently Asked Questions

<details>

<summary>Can institutions modify the software for internal use only?</summary>

Yes, institutions can modify the software for internal use without any obligation to share the modifications, as long as the software is not made accessible to users outside the institution.

</details>

<details>

<summary>What happens if the institution provides the software as a hosted service?</summary>

If students, faculty, or external users interact with the software over a network, then the institution is legally required to provide the modified source code.

</details>

<details>

<summary>Can institutions sell services around the software?</summary>

Yes, institutions can charge for:

* **Hosting the software** (e.g., running a cloud-based instance for other institutions).
* **Support and training services**.
* **Implementation and customization consulting**.

However, they **cannot sell the software itself as proprietary**.

</details>

<details>

<summary>How can institutions ensure compliance?</summary>

* Always document and maintain a repository of any modifications.
* Make source code changes accessible via a public repository when required.
* Ensure that third-party vendors working with the software understand and adhere to the AGPL-3.0 terms.

</details>



### Additional Resources

* [Full AGPL-3.0 License Text](https://www.gnu.org/licenses/agpl-3.0.txt)
* [Full AGPL-3.0 License Text](https://www.gnu.org/licenses/agpl-3.0.en.html)
* Guide to open source Licensing&#x20;
* Best practices for AGPL-3.0 Compliance
