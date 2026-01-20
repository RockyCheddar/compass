---
icon: compass-drafting
description: >-
  This guide provides step-by-step instructions for course designers using the
  edEHR system. It focuses specifically on how to navigate and use the software
  for creating and managing learning content.
---

# Course Designer Guide

### Understanding the Course Designer Role

Course designers in the EdEHR system are responsible for creating and managing educational content, including case studies and learning objects.

They develop assignments using simulated Electronic Health Records (EHR) or simulated Lab Information System (LIS) and connect these to their curriculum through their Learning Management System (LMS).&#x20;

This guide assumes you have access to an EdEHR instance and basic familiarity with your institution’s LMS. For assistance, support@edehr.org.

***

### Prerequisites

Before you begin creating content in EdEHR, ensure that:

* Your LMS administrator has created the external connection tool for EdEHR
* You understand how to use this external connection tool in your LMS
* You’ve reviewed the documentation for Student guides, Instructor guides, navigation tools, and Electronic health records basics

***

### Content Structure in EdEHR

Understanding the relationship between different content elements is crucial:

* **Activities**: Created in your LMS and links to a EdEHR Activity.  This holds the class list and instructor feedback.  The Activity can, optionally, enable and control SimTiming©
* **Learning Objects**: A EdEHR Activity is connected to a Learning Object which provides the lesson plan, objectives and case study data and can be reused across courses or semesters.  The Learning Object also defines the SimTiming© stages.
* **Case Studies**: Contain the EHR/LIS simulation data for virtual patients.

***

This hierarchical relationship flows as:

1. LMS Activity → links to → EdEHR Activity
2. EdEHR Activity → uses → one Learning Object
3. Learning Object → contains → learning objectives and uses one Case Study
4. Case Study → provides → simulated patient EHR/LIS data
