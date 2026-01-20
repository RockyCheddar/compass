---
icon: gear
description: >-
  LMS administrator guide for connecting EdEHR to your learning management
  system using LTI.
---

# Setting Up EdEHR in Your LMS

## Setting Up EdEHR in Your LMS (Admin Guide)

This guide walks LMS administrators through connecting EdEHR to your LMS using LTI. The process is quick, but you’ll need to coordinate with your EdEHR admin for a couple of details.

***

### What is LTI and Why Use It?

LTI (Learning Tools Interoperability) lets EdEHR integrate directly into your LMS, so instructors and students can access EdEHR activities from within their courses, no extra logins needed.

***

### Prerequisites

Before you start, make sure you have:

* Access to your institution’s EdEHR instance.
* The API URL, consumer key, and shared secret from your EdEHR admin.\
  &#xNAN;_(If you don’t have these, reach out to EdEHR support—see below.)_

***

### Step-by-Step: External Tool Configuration in Moodle

<div align="left"><figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure></div>

The following steps are for Moodle, but most LMS platforms have a similar process.

1. **Log in** to your LMS as an administrator.
2. Navigate to **Site Administration** (bottom left of the home screen).
3. Select **Plugins** > **Activity Modules** > **External Tool**.
4. Click **Manage tools** under External Tool.

***

### Configure the Tool

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

Fill in the following fields:

* **Tool Name:** Choose a name your course designers will recognize (e.g., “EdEHR”).
* **Tool Description:** Briefly describe what this connection does.
* **Tool URL:** Enter the EdEHR API URL (ask your EdEHR admin if unsure; e.g.,\
  `https://edehr.org/api/launch_lti`)
* **Consumer Key & Shared Secret:** Obtain these from your EdEHR admin.
* **Default Launch Container:** Select “Existing window” or “New window.” _(Avoid the default “embedded” option.)_

Click **Save** when finished.

Let your course designers know the tool is ready and provide them with the name you used.

***

## Blackboard Ultra

### Adding EdEHR as an External Tool (LTI 1.1) in Blackboard Ultra

In Blackboard Ultra, an **LTI Placement** is what makes an external tool reusable by instructors. Once the placement is created, instructors will see _EdEHR_ listed in their **Content Market / Books & Tools**. They can then add it to any course without needing to configure keys or URLs themselves.

#### Step 1 – Admin Panel

1. Log in to Blackboard as an administrator.
2. Go to **Admin Panel → Integrations → LTI Tool Providers**.
3. Click **Register LTI 1.1 Tool Provider**.

#### Step 2 – Register the Tool Provider

1. **Tool Provider Domain**: enter `edehr.org`
   * Blackboard uses this destination domain to decide when to send the EdEHR key/secret along with a launch.
2. **Status**: set to **Approved**
   * _Status_ determines whether Blackboard will allow outgoing launches to this domain. If not approved, launches will be blocked or prompt for confirmation.
3. **Key** and **Secret**: use the values provided by EdEHR.
4. **User Fields to Send**: enable **Name** only (do **not** select email).
5. Save.

#### Step 3 – Create a Placement

1. After saving, click the EdEHR tool → **Manage Placements** → **Create Placement**.
2. Enter:
   * **Label**: _EdEHR_
   * **Handle**: _edehr_
   * **Tool Provider URL (Launch URL)**: `https://app.edehr.org/api/launch_lti`
3. **Placement Type**: select **Course content tool**.
4. **Launch in New Window**: set to **Yes** (EdEHR must open full-window, not inside a frame).
5. Save.

#### Step 4 – Instructor Use in Courses

1. Instructors go into an Ultra course and open **+ Add Content → Content Market** or **Books & Tools**.
2. They will see _EdEHR_ as an option.
3. Selecting it adds the tool link into the course content.

#### Step 5 – Verify

* Test as instructor and student:
  * The tool opens in a new browser window.
  * User name and course context are passed correctly.
  * No email addresses are sent.

***

### Need Help or Missing Information?

If you need the API URL, key, or secret—or if you have questions—please contact the EdEHR support team:

**Email:** [support@edehr.org](mailto:support@edehr.org)



***

Once the tool is set up, course designers can add EdEHR activities to their courses using the new external tool.
