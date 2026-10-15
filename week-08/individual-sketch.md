
# Individual Sketch ��� Week 8 Round 1
**Student:** Salah Robleh
**Date:** 10/15/2026

---

## 1. Tonight's Prompt

**Step 1: How each class gets what it calls.** For every solid arrow in your diagram that goes from one class to another class, one row. Skip arrows from the actor. If one class calls the same other class more than once, that's still one row.

Exactly these four columns:

| Class | Calls | How it gets it | Where that object comes from |
|---|---|---|---|
| `Menu` | `removeItem` | called by a missing barista interface | ingredient selected from barista interface and `handed in on the call` |

```java
public Menu(int menuID)
```


## 2. What I'm Not Sure About


I note that the class model is missing a way for the barista agent to interact with system like a barista interface class where one option is to mark an ingredient out and the barist can put the ingredient name or id. Also not sure if there should be another class that holds a Menu instance, or if the menu should be a singleton that can give its reference to the ingredient class. I believe it's necessary because whenever an ingredient is marked out the menu class can look if any items use that out of stock ingredient then remove the item from the pickable item list.

---

**Commit this file before group discussion begins.**

    