---
title: "Additional configuration for my blog: Google Analytics"
date: 2019-02-16
tags: [Google Analytics]
excerpt: "Configuring google analytics"
---

## In this post I share the additional config for Google Analytics
I want to keep track of the traffic on the blog, so I will configure Google Analytics.

The first step is to go to *https://analytics.google.com/analytics/*.

Sign up using a Gmail account, for this purpose I used my personal Gmail account.

This is the general data you need to submit, the most important settings here are the blog URL and the "https" setting.  

<img src="{{ site.url }}{{ site.baseurl }}/images/googleanalytics_createaccount.PNG" alt="">

These other settings are optional, I only enabled the less intrusive ones: Benchmarking and Technical Support   

<img src="{{ site.url }}{{ site.baseurl }}/images/googleanalytics_datasharing.PNG" alt="">

One interesting fact about the Google Analytics Terms of Service Agreement is the pricing.

As described on section 2 of the Agreement the analytics is provided at no charge for "Hits" below 10,000,000. The definition of a "Hit" is also stated on the Agreement:

*"Hit" means the base unit that the Google Analytics system processes. A Hit may be a call to the Google Analytics system by various libraries, including, Javascript (e.g., analytics.js), Silverlight, Flash, and Mobile. A Hit may currently be a page view, a transaction, item, or event, social interaction, or user timing. Hits may also be delivered to the Google Analytics system without using one of the various libraries by other Google Analytics-supported protocols and mechanisms the Service makes available to You.*

Once the account is created a **Google Analytics Tracking Code(GATC)** is assigned. We need to add this code to our code in order to report to the platform. I'm using yml configuration files and Markdown markup language so my case I added it to my *_config.yml* file:

```yaml
# Analytics
analytics:
  provider               : google # false (default), "google", "google-universal", "custom"
  google:
    tracking_id          : UA-*********-*
```
That is the format of the **GATC** notice I masked my **tracking_id** for privacy purposes.

Finally once the site is configured it will be reporting the information can be seen on the Google Analytics Platform dashboard.

I tested it and it showed only active user, that's me:

<img src="{{ site.url }}{{ site.baseurl }}/images/googleanalytics_report.PNG" alt="">
