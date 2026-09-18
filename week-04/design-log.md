# Design Log — Week 4
### ICS 372 FALL
**Student:** Salah Robleh
**Group:** 1 
**Date:** 9/17/2026 
**Topic:** Unsure

---

## Part 1 — The Problem

The problem for tonight was walking through certain use cases for actors of the system and breaking down the process in a step by step manner visualized with the addition of use case tables. Furthermore, the usage of sequence diagrams helped with showing the relationship between entities and entity activity. These tools feel somewhat tied together in the shape of further refining the domain model, and left our group and myself especially with alot of thinking on the gaps in our domain via left out entities.

---

## Part 2 — Your Design Decision

Our group combined our use cases and sequence diagrams into one copy where we refined our ideas completely rewritting our sequence diagram. For our use case diagrams we were suprisingly mostly on the same page albeit a bit different than what we discussed afterwards in class. Both of our use case scenarios had one or two steps way less than what was discusses as we thought the use case was limited towards the end of a process.



---

## Part 3 — How You Got There

I did not fully complete the use cases before the group talk portion so I did not come up with any alternative flows. Most of my ideas for alternative flows felt like they should've been preconditions especially for my portion scenario where a barista marks a order as complete. That is one action the barista is taking which should have a ton of preconditions nad not too much follow up or alternative flow. The only couple of alternative flow I could think of were if the order was cancelled in like a coffee shop the order would not be able to be completed but discarded. Therefore, I argued a position of my scenario having a bunch of preconditions with no alternative flow within my group, but ultimately could not feel 100% confident in my decision so we added another group members alternative flow to the final design. We believed sam should pay $5.00 instead of $4.50 but too be honest our domain model was not setup for it. We had only one item entity where I believe we should've had multiple types such as a menu item and cart item. This hopefully would allow the cart item to re calibrate it's price with the menu item's cost of ingredients whenver the menu item was updated.


---

## Part 4 — The Road Not Taken

Too be completely honest we believed our domain model was fine althought after listening to your interpertation of the scenario I believe that we would need to add a bunch of new entities to our domain model and will hope to add to the group sequence diagram furthermore on 9/18/2026. My thought is that once a menu item is selected, customized, and added to cart it is no longer a menu item but a selectedItem meaning it ceased to be a menu item entity and become it's own type of entity. Basically, our group needs to work alot more on refining our domain.

---

## Part 5 — What You're Uncertain About

Quite confused about the meaning between not finding every place a instance shape occurs. If shape means entity I believe that we were missing entites such as Menu, and dividing item into certain types such as menu item and cart item. Along with maybe some time of order manager responsible for adding orders to the barista queue to be worked on. Also could not understand whether order should be reponsible for adding itself to the barista queue. These were some of the concerns I had with our domain model.

---

## Word Count: [X words]

---

*Aim for 300–500 words across Parts 2–5. Part 1 does not count toward the word count.*
