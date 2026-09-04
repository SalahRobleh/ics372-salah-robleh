# Individual Sketch — Week [2] Round [2]
**Student:** [Salah Robleh]
**Date:** [09/03/2026]

---

## My Answer

*Respond directly to the prompt. Write in plain sentences — no need to be formal. You have 12 minutes total, so think first, then write.*

In java when created I believe an order will be just tied to a customer maybe when they first start looking at the menu after creating a customer entity. Each order has to be tied to one customer while I belive a customer can have multiple orders.

1. An order when first instantiated should be assigned a unique identifier, and a empty collection type that can store menu items in the future, also I believe a status that can represented with strings or numerical that represents its current state. For example a order with no items can be either a empty order or a order being built, while a order that is placed would be assigned a status of placed. The methods needed for the order class should be to add a menu item to its collection type and remove menu items from tis collection type, along with the option to place order. The unique ID should stay the same

2.If a order has been submitted its status field should be updated to in progress and it should have a list of menu items the size of one menu item or more. The methods needed for the order class should be to add a menu item to its collection type and remove menu items from tis collection type, along with the option to place order. The unique ID should stay the same

3. When the order is completed and picked up by the customer it can either be just have a status of complete or status of complete and then when picked up be further changed to picked up. Once again the list of orders should be one or more and the order must persist and be assigned to the list of fullfilled orders. The methods needed for the order class should be to add a menu item to its collection type and remove menu items from tis collection type, along with the option to place order. The unique ID stays the same throughout all of these 3 states.

---

## Diagram

*Include your Mermaid diagram below. If the prompt doesn't ask for a diagram, delete this section.*

```mermaid

```

---

## What I'm Not Sure About

*One or two sentences. What feels uncertain or wrong about what you just produced?*

[Similiar worries to last round if the order class should have certain methods other than methods that deal directly with the fields in it's class and not other fields. I did my best to limit the methods in the order class to try to adhere to single responsiblity principle.]

---

**Commit this file before group discussion begins.**