# Individual Sketch — Week 4 Round 2
**Student:** Salah Robleh
**Date:** 9/17/2026

---

## My Answer



---

## Diagram


```mermaid
sequenceDiagram
  actor Customer
  participant Item
  participant Cart
  participant Barista

  Customer ->> Item: selectsItemFromMenu
  Item ->> Cart: findBook("Dune")
  Library ->> Catalog: search("Dune")
  Catalog -->> Library: book
  Library -->> UI: book
  UI -->> Member: display results
```

---

## What I'm Not Sure About

*One or two sentences. What feels uncertain or wrong about what you just produced?*

[Your response here]

---

**Commit this file before group discussion begins.**
