---
title: "CrowdStrike Incident - One Year Later"
slug: "crowdstrike-incident-one-year-later"
date: "2025-07-19T14:24:00"
author: "Matthew Burr"
summary: "On July 19, 2024 an incident occurred where approximately 8.5 million Windows computers were taken offline due to a bad definition file being deployed to the CrowdStrike Falcon product. Due to the way that the definition file was formatted, the way that Windows does not allow bad drivers to be bypassed at boot time, and the way that Windows handles Antivirus products in general all contributed to the outage. It has been a year since this incident and I wanted to go over what has changed, and if it is still possible for this issue to occur in the future."
tags: [
    "CrowdStrike",
    "Microsoft",
    "Windows"
]
categories: [ "Blog" ]
thumbnail: "/images/blog/00076/crowdstrike-logo.png"
toc: true
draft: false
---

On July 19, 2024 an incident occurred where approximately 8.5 million Windows computers were taken offline due to a bad definition file being deployed to the CrowdStrike Falcon product. Due to the way that the definition file was formatted, the way that Windows does not allow bad drivers to be bypassed at boot time, and the way that Windows handles Antivirus products in general all contributed to the outage. It has been a year since this incident and I wanted to go over what has changed, and if it is still possible for this issue to occur in the future.

## What Happened? ##

If you work in the IT field then I don't need to explain what happened as it was widely reported on at the time, but if you are not familiar here is basically what happened:

* CrowdStrike Falcon Sensor is a vulnerability scanner that is available for the Linux, macOS and Windows operating systems. This issue was only present on Windows, although it has been revealed that a similar issue happened with Linux systems earlier in 2024.
* CrowdStrike pushes updates to the software as required, with definition updates and signatures to identify zero-day attacks.
* The CrowdStrike Falcon software installs itself as a Windows kernel driver, which gives it visibility and access to the entire operating system.
* The kernel driver loads the files that are provided from CrowdStrike, which happens without any interaction from the user.
* The driver was configured as a **boot driver**, which means that the operating system will not start if there is an issue. This is important, as this caused the issue with Windows not being able to boot properly.
* On July 19, 2024, CrowdStrike pushed an update that was corrupt and invalid, and that caused the operating system to crash.
* Since the faulty update was present on the Windows device and the software was configured as a boot driver, the operating system was not able to start.

I also put together a [post](/blog/2024/07/23/crowdstrike-incident/) about the issue that I updated several times as more information was released about the issue.

## Has Anything Changed? ##

Microsoft has [committed](https://blogs.windows.com/windowsexperience/2025/06/26/the-windows-resiliency-initiative-building-resilience-for-a-future-ready-enterprise/) to making changes to the way that Windows and Antivirus products operate to avoid issues like the CrowdStrike incident from happening again. [CrowdStrike](https://www.crowdstrike.com/en-us/blog/reflecting-on-building-resilience-by-design/) has also made changes to the way that definition updates are deployed to prevent wide scale issues from occurring as well.

Currently, Antivirus products hook directly into the Windows kernel to operate correctly and do not typically operate in user space. This means that an issue with the Antivirus product can crash the system, and in CrowdStrike's case, prevent the system from starting correctly.

As part of the fix for this issue, Microsoft will be moving Antivirus products out of the kernel and into user space. This is happening through the [Microsoft Virus Initiative](https://learn.microsoft.com/en-us/unified-secops-platform/virus-initiative-criteria), and involves collaboration with multiple vendors to ensure that everything works correctly. This is still a work in progress, and will take some time to resolve.

## Can It Happen Again? ##

In the context of a botched software update causing downtime on a large scale? It will almost certainly happen again.

I learned very quickly in my IT career to never, ever promise that an issue will never occur again. Downtime can happen at any time, and it can be completely outside of your control. The only thing you can do is plan accordingly and ensure that the risk with every update is known.

Easier said than done.

## Links ##

* [CrowdStrike - One Year Later: Reflecting on Building Resilience by Design](https://www.crowdstrike.com/en-us/blog/reflecting-on-building-resilience-by-design/) ([Local Version](/docs/blog/00076/crowdstrike_one_year_later_reflecting_on_building_resilience_by_design.pdf))
* [Microsoft - The Windows Resiliency Initiative: Building resilience for a future-ready enterprise](https://blogs.windows.com/windowsexperience/2025/06/26/the-windows-resiliency-initiative-building-resilience-for-a-future-ready-enterprise/) ([Local Version](/docs/blog/00076/microsoft_the_windows_resiliency_initiative.pdf))
* [Microsoft Learn - Microsoft Virus Initiative](https://learn.microsoft.com/en-us/unified-secops-platform/virus-initiative-criteria) ([Local Version](/docs/blog/00076/microsoft_learn_microsoft_virus_initiative.pdf))
