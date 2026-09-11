# Group Artifact — Week 3 Round 01

**Group:** 1
**Members present:** Nadia Konieczny, Connor Goehring Trempe, Salah Robleh, Kaashif Khan
**Date:** September 10th, 2026

---

## Part A: Table of Requirements

| Req | Functional / Non-Functional / Neither | Why, if it was arguable                                        |
| --- | ------------------------------------- | -------------------------------------------------------------- |
| 1.1 | Neither                               | Implementation                                                 |
| 1.2 | Neither                               | Implementation                                                 |
| 1.3 | Neither                               | Implementation                                                 |
| 1.4 | Non-Functional                        | Speed/reliablity                                               |
| 2.1 | Functional                            |                                                                |
| 2.2 | Functional                            |                                                                |
| 2.3 | Functional                            |                                                                |
| 2.4 | Functional                            |                                                                |
| 2.5 | Functional                            |                                                                |
| 2.6 | Functional                            |                                                                |
| 2.7 | Neither / disagree                    | Very vague how to interpret                                    |
| 2.8 | Neither / disagree                    | Discount is a function, but there's also a constraint involved |
| 3.1 | Functional                            |                                                                |
| 3.2 | Functional                            |                                                                |
| 3.3 | Functional                            |                                                                |
| 3.4 | Non-Functional                        | More of a constraint on placing orders than a function         |
| 3.5 | Functional                            | Could also see as a constraint                                 |
| 3.6 | Functional                            |                                                                |
| 3.7 | Non-Functional                        | Constraint on access, not a function                           |
| 4.1 | Non-functional                        | Can be treated as a constraint                                 |
| 4.2 | Functional                            |                                                                |
| 4.3 | Functional                            |                                                                |
| 4.4 | Functional                            |                                                                |
| 4.5 | Functional                            |                                                                |
| 4.6 | Functional                            | Mentions order time so needs to keep track of it               |
| 5.1 | Neither                               |                                                                |
| 5.2 | Neither                               |                                                                |

---

## Part B: Questions

1. 4.4 Says the system should warn you when inventory is getting low but it doesn't specifiy what "low" is exactly. Does every ingredient need its own low stock amount or should the same threshold be used for all ingredients? One threshold would probably be simpler to manage, while individual thresholds would require different restocking points.
2. 3.7 and 4.1 contradict because 3.7 says a barista can add a menu item when the manager isn't present but 4.1 says only managers can modify the menu. Should baristas be allowed to add menu items when manager's are not there or should they wait for the manager before changes are made? Restricting it to managers would give more control over the menu, for now the assumption will be that only managers can modify the menu.
3. 4.3 says a manager can restock an ingredient, but then describes the owner being the one to update inventory. Can managers update inventory directly, or not?

---

## How We Got Here

We went through the numbered items and each of us had most items in functional because most of the items do describe things the system should do. There are few items in the neither category because they were either too vague or just didn't help describe the system as a whole (both items under section 5). The others are in non-functional because they generally describe constraints/speed/reliability that don't necessarily translate to actual objects.

---

## Where we disagreed

2.8 was somewhat split between neither and functional, as it could either be something that the customer handles itself (meaning neither), but since it needs to be entered into the system it's functional.
2.7 was also iffy because of how vague it was.

---

## What We're Unsure About

Besides the questions posed above in Part B: we felt we have a bit too much in functional in general. Some requirements seemed to involve both functions and constraints.
