---
title: "Why I Ditched Microsoft 365 (Part 1)"
date: "2025-05-15T21:56:00"
author: "Matthew Burr"
summary: "I have been stuck in a loop for a while using multiple services from different providers to get things done in my daily workflow. I have been looking for ways to consolidate and simplify those services as much as possible, as I am tired of dealing with multiple providers for everyday tasks. I have written about this several times on this website, and I have made a lot of efforts to reduce the number of services that I am using. Obviously, this is not a problem for a lot of people, and they have no issues switching back and forth between services, but I find it to be quite annoying and distracting. After going back and forth and tracking my usage, I decided that I no longer need Microsoft 365 at all, and it was time for it to go. The Microsoft 365 services that are offered can be provided elsewhere, and that was what I wanted to investigate."
tags: [
    "Copilot",
    "Microsoft",
    "Office 365"
]
categories: [ "Blog" ]
thumbnail: "/images/blog/00074/microsoft-365.png"
toc: true
draft: false
---

I have been stuck in a loop for a while using multiple services from different providers to get things done in my daily workflow. I have been looking for ways to consolidate and simplify those services as much as possible, as I am tired of dealing with multiple providers for everyday tasks. I have written about this several times on this website, and I have made a lot of efforts to reduce the number of services that I am using. Obviously, this is not a problem for a lot of people, and they have no issues switching back and forth between services, but I find it to be quite annoying and distracting. After going back and forth and tracking my usage, I decided that I no longer need Microsoft 365 at all, and it was time for it to go. The Microsoft 365 services that are offered can be provided elsewhere, and that was what I wanted to investigate.

I have been using Microsoft 365 (formerly Office 365) since 2011 in one way or another, for my personal accounts, my business accounts, and my work accounts. As much as people do not like to admit it, Microsoft 365 is the standard in the industry with at least 400 million users in 2024[^1], which represents tens of billions of dollars in revenue for Microsoft. For the purposes of this post, this entire issue is related to my personal and business usage of Microsoft 365, and this has no effect on anything that I do that is work related. I am fairly removed from that aspect in IT at this point in my career, as that is not really my focus anymore. This also does not apply to Azure, as that is also a completely different issue (which I will also deal with later). The Microsoft 365 ecosystem has become too complex for my liking, and I wanted to move to a simpler solution for basic services such as email.

