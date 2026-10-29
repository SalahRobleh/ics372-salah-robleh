
# Week 10: Individual Sketch
### ICS372 | Object-Oriented Design and Implementation

**25 minutes, alone.** Commit to `week-10/individual-sketch.md`.

## Checklist

Check every box before you commit. **10 points.**

- [ ] Step 1 has the whole body of your method in Java, with every call it makes **(3 pts)**
- [ ] Step 2 has a row for every collection your method walks that another class owns, with exactly one of the five values under **What it gets** **(3 pts)**
- [ ] Every row of step 2 says `yes` or `no` under **Could it change it?** **(2 pts)**
- [ ] Section 2 of the template says what you're least sure of **(2 pts)**
- [ ] Committed to `week-10/individual-sketch.md` **(required: nothing is graded without it)**

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


- **UC-2:** the method that uses up the ingredients for every item on the order, including the ingredients its customizations add (step 5).
- **UC-3:** the method that counts how many of each menu item sold today (steps 2 and 3).

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