
# Week 11: Individual Sketch
### ICS372 | Object-Oriented Design and Implementation

---

Tonight you start from code somebody else wrote. Open `week-11-the-case.md`. Read it whole before you start: every file, and the requirement at the end.

Copy steps 1 and 2 into **section 1 of your sketch file** and put your work directly under each step.

**Step 1: What the barista's screen costs.** Don't write the screen. Work out what adding it would do to the case as it stands.

In a table with exactly these three columns, one row for every file in the case that would have to change:

| File | What changes in it | Why it has to change |
|---|---|---|
| `OrderDesk.java` | the constructor gets a sixth parameter which is the view class | the new class needs to be handed in on creation |
| `OrderDesk.java` | the `OrderDesk.place(Order order)` method needs to be changed | the method now needs to print out a list of orders whenever a new ordered is added |
| `OrderDesk.java` | the `OrderDesk.place(Order order)` method needs to be changed | the method now needs to print out the orders waiting whenever a new ordered is added |
| `OrderDesk.java` | the `OrderDesk.completeNext(LocalDateTime now)` method needs to be changed | the method now needs to print out the orders remaining after completing a order |
|`PlaceOrderTest.java`|this test class needs to be changed|The test class needs to include the new sixth paramter to compile.|
|`CompleteOrderTest.java`|this test class needs to be changed|The test class needs to include the new sixth paramter to compile.|
|`Order.java`|this data class needs to be modified|Due to the requirement of printing out every order I believe a to String methid should be included so we can have a public method that can print out information about each order object class so the collection class can present it to the user.|

`Total: 4 files`

```java
package edu.metrostate.oodi.brewandbyte.model;

import edu.metrostate.oodi.brewandbyte.view.ManagerWarnings;
import edu.metrostate.oodi.brewandbyte.view.PickupBoard;
import java.time.LocalDateTime;

public class OrderDesk {
    private final OrderQueue queue;
    private final Inventory inventory;
    private final SalesLedger ledger;
    private final ManagerWarnings warnings;
    private final PickupBoard pickup;
    private final BaristaScreen bScreen;

    public OrderDesk(OrderQueue queue, Inventory inventory, SalesLedger ledger,
                     ManagerWarnings warnings, PickupBoard pickup,
                     BaristaScreen bScreen) {
        this.queue = queue;
        this.inventory = inventory;
        this.ledger = ledger;
        this.warnings = warnings;
        this.pickup = pickup;
        this.bScreen = bScreen;
    }

    public void place(Order order) {
        queue.add(order);
        // Assumes that queue.next() method returns a boolean
        while (queue.next()) {
            System.out.println(queue.next().toString());
        }
    }

    public void completeNext(LocalDateTime now) {
        Order order = queue.next();
        order.markComplete(now);
        for (Ingredient low : inventory.useUp(order)) {
            warnings.lowStock(low);
        }
        queue.remove(order);
        ledger.record(order);
        pickup.call(order.getConfirmationNumber());
    }
}
```

**Section 2 of the template: what you're not sure about.** Name the part of your fix you're least sure would work, and what would show you.

**Do step 1 first, and quickly.** Step 2 is the one that matters, and a rough fix you can explain is worth more than a perfect count.

