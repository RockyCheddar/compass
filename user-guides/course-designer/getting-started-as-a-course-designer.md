---
icon: flag-checkered
description: >-
  Getting started with course designer mode, including role switching and
  available features.
---

# Getting Started as a course designer

Getting started as a course designer in EdEHR means unlocking a new set of creative and technical tools. This page will walk you through the basics of switching roles, enabling Course Designer Mode, and understanding the additional features available for building and managing your own learning content. Whether you’re new to EdEHR or just need a refresher, you’ll find the essentials here to get up and running smoothly.

What You’ll Learn

* [The difference between Instructor and Course Designer roles](getting-started-as-a-course-designer.md#instructor-vs.-course-designer-content-creator-roles)
* [How to enable Course Designer Mode](getting-started-as-a-course-designer.md#step-1-enable-course-designer-mode)
* [What you can do as a Course Designer](getting-started-as-a-course-designer.md#what-you-can-do-as-a-course-designer)
  * [Navigating the Account Page](getting-started-as-a-course-designer.md#account-page)
  * [Course Designer options for managing Case Studies ](getting-started-as-a-course-designer.md#once-in-course-designer-mode-you'll-have-additional-permissions-to-create-and-manage-learning-objects)
  * [Course Designer options for managing Learning Objects](getting-started-as-a-course-designer.md#course-designer-options-will-see-the-following-menu-items-for-learning-objectives)

***

## Instructor vs. Course Designer (Content Creator) Roles

When you first access EdEHR as an instructor, you have permissions to:

* Manage class lists
* View learning objects and case studies
* Access student submissions



{% hint style="warning" %}
**Warning:** Edits made in Course Designer Mode go live immediately and affect all activities or courses that use the case. Before editing a base case or learning object, double-check that you're working on the right version and coordinate with your team if others are using the same content.
{% endhint %}



***

## Promote to Course Designer Role

To create and manage content, you must self-promote to "**Course Designer**" role.&#x20;

To promote yourself from Instructor to Course Designer, follow these steps:

### Enable Course Designer Mode

{% stepper %}
{% step %}
#### By default, you will be in Instructor View. Once inside edEHR, look for the menu on the left side of the screen. Find and check the box labeled “**Course Designer Mode**.”

<div align="left"><figure><img src="../.gitbook/assets/Creating Learning Objects in EHR System - Step 2.png" alt=""><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
#### Course Designer Mode Enabled

You should now see additional editing options and features for creating and managing content.

If you don’t see the option to enable Course Designer Mode, contact your EdEHR administrator for access.

{% hint style="warning" %}
**Warning:** Enabling Course Designer Mode is the essential first step for any walkthrough or task in the Course Designer Guide. Before proceeding, make sure this mode is selected and active otherwise, you won’t have access to the tools and options described in the following sections.
{% endhint %}
{% endstep %}
{% endstepper %}

***

## What You Can Do as a Course Designer

Once you’ve enabled Course Designer Mode, you’ll unlock a full suite of tools and options for building and managing your own content. The next sections will walk you through everything you can do as a Course Designer, from editing case studies and learning objects to customizing activities for your course.

* [Account Page](getting-started-as-a-course-designer.md#account-page)
  * [LMS](getting-started-as-a-course-designer.md#lms)
  * [Active Counts](getting-started-as-a-course-designer.md#the-active-counts)
  * [Constants](getting-started-as-a-course-designer.md#constants)
  * [Medications](getting-started-as-a-course-designer.md#medications)
  * [Feature Flags](getting-started-as-a-course-designer.md#feature-flags)
  * [Statistics](getting-started-as-a-course-designer.md#statistics)
* [Case Studies](getting-started-as-a-course-designer.md#case-studies)
* [Learning Objects](getting-started-as-a-course-designer.md#learning-objects)

***

### Account Page

With Course Designer Mode enabled, you’ll now notice a new page in your navigation called "Account." This page gives you access to several important tools and data points, including LMS integration details, the current active user count (which is used for billing), Constants, Medication Libraries, Feature Flags, and key Statistics. Below, I’ll give you a quick overview of what each of these sections offers.

<figure><img src="../.gitbook/assets/Screenshot 2025-07-07 at 11.48.43 AM.png" alt=""><figcaption></figcaption></figure>



#### LMS

The LMS section displays all the essential details you need for integrating EdEHR with your institution’s learning management system. Here you’ll find connection settings, integration keys, and other technical information that make syncing courses and user data seamless.&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2025-07-07 at 11.52.01 AM.png" alt=""><figcaption></figcaption></figure>

#### The Active Counts

The Active Counts section shows the number of users currently active in EdEHR, including monthly active students. This information is important for tracking usage and is used for billing purposes, so you can easily see how many learners are being counted each month.

<figure><img src="../.gitbook/assets/Screenshot 2025-07-07 at 11.58.18 AM.png" alt=""><figcaption></figcaption></figure>

#### Constants&#x20;

The constants listed here allow you to fine-tune key aspects of EdEHR’s simulation settings:

* **wbcFieldFactor**: Sets the default white blood cell (WBC) field factor for hematology peripheral blood film (PBF) reports. Adjusting this value impacts how WBC counts are calculated in lab simulations.
* **pltFieldFactor**: Sets the default platelet (PLT) field factor for hematology PBF reports. This controls how platelet counts are reported in simulated lab results.
* **tubeSuction**: Establishes the default suction setting for chest tube profiles, shown here as 20 cm H2O. This is the standard value used when simulating chest tube management scenarios.

Before saving any changes, you’ll need to acknowledge that all modifications are logged for tracking purposes.

<figure><img src="../.gitbook/assets/Screenshot 2025-07-07 at 11.52.38 AM.png" alt=""><figcaption></figcaption></figure>

#### Medications

This section allows you to change the medication database for all users in your EdEHR instance. Any updates you make here will instantly apply across every course and scenario, so use this feature when you need to standardize or update medication options program-wide.

<figure><img src="../.gitbook/assets/Screenshot 2025-07-07 at 11.53.28 AM.png" alt=""><figcaption></figcaption></figure>

#### Feature Flags

The Feature Flags section lets you see which new or experimental features are available but not yet turned on by default. Each feature listed here is hidden behind an opt-in flag, so you can choose which ones to enable for your EdEHR environment. To activate a feature, simply select "Enable" next to the option you want to try.

<figure><img src="../.gitbook/assets/Screenshot 2025-07-07 at 11.54.12 AM.png" alt=""><figcaption></figcaption></figure>

#### Statistics&#x20;

The Statistics section gives you a quick snapshot of your EdEHR environment’s activity and usage. Here you’ll find data like total visit counts, the number of learning objects and case studies, active user counts, and other key metrics. This overview helps you track engagement, monitor growth, and spot trends across your program at a glance.

<figure><img src="../.gitbook/assets/Screenshot 2025-07-07 at 11.54.31 AM.png" alt=""><figcaption></figcaption></figure>

***

### Case Studies

Once in Course Designer mode, you'll have additional permissions to create and manage Learning Objects and Case Studies.

<figure><img src="../.gitbook/assets/Accessing Case Studies in EHR Course Designer - Step 17.png" alt=""><figcaption></figcaption></figure>

Course Designer Options will see the following menu items for Case Study

* <img src="../.gitbook/assets/Eye Case Study Icon.png" alt="" data-size="line"> **Go to Learning Object**
* <img src="../.gitbook/assets/Edit Case Study icon.png" alt="" data-size="line"> **Go to Selected Case Study**
* <img src="../.gitbook/assets/Settings.png" alt="" data-size="line"> **Edit the Properties of the Case Study**
* <img src="../.gitbook/assets/Download Icon.png" alt="" data-size="line">  **Download**
* <img src="../.gitbook/assets/duplicate icon.png" alt="" data-size="line"> **Duplicate the Case Study**
* <img src="../.gitbook/assets/Learning Objectives.png" alt="" data-size="line"> **Create a Learning Object for this case**
* <img src="../.gitbook/assets/trash bin icon.png" alt="" data-size="line"> **Delete the Case Study**



For more details on working with case studies, check out the dedicated guide: [Working with Case Studies.](working-with-case-studies/)

***

### Learning Objects

Course Designer Options will see the following menu items for Learning Objectives

<div align="left"><figure><img src="../.gitbook/assets/Accessing EHR Learning Object Details - Step 1.png" alt=""><figcaption></figcaption></figure></div>

* <img src="../.gitbook/assets/Learning Objectives.png" alt="" data-size="line">  **Go to Assessment & Documentation with EdEHR**
* <img src="../.gitbook/assets/Case Studies.png" alt="" data-size="line">  **Edit the Properties of the Learning Objective**&#x20;
* <img src="../.gitbook/assets/Settings.png" alt="" data-size="line">  **Edit the Properties of the Learning Objective**
* <img src="../.gitbook/assets/duplicate icon.png" alt="" data-size="line">  **Duplicate the Learning Objective**
* <img src="../.gitbook/assets/Download Icon.png" alt="" data-size="line">  **Download Learning Objective**
* <img src="../.gitbook/assets/trash bin icon.png" alt="" data-size="line">  **Delete the Learning Objective**



To dive deeper into managing learning objectives, see the full guide: [Working with Learning Objectives.](working-with-learning-objectives/)

***

Now that you’re up to speed on all the extra tools and powers you get as a Course Designer, you’re ready to dive in and [create your first activity](creating-your-first-edehr-activity.md).&#x20;

