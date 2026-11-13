# Week 12: Individual Sketch
### ICS372 | Object-Oriented Design and Implementation

### Step 1

| File | What changes in it | Why it has to change |
|---|---|---|
| `Receipt.java` | The methods involving calculating the total and using discount method will have to change | The methods need to be modified to allow the use of different calculation strategies.|
| `DaySales.java` | The loyaltySavingsInCents method needs to be changed | The methods need to be modified to allow the use of different calculation strategies.|
| `Order.java` | The subtotalInCents method needs to be changed | The methods need to be modified to allow the use of different calculation strategies.|

`Total: 2 files`.

### Step 2

```java
public class Order {
    private final Customer customer;              // null for a walk-up customer
    private final List<OrderLine> lines = new ArrayList<>();
    private final Strategy chosenStrategy;

    public Order(Customer customer) {
        this.customer = customer;
    }

    public void add(OrderLine line) {
        lines.add(line);
    }

    public setStrategy(Strategy chosenStrategy) {
        this.chosenStrategy = chosenStrategy;
    }

    public Customer getCustomer() { return customer; }

    public int subtotalInCents() {
        int subtotal = 0;
        for (OrderLine line : lines) {
            subtotal += line.priceInCents();
        }
        return subtotal;
    }

    public int totalInCents() {
        int subtotal = subtotalInCents();
        int calculationStrategyResult = chosenStrategy.calculate(subtotal);
        return subtotal;
    }
}
```

#### Section 2 of the template: what I'm not sure about.

Not sure if I should have a collection of said strategies in here that I can rotate through or only one can be set.

**Do step 1 first, and quickly.** Step 2 is the one that matters, and a rough fix you can explain is worth more than a perfect count.

---
