---
title: "Types of data structures"

tags: [data structures]
categories: [software engineering]
---

In the Algorithm Design Manual, Skiena explains that there are two types of data structures – contiguous and linked data structures. Their distinction being how they are stored in memory.

1. **Contiguous data structures** are composed of a single slab of memory, and include arrays, hash tables, matrices, and heaps.

1. **Linked data structures** are composed of distinct chunks of data bound together by *pointers*, and include linked-lists, trees, and graphs.

---

Under the hood, heaps are actually arrays with an implicit binary tree structure. Hash tables are represented by an array of linked-lists while matrices use an array of arrays to represent them. Since they all use arrays they are all contiguous data structures.
