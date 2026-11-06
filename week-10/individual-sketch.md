# Week 10: Individual Sketch
### ICS372 | Object-Oriented Design and Implementation

---

````markdown
```java
public void Hashset<OrderItem,int> getAmountOfSoldMenuItems {
    HashSet<OrderItem,int> newHashet = Hashset<>();
    List<Order> pastOrders = this.pastOrders;
    for (Order order : pastOrders) {
        Hashset<O.getOrderQuantity()
    
    }

}
```
````

Write it against your group's classes as they are now in `src/main/java`. If you need a method that doesn't exist yet, write the call anyway, and put a comment on that line naming the class it belongs to. Don't change any files in the repo; this lives in your sketch only.

**Step 2: The walk table.** One row for every collection your method walks that belongs to **another** class: a list, an array, a set or a map. If your method walks the same class's collection twice, that's still one row.

Exactly these four columns:

| Walks it | Whose collection | What it gets | Could it change it? |
|---|---|---|---|
| `OverdueReport` | `Member`'s holds | a copy | no |

**What it gets** is exactly one of these five values:

- `the collection itself`: the owner hands over its own field, like `getHolds()` whose body is `return holds;`. This is also the value when the walker made the list and handed it to the owner, because both now hold the same list.
- `a copy`: a new collection with the same objects in it, like `List.copyOf(holds)` or `new ArrayList<>(holds)`.
- `a read-only view`: the owner's own collection wrapped so that any change throws an exception, like `Collections.unmodifiableList(holds)`.
- `an iterator`: the owner hands out something that walks its collection, and nothing else. The owner implements `Iterable<Hold>`, so the walker writes `for (Hold hold : member)`.
- `the answer`: the owner walks its own collection and hands back only the result, like `member.countOverdue(today)`. Your method then doesn't walk it at all, but the row still goes in.

**Could it change it?** `yes` if your method, or anything holding what your method got, could add to the owner's collection, take something out of it, or reorder it. `no` if it couldn't.

**Section 2 of the template: what you're not sure about.** Name the row you were least sure of, and what made it hard to decide.

**Get the body down first, even with calls that don't exist yet.** A rough method with every walk in it is worth more than a perfect one that stops halfway.