---
title: "CAP Theorem"

tags: [distributed systems]
categories: [software engineering]
---

The CAP Theorem states that you can only provide two out of the following three guarantees:

- Consistency
- Availability
- Partition tolerance

Given that networks are not reliable, one of the two guarantees **must** always be partition tolerance. Therefore, realistically, we only have consistency and availability to choose from.
