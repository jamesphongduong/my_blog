---
layout: post
title: IP Addresses and Port Forwarding
date: 2021-05-03 10:00:18 +1000
categories: tech
---

The internet needs a way to differentiate computers, routers and websites, hence the need for IP addresses (unique address that IDs devices on the internet or on a local network.)

There are two types of IP addresses:

1. Public IPs: used by routers and are accessible by the public
2. Private IPS: used by devices that are only known to a router and its home network

Routers have 2 IP addresses as it requires both to act as a middleman between the local network and the wide web:

1. WAN (Wide Area Network): Public IP address used to face the Internet
2. LAN (Local Area Network): Private IP address used for the home network

# Basic home network with router setup

![horizontal scaling diagram](/images/ip_addresses.svg)

With this current setup, if the computer on the Internet side wanted to access the node server via 66.117.135.8:8080, additional configuration is required. With standard configuration, the router won't know what to do with the request.

A common method to get this working is doing **port forwarding** which is achieved by configuring the Router options. You configure incoming requests on a port number for the WAN and where said requests go to in the internal network.

`8080 (port number) -> 192.168.100`
