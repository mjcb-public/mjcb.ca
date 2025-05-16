---
title: "Why I Ditched Microsoft 365 (Part 2)"
date: "2025-05-15T21:57:00"
author: "Matthew Burr"
summary: "There were several tasks that needed to be completed to successfully migrate away from Microsoft 365. I decided that I would test different solutions and make changes as needed, but the move away from Microsoft 365 would be a one-way trip. I had no intention of going back to that platform, and I was going to make whatever solution I ended up with work for me. At the end of this migration, I was able to have a proper email and groupware solution that did everything I needed it to do, and it was on a non-US provider."
tags: [
	"EU Alternatives",
    "iCloud",
    "Office 365",
    "Proton"
]
categories: [ "Blog" ]
thumbnail: "/images/blog/00075/proton-ag.png"
toc: true
draft: false
---

There were several tasks that needed to be completed to successfully migrate away from Microsoft 365. I decided that I would test different solutions and make changes as needed, but the move away from Microsoft 365 would be a one-way trip. I had no intention of going back to that platform, and I was going to make whatever solution I ended up with work for me. At the end of this migration, I was able to have a proper email and groupware solution that did everything I needed it to do, and it was on a non-US provider.

This is a continuation of the [the first part of this post](/blog/2025/05/15/why-i-ditched-microsoft-365-part-1/).

There were several tasks that needed to be completed to consider the migration from Microsoft 365:

* Migrate Telephony Services
* Migrate Productivity Software
* Migrate Email Services
* Migrate Calendars and Contacts
* Migrate Cloud Storage

As of this writing, all of these tasks have been completed successfully, and everything is working as expected.

## Telephony Services ##

