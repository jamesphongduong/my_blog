---
layout: post
title: Webhooks
date: 2021-04-21 10:00:18 +1000
categories: tech
---

Webhooks are a technique used to allow you to "hook" into an external service's event and send automated messages when said event occurs.

### Webhooks vs Polling

Imagine if you wanted to buy a specific MacBook model from the Apple website, and wanted to know when it went on sale. One method of doing so would be to checking the Apple website everyday. 
This manual process of having to constantly check for updates is known as _polling_.

What would be nice is if Apple, gave us the option to subscribe to the sale event of this specific MacBook model. And once this "sale event" occurs, then please notify me. 
This method is known as a _webhook_.

### Benefits 
- Resource efficiency - polling is an expensive process as you are constantly checking for updates and the majority of the time you are fetching data that hasn't changed, whereas webhooks are only executed when required
- Latest data - polling doesn't guarantee up-to-date data as data fetching occurs in intervals, whereas webhooks does

