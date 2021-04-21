---
layout: post
title: Database Indexes
date: 2021-04-21 10:00:18 +1000
categories: tech
---

Webhooks are a technique used to allow you to "hook" into an external service's event and send automated messages when said event occurs.s

### How they work

Let's have a look at GitHub, who has webhook support.
Let's focus on the two main configs:

1. Payload URL (aka webhook URL)
2. Which events would you like to trigger this webhook?

This means that for any push events that occur on this GitHub Repository, a `POST request` is sent to the provided Payload URL (http://mymessageservice.com). Now the message service can do whatever it wants with this request, such as notify a user.

### Webhooks vs Polling

The benefits of webhooks can be seen when you compare to the polling technique. If we wanted
