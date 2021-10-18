---
title: "Consistency vs. availability"

tags: [distributed systems]
categories: [software engineering]
---

Let's consider the following scenario, Arya and Bhavani want to collaborate on an online document.

## Always consistent, but not always available

One approach is when one person is working on the document, the document is locked to prevent the other person from working on it at the same time. This is the approach used in WordPress.

The trade-off here is that the document remains locked as long as one person has the document opened, making it unavailable for anyone else to work on it.

This guarantees that the document is **always consistent, but not always available**.

This approach is used in WordPress and Microsoft SharePoint.

## Always available, but not always consistent

Another approach is to allow both parties to work on the document at the same. This is the approach in Google Docs.

The trade-off here is that there may be conflicts and occasionally someone might overwrite the other person's work.

This approach guarantees that the document is **always available, but not always consistent**.

## Conclusion

In a distributed system, partition tolerance is non-negotiable as network reliability is unpredictable. Therefore, an application must choose between consistency and availability.

A service can have

- high consistency by blocking any requests (not available) to the data until they are resolved, or
- high availability by returning data that may be stale (not consistent)

There are trade-offs to either approaches and the right solution depends on what's important for your application.

For instance, it is more important for a shopping cart to have high availability. On the other hand, a bank account balance must always be consistent.
