---
title: "What's the difference between a proxy and reverse proxy server?"

tags: [proxy]
categories: [software engineering]
---

## Proxy server

In a proxy server, the servers do not know which client is making the request.

A VPN server is a type of proxy server which allows a client to hide their actual IP address from the servers.

## Reverse proxy server

In a reverse proxy server, the clients do not know which server is responding to the request.

A load balancer is a type of reverse proxy server that distributes its traffic to available servers to process requests. The clients wont know which specific server has responded to their request.