The first and easiest task was migrating my DID numbers and other telephony services to another provider. I have been using [VoIP.ms](https://voip.ms/) for several years for several different projects, and it is a Montreal-based VoIP company that offers a considerable amount of customization options. This was an easy task to perform, and porting my numbers from Microsoft 365 only took a few days. Once the numbers were ported, they were available immediately.

I won't go into the details of how the setup process works on the VoIP.ms platform, as I would be doing a disservice to the amount of configuration options that are available. Overall, the service works very well and has a lot of redundancies built-in, so it is very reliable.

## Microsoft Office Replacement ##

I went back and forth on this, but it was actually an easy issue to resolve. As stated in the last post, I rarely use anything except for Excel from the base Microsoft Office offerings. I have used the offerings from Apple (Pages, Numbers and Keynote). I have nothing to say except they are applications that exist. They are not good applications, and only offer basic functionality. Using them is actually frustrating because of the issues that they have.

I use Visio on a daily basis, as I am constantly working on documentation and creating network diagrams. I have a license for Visio 

I received a free copy of Office Home 2024, which is the offline version of Microsoft Office. I don't use it, but I do have a license for it. For that version, it is missing some features from the Microsoft 365 versions, and it doesn't include Copilot.

I am a big supporter of [LibreOffice](https://www.libreoffice.org/), and I find that it works extremely well. I have been using this platform on and off for over 15 years, back before it was forked from [OpenOffice.org](https://www.openoffice.org/) (which is effectively dead at this point). LibreOffice is one of the few applications that I keep copies of the installers for, and I have been doing this for a few years. Whenever there is major release of LibreOffice, I will download and keep copies of all available versions and architectures so that I always have a fully offline installer for an office suite.

With it being a locally installed application, I never run into situations where I need to lookup complex documents on a mobile device or on the web, so I have no issues with mobility with any application. Despite what people say, there is no replacement for Visio. If people disagree with me on this opinion I can respect that, but I have found that all other solutions are completely inadequate.

## iCloud+ ##

I wanted to try using the email features that are available in iCloud+ since I was already paying for Apple One Premier ($44.95 CAD per month). iCloud supports custom domain names, so I thought it would be worthwhile to test the email functionality since I technically already had the service available to me. I ended up using this for about 5 months, and while it "worked" for what it was supposed to do, it had too many minor issues which forced me to try something else. From a usability perspective, iCloud is actually quite simple and easy to use:

![The iCloud portal immediately after logging in. The Advanced Data Protection feature is enabled on my account, which is why no previews are shown.](/images/blog/00075/icloud-portal.png)

I will go over the details on what was required to migrate to iCloud Mail from Microsoft 365.

### iCloud Mail ###

I already had an iCloud email account which I have had for many years which was tied to my Apple Account, but I never really used it for anything. iCloud Mail supports custom email domains (5 domains total) with the appropriate subscription, and you can buy a domain directly through them (which uses Cloudflare as the registrar). All that is required are custom MX records and several other DNS records to support iCloud Mail. Overall, it is not difficult to setup and use.

I ended up adding three custom domains, which included my primary domains that I used for email as well as one alternative domain that I use for testing purposes. This was a very easy process and from the time I added the appropriate records to the time I was able to use those domains for email was only a few minutes. This is why it is important to lower the TTL on DNS records to only a few minutes when you know a migration is going to occur.

Importing my existing email from Microsoft 365 was actually a trivial process. I just added my iCloud account to my Outlook client and imported the email. iCloud Mail uses IMAP for managing email, so it was important to ensure that all folders are subscribed to when using a desktop email client. The same process worked for my calendars, as well as any contacts that I had in Microsoft 365. The process was simple, and it took about 24 hours for everything to sync up.

The Mail client on macOS, iOS and the iCloud webmail client worked well most of the time, but there were a lot of little issues that ruined the experience for me.

#### iCloud Mail Issues ####

Well, there were some issues with iCloud Mail:

* Junk mail controls were virtually non-existent and questionable at best. When email was marked as junk it would not always do anything with future messages that were also junk. Sometimes emails would be sent to me that just vanished, and doing some investigations showed that this was a common issue.
* PGP integration with Mail on macOS was fine with the appropriate plugins, but it was not able to be easily used on iOS. The webmail client had no support at all.
* Search is not very reliable and would often return no results when I knew that there were emails that fit the criteria.

I often use the webmail client when I am not at home, as I don't like to carry a personal computer with me as often as I used to, and I don't like to write long emails on my phone. I noticed that there were a lot of stability issues when I was using the webmail client, and I saw this error at least once a week for no reason:

![The iCloud Mail web client would crash randomly and throw this message.](/images/blog/00075/icloud-mail-error.png)

I would also run into issues when trying to modify contacts through the iCloud web interface:

![The ability to manage contacts from the web would never work correctly, and this was the error every time.](/images/blog/00075/icloud-contacts-error.png)

I ran into a weird issue where a certain email alias wasn't receiving any email, and it wasn't immediately obvious what was going on. It turns out that in 2017 I created an Apple ID for that particular address and completely forgot about it. I couldn't find it in my list of passwords, and I had to reset the password using a somewhat convoluted process with iCloud. It turns out that I set it up as a test account and forgot to delete it when I was finished, and it was blocking email to that address on my main account. Again, weird issue, glad it was an easy fix, but there was no obvious error message showing what was happening.

Similar to my issues with Copilot with Microsoft 365, I also refuse to deal with Apple Intelligence. I received some interesting summarizations of my emails, which was humourous, but would just introduce more "noise" into what I was working on.

### Apple Applications ###

iCloud includes Pages, Numbers and Keynote. This is the Word, Excel and PowerPoint equivalents that Apple offers, and it is available on macOS, iOS, iPadOS and through iCloud. This is part of the legacy iWork suite, but they are separate applications that are available on multiple platforms. They are not good applications as I stated above. I am certain there are people that disagree with that and actually like those applications, but I am not one of those people. There are multiple alternatives that are leaps and bound better than those applications.

A major change that has happened in the last few releases on iOS and macOS is the Passwords app. Prior to this there were password management features present, but it was buried in the Settings app on iOS and macOS. The latest versions of iOS and macOS now include proper password and authentication features which integrates directly into iCloud, using a dedicated app. The only downside is the lack of a web version of this app.

Private Relay is also an interesting feature. It seems to behave like a VPN solution that can hide network traffic, but there is no transparency on how it actually functions. It is also extremely limited on how it actually works, and has no portability with other operating systems. This was not something I was interested in, but it is worth mentioning.

iCloud Drive is nice feature if you are fully committed to the Apple ecosystem. It integrates very well with most Apple applications, and makes sharing files with iMessage quite trivial. Recent improvements with macOS made it easier to flag files and folders to always be available offline, which was a welcome change.

### iCloud Future ###

There is a big difference between the quality of offerings between iCloud and Microsoft 365. This is not an issue with Apple and what they offer, it is simply a difference between platforms and what is offered between personal and enterprise solutions. I am sure there are people that will disagree with that comparison, but it is simply the way that it is. I decided to try iCloud+ features because I was already paying for it, so I had nothing to lose.

I decided that I would prefer to utilize other solutions that have more portability, and are not tied to a specific operating system.

## Proton ##

I eventually settled on using Proton for most of my important online services. I have used Proton for several years, but never with a paid subscription or as my primary provider. This service checked off a lot of boxes for what I was looking for:

* The service combined several applications into one account and was simple to use.
* Encryption is enforced automatically on the services.
* The service was relatively simple to use, and does not require complex tools to customize.
* It was located on non-US servers (based in Switzerland).
* The Proton platform is not dependent on a particular operating system.

A bonus that I did not consider originally that was a bonus is that many of the Proton applications are [open source](https://proton.me/community/open-source/).

There are several versions of Proton subscriptions that can be used, all offering slightly different features and pricing:

| License          | Cost[^3]   | Storage  | Mail  | Calendar | VPN   | Drive | Pass  | Wallet |
|:-----------------|:-----------|:---------|:------|:---------|:------|:------|:------|:-------|
| Proton Free      | $0         | 1 GB     | Y     | N        | N     | N     | N     | N      |
| Mail Plus        | $4.99      | 15 GB    | Y     | Y        | N     | N     | N     | N      |
| Proton Unlimited | $12.49     | 500 GB   | Y     | Y        | Y     | Y     | Y     | Y      |
| **Proton Duo**   | **$18.74** | **1 TB** | **Y** | **Y**    | **Y** | **Y** | **Y** | **Y**  |
| Proton Family    | $28.19     | 3 TB     | Y     | Y        | Y     | N     | N     | N      |

[^3]: Proton subscription prices per month (without taxes), in CAD as of May 2025. These costs are for annual subscriptions only, and monthly subscriptions are 20% higher in costs.

I ended up getting the Proton Duo subscription as it had all of the features I was looking for.

### Proton Mail ###

Migrating from iCloud Mail to Proton Mail was straightforward and only required a few steps to complete. I added the same three domains and updated the DNS settings accordingly. I did try a different method for importing my existing email from iCloud. I used the **Easy Switch** tool from Proton, which took about 3 days to migrate my email. I then configured the **Proton Mail Bridge** application to allow my mail apps to access everything. This works perfectly fine with Outlook, but I don't use that application anymore.

Proton also supports backing up email using a CLI tool that is available for download.

The best part of Proton Mail is the ability to natively encrypt emails without the need for any external plugins. This works perfectly in the web interface and in the iOS client.

### Proton Issues ###

There are two issues that immediately come to mind, that are not deal breakers, but are minor issues:

* Contacts don't sync with the native iOS Contacts app, but apparently that feature is coming in a later release of the Proton Mail app.
* There is no Proton Drive application for Linux, but there is supposed to be a release "at some point in the future."

## What Was the Outcome? ##

I successfully migrated my email and other essential services from Microsoft 365. I am also on a platform that is not hosted in the US. I consider the exercise to be successful, even if it took several months of trial and error. I met all of the requirements that I originally set out to accomplish, as well as the added requirements starting at the beginning of 2025.

## Future ##

I will update my [current backup strategy](blog/2024/04/09/backup-strategy/) accordingly, as that process should always be reviewed no matter what.

I will also be posting about migrating other services to non-US providers, which will also include the services required for this website. I have already migrated my domains and my DNS provider to other countries.

## Links ##

* [Backup Strategy](blog/2024/04/09/backup-strategy/)
* [iCloud](https://icloud.com/)
* [LibreOffice](https://www.libreoffice.org/)
* [OpenOffice.org](https://www.openoffice.org/)
* [Proton](https://proton.me/)
* [Proton - Open Source](https://proton.me/community/open-source/)
* [Visual Studio Code with LaTeX](/blog/2020/01/23/visual-studio-code-with-latex/)
* [VoIP.ms](https://voip.ms/)
