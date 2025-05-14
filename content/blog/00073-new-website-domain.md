---
title: "New Website Domain"
slug: "new-website-domain"
date: "2025-02-13T22:57:00"
author: "Matthew Burr"
summary: "I wasn't planning on making this change right now, but recent events have accelerated my schedule. I am retiring the mjcb.io domain and moving everything to the mjcb.ca domain for all of my online services. I wanted to make this change sooner rather than later, as it will take time for those changes to be propagated. Fortunately, I am not too concerned with a lot of the issues that arise from changing domains."
tags: [
    "EU Alternatives",
    "Netlify",
    "Website"
]
categories: [ "Blog" ]
thumbnail: "/images/blog/00073/mjcb.png"
toc: false
draft: false
---

I wasn't planning on making this change right now, but recent events have accelerated my schedule. I am retiring the **mjcb.io** domain and moving everything to the **mjcb.ca** domain for all of my online services. I wanted to make this change sooner rather than later, as it will take time for those changes to be propagated. Fortunately, I am not too concerned with a lot of the issues that arise from changing domains.

As of today, the **mjcb.io** domain that I have been using since 2018 is now deprecated. I am now using the **mjcb.ca** domain for my online presence. I have setup the old domain to redirect all URLs to the new domain, and it should be transparent to people that are using the old domain. This change also applies to the **docs.mjcb.io** domain as well, as it is being redirected to the **docs.mjcb.ca** domain. I will leave this redirect in place indefinitely.

Luckily, Netlify makes this change trivial to complete (similar to an htaccess file):

```
[[redirects]]
    from = "https://mjcb.io/*"
    to = "https://mjcb.ca/:splat"
    status = 301
    force = true
```

There are a lot of reasons why I decided to make this change now, and I will go into details in later posts as there are a lot of other changes going on. Other items will slowly be updated to reflect this new domain name, and that will occur over the new few months.

I also made a few other changes, and that is with the GitHub repository that I was using for hosting the website repo, as well as the analytics tool. I have migrated to a different [GitHub profile](https://github.com/mjcb-public/) for my public repositories, as I was never comfortable with mixing private and public repos. I also got rid of Google Analytics and moved to a different provider ([Simple Analytics](https://www.simpleanalytics.com/)).

My [contact information](/about/#contact) has also been updated as a result of the domain name change.

Hopefully this change is completely transparent and doesn't cause any issues. I have been keeping an eye on the traffic for the last few days and I can't see any issues so far.

## Links ##

* [GitHub Profile](https://github.com/mjcb-public/)