[^1]: [Microsoft Cloud Revenues Powered by Office 365 - Office 365 for IT Pros](https://office365itpros.com/2024/01/31/office-365-reaches-400-million/#Office_365_Reaches_400_Million_Paid_Seats) ([Local Version](/docs/blog/00074/office_365_reaches_400_million_users.pdf))

I stopped using Microsoft 365 and moved to [iCloud+](https://icloud.com/) for several months for hosting email. I ended up using [Proton](https://proton.me/) for everything, and I am currently happy with the results. I wrote more about this in [the second part of this post](/blog/2025/05/15/why-i-ditched-microsoft-365-part-2/), as this post ended up being longer and more in-depth than I originally planned.

## Background ##

As I have mentioned many times before on this website over the last few years, I have been working for some time to consolidate a lot of my online services onto as few platforms as possible. There were several reasons for this:

1. Reduce the number of accounts that I need to use daily.
2. Reduce the attack surface of my accounts.
3. Reduce the complexity in maintaining those services.
4. Reduce the amount of time needed to move data between services.
5. Reduce the amount of "noise" in those services.
6. Reduce costs if possible.
7. Be platform agnostic and portable.

The last point is just a nice to have. I have never once had an issue in paying for services that I use, because if there is value in those services it is money well spent. If a paid service can simplify my workflow, then it is worthwhile to use, and I have no issue in paying for it. If that service also allows me to be more secure, then it is an easy decision to pay for it. If the service is free, then that is always a good thing. The only issue is that I would like to have a method to move away from that platform should an issue ever occur.

Another factor that I have been dealing with as well, is that I have practically migrated entirely from Windows to macOS over the last few years. This has started to become an issue with maintaining the services that I use with Microsoft, and the ones that I use with Apple. To further complicate this, I am also considering a move away from the Apple ecosystem, as some of the issues that I was having with Microsoft also apply to Apple.

It does not help that I do not use most of the services that are on Microsoft 365, so I feel like I am just wasting my money. I noticed that in early 2024 I was only ever using Microsoft 365 for email, and I rarely used Teams anymore as I strongly prefer to communicate and collaborate with people over email. I have found that a lot of the services that were provided outside of Office and Exchange were not especially useful and are just niche products that people feel forced to use. Microsoft also has a bad habit of retiring those services without much notice, or merging them together, so I just avoided them.

As time went on, I guess I just wanted more of a basic "groupware" solution that I didn't have to manage and would always work. Between 2006 and 2010 I used to manage a [Horde](https://www.horde.org/) instance for an old email domain that I used to own on some long-gone hosting provider. Even though that platform is effectively dead, I always liked how well it worked and how customizable it was. I might write something about this in the future, as I still have old configurations and documentation for it. I also am not interested in hosting such a solution myself, as I would prefer to focus my time and effort on other things.

Microsoft Office as a productivity suite has also become less important to me as I don't really use it much anymore. The only Office applications that I use daily is Excel and Visio. The functionality of Excel is easily replaced, and there are multiple options to choose from in 2025. I have tried many Visio alternatives over the years, but at the end of the day it works the best (I will die on that hill). Even though I use macOS as my daily driver, I have a virtual machine on my local Hyper-V server running Visio just so that I don't have any issues with it.

### Requirements ###

The requirements for replacing Microsoft 365 aren't even that complex, and there are multiple solutions that provides the base features for the communication aspects for it. This is for the Exchange Online features that a traditional Exchange server provides. Things like email, calendar and contacts are a given for basic support, but I required the ability to use custom domains without workarounds. I will always host DNS on other providers, and this shouldn't be an issue for modern providers.

PGP support has always been tricky in my experience. Some providers make it easier than others, and it usually always relies on a plugin or extension on the mail client to support it. The problem is usually with going from desktop to mobile apps, and the way that keys are managed. Having this as a built-in feature would be a bonus, as I deal with encrypted emails on an almost daily basis.

### Recent Events ###

I started this post a few months ago, knowing it would take some time to migrate between services and properly test them. I didn't want to rush through any testing, and I didn't want to use test accounts for anything. For personal projects I have no issue with going "all in" and testing things knowing that things may be broken. If things don't work out, I will try something different, and it is not really a big deal. I had no agenda or timeline, and I was open to anything if it worked for me. Something I never expected to happen was at the end of 2024, and that changed my attitude on the entire goal of this exercise.

I am a Canadian, and a lot of online services that I use are based in the US. The constant economic threats and threats to Canadian sovereignty has been quite off-putting, and as a result I am working to migrate all my essential services to other providers in other countries. As part of this exercise, I had been using iCloud Mail for several months in 2024 up until the beginning of 2025, but I moved away from this service a few months ago as a response to the issues with the US. I eventually settled on an EU-based email solution, which also allowed me to migrate other services as well. This also allowed me to migrate other services as well, as I made those migrations at the same time.

I will post more about this topic in the future, as it is a work in progress and there are many moving parts involved.

## Microsoft 365 ##

I have had a Microsoft account through [Outlook.com](https://outlook.com/) for a long time, which is linked to an old email address that I no longer use on a regular basis. I keep this account around for my Xbox Live account, and for testing a regular Microsoft account with newer versions of Windows. At one point this account was linked to an Office 365 subscription which I used simply to get a valid copy of Microsoft Office, and I believe I had the Outlook.com Premium subscription at one point so that I could use custom email domains. At this point, the email address is completely unused, and I login every few months just to clear the junk folder.

### Microsoft 365 Business Subscription ###

Back in 2016 when I was setting up my [IT consulting company](https://tenfifteen.ca/) I wanted to have it separate from my personal accounts. I have never liked any of the offerings from Google, and I was not interested in setting up my own solution for email and other online services. Since Exchange is the de facto industry standard for corporate email, I ended up using Office 365 with my own tenant using a separate domain. I went back and forth for a while trying different licensing options, and eventually I settled on a license for [Microsoft 365 Business Premium](https://www.microsoft.com/en-ca/microsoft-365/business/compare-all-microsoft-365-business-products). It seemed like it was a good balance between the features that I needed to use, and it wasn't overly expensive when it was paid for annually.

As of this writing there are four versions of Microsoft 365 Business which all offer slightly different base features and pricing:

| License              | Cost[^2]   | Exchange | OneDrive | SharePoint | Teams | Office Apps  |
|:---------------------|:-----------|:---------|:---------|:-----------|:------|:-------------|
| Business Basic       | $8.10      | Y        | Y        | Y          | Y     | Y (Web Only) |
| Business Standard    | $17.00     | Y        | Y        | Y          | Y     | Y            |
| **Business Premium** | **$29.80** | **Y**    | **Y**    | **Y**      | **Y** | **Y**        |
| Apps for Business    | $11.70     | N        | Y        | N          | N     | Y            |

[^2]: Microsoft 365 Business subscription prices per month (without taxes), in CAD as of May 2025. These costs are for annual subscriptions only, and monthly subscriptions are 20% higher in costs.

The Microsoft 365 Business Premium license includes the following features:

* Office (Excel, OneNote, Outlook, PowerPoint, Word)
* Teams (with Audio Conferencing)
* OneDrive (with 1 TB of storage per user)
* SharePoint
* Exchange Online
* Intune
* Microsoft Purview
* Defender
* Entra ID

Some of the other applications that are included are:

* Bookings
* Clipchamp
* Forms
* Lists
* Loop
* Planner
* Search
* Sway
* To Do
* Viva
* Whiteboard

For my purposes, most of the included base features are quite useful. Having the full Office suite with OneDrive was very convenient at the time, and the Office applications included the desktop, online and mobile versions. It also included Visio Online, which was useful for viewing diagrams on the web, but I have always had a full version of Visio for getting actual work done. Also included was licensing for Windows 10 Business, which was automatically activated when I logged into a Windows 10 workstation with the associated account. As I have reduced my dependence on Windows for my personal usage, this has become less important.

The other web applications were not particularly helpful or useful and were included to "beef up" the overall Office 365 offering. Having a bunch of proprietary products that were difficult to use outside of the Office 365 ecosystem was always a hard sell for me. Microsoft also has a poor record of retiring services or merging them without much notice. I always found that those products were solutions in search of a problem, and they were usually redundant in nature.

The Audio Conferencing options that Microsoft 365 offered were useful, and for a time I did have a few DID numbers associated with my Teams account using the [Microsoft Teams Phone](https://www.microsoft.com/en-ca/microsoft-teams/microsoft-teams-phone/) service. It worked well, despite the lack of SMS options. I was able to setup a cloud PBX to handle calls, which was a nice feature that I ultimately didn't get much usage out of.

### Microsoft 365 Applications and Services ###

I started by looking at the Microsoft services and applications that I was using with Microsoft 365, and determining if I really needed it:

* **Microsoft Office** - I don't use it as often as I used to, and when I do it is only for Excel. I never really liked using the web versions of Office, and I have never been compelled to use the mobile versions. I do the most of my document generation with [LaTeX](/blog/2020/01/23/visual-studio-code-with-latex/) and I rarely use Word. I will talk more about what I ended up doing about Office at the end of this post.
* **Microsoft OneDrive** - I don't have any use for OneDrive since I have migrated to iCloud and other cloud storage platforms. I have never liked that the macOS client had extremely poor performance and was essentially useless.
* **Microsoft Outlook** - I have no real attachment to the Outlook client, and it is just a mail client for me. Outlook is in a weird transition period at the moment as Microsoft is actively trying to move to a "modern" version that is completely different from the legacy Outlook and removes a considerable amount of functionality. I have no issues with any mail client, whether it be Microsoft Outlook, Mozilla Thunderbird, macOS Mail or any webmail services. If I can back up my email without too much hassle that is a bonus, but that is not a hard requirement.
* **Microsoft SharePoint** - I tried using SharePoint for a few things, but it was overkill for my needs.

For the Exchange components of Office 365, this wasn't really a big issue. At the end of the day, it is just an email service, and there are countless methods for replacing it. The only requirement was that I needed to be able to import by existing email into the new provider, which is never a difficult task to do.

### Microsoft 365 Copilot ###

I originally didn't care about this product and its influence at all, but it is driving a lot of the decision making at Microsoft. I am tired of Copilot, and I have no interest whatsoever in it. I want to have absolutely nothing to do with Copilot. It has nothing to do with my daily workflow.

This may seem like an extreme stance to take considering the "perceived importance" of generative AI, but I particularly do not like Copilot for several reasons:

* I am tired of seeing Copilot in in Windows.
* I am tired of seeing Copilot in in Edge.
* I am tired of seeing Copilot in Microsoft 365.
* I do not find Copilot to be useful at all.

I am also not thrilled that Copilot has found its way into GitHub and VS Code. My attitude towards generative AI is not specific to Copilot, it applies to all the other tools. I also find the idea of a Copilot+ PC and Recall ridiculous, but that is a topic for another day.

### Other Microsoft Services ###

Aside from the offerings from a paid Microsoft 365 subscription, there were also a few other Microsoft applications and services that I occasionally used:

* **Microsoft Authenticator** - I have never liked this authenticator app. I always found it slow to use, it didn't have a search feature for the longest time, and the backup feature was questionable at best. I also don't like that the app only worked on my phone and offered no web interface, or the ability to use it on a computer. There are many alternatives to this app, and for a time I was using the Passwords app on iOS and macOS.
* **Microsoft OneNote** - Oddly enough I have never actually been a fan of this application, and I only had a few notes that I have migrated to other tools. I wanted to like OneNote since it was first introduced, but I don’t like to rely on a third-party tool to look through my notes. I prefer Markdown for storing notes, as they are plaintext, portable and have no overhead.

I am still using Azure for a few things, but those services are not really needed anymore. I am looking to migrate those services to another provider, migrate them to a local device, or just retire those services entirely. As mentioned earlier, I still have an Xbox Live account that I use on a regular basis, so I will keep my legacy Microsoft account strictly for that purpose.

#### GitHub ####

This is only relevant since Microsoft owns [GitHub](https://github.com/), but I use GitHub for hosting all my Git repositories. I have two accounts, one of which is for all my private repos and the other for my public repos. I use my public account for hosting all my [external websites through Netlify](/blog/2021/12/23/goodbye-wordpress-hello-hugo/). I have a GitHub Pro subscription for my main account, and I do not find it to be particularly useful anymore. I am actively looking to migrate this to another service, and I am also considering hosting it myself with [GitLab](https://gitlab.com/). The main reason is Copilot and storage location on my data, which I can only assume is in the US. I am not concerned about my other account at this time as it is already hosting public data that is already openly available (this website is hosted there). That is something that I will deal with later.

#### VS Code ####

I use VS Code as my primary IDE for everything. I use this application every day at work, and I use it at home for most of my personal projects. As much as I like VS Code, I will stop using it if Copilot makes its way into it. Currently there are extensions for Copilot, and they are entirely optional, but I will not tolerate that feature being there by default. There are countless alternatives for this application, and I am happy to use any of those alternatives should it ever become an issue.

## Next Steps ##

I decided to trial using iCloud+ services to replace the base functionality of Microsoft 365, with varying levels of success. I tried that solution for several months and I am currently using Proton for those services. I also had to migrate my telephony services to another provider, as I did not want to leave those services with Microsoft 365.

Read more about this in the [the second part of this post](/blog/2025/05/15/why-i-ditched-microsoft-365-part-2/).

## Links ##

* [GitHub](https://github.com/)
* [GitLab](https://gitlab.com/)
* [Goodbye WordPress, Hello Hugo](/blog/2021/12/23/goodbye-wordpress-hello-hugo/)
* [Horde](https://www.horde.org/)
* [iCloud](https://icloud.com/)
* [Microsoft 365 Business Premium Overview](https://learn.microsoft.com/en-us/microsoft-365/business-premium/m365bp-overview?view=o365-worldwide)   ([Local Version](/docs/blog/00074/microsoft-365-business-premium-overview.pdf))
* [Microsoft 365 Business Products](https://www.microsoft.com/en-ca/microsoft-365/business/compare-all-microsoft-365-business-products)             ([Local Version](/docs/blog/00074/microsoft-365-business-product-overview.pdf))
* [Microsoft Teams Phone](https://www.microsoft.com/en-ca/microsoft-teams/microsoft-teams-phone/)
* [Proton](https://proton.me/)
* [Ten Fifteen Solutions](https://tenfifteen.ca/)
* [Visual Studio Code with LaTeX](/blog/2020/01/23/visual-studio-code-with-latex/)
