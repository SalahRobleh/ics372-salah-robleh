# Individual Sketch — Week 4 Round 1
**Student:** Salah Robleh
**Date:** 9/17/2026

---

## My Answer

---

### UC-1 Barista Marks an Order Complete

**Actor:** Barista 

**Precondition:** Order could not have been a empty order,
Order must be fulfilled meaning no item is missing from customer's order, Customer hasn't cancelled the order, Ingredients level for each ordered item is sufficient for the item to be prepared.

**Postcondition:** Order is no longer in the queue of incoming orders, order information has been pushed to the database, all items required ingredeients deducted from inventory ingredient levels.

**Main flow**

| Actor Action | System Response |
|---|---|
| 1. Barista Clicks the mark order as complete button | |
| | 2. System checks if order was not empty, order was not cancelled by customer, sufficient ingredient levels for each item for the order to be fulfilled. If one or more of these conditions fail then go to alternative flow. If sucessful remove order from active incoming order list and push order information to recording database. Afterwards show next incoming order screen.

**Alternative flows**

*Each one is keyed to the step in the main flow where it branches. Say where it rejoins, or that it ends the use case.*

**[A1] At step 3 ��� [what is different this time]**

| Actor Action | System Response |
|---|---|
| 3a. [What the actor does instead.] | |
| | 3b. [How the system responds.] |

*Rejoins the main flow at step 4.* [or: *Ends here; the postcondition does not hold.*]

**[A2] At step [N] ��� [what goes wrong]**

| Actor Action | System Response |
|---|---|
| | [N]a. [What the system does about it.] |

*[Where it goes.]*

**Assumptions:** [Anything you decided that the requirements did not decide. Cross-reference the entry in `open-questions.md`.]

---,


---

---

## What I'm Not Sure About

*One or two sentences. What feels uncertain or wrong about what you just produced?*

[Unsure about what is functional and what is non-functional if im categorizing correctly.]

---

**Commit this file before group discussion begins.**



































