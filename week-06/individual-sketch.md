#### Individual Sketch

```
| Entity | Verdict | Becomes | If no class, where it went |
|---|---|---|---|
| User | not a class | interface | canInteractWithGui |
| Manager | one class | Manager| - |
| Barista | one class | Barista | - |
| Customer | one class | Customer| - |
| Order | one class | Order | - |
| Menu | one class | Menu | - |
| Item | several classes | Item, MenuItem, OrderItem | - |
| Inventory | one class | Inventory| - |

```

```
### Manager
- Responsible for: interacting with inventory, menu, and item entities.
- Knows: managereID : int; login : String; password : String;
- Does: login(login : -String, password : -String), logout();
```

```
### Barista
- Responsible for: interacting with inventory, menu, and item entities.
- Knows: managereID : int; login : String; password : String;
- Does: login(login : -String, password : -String), logout();
```

```
### Manager
- Responsible for: interacting with inventory, menu, and item entities.
- Knows: managereID : int; login : String; password : String;
- Does: login(login : -String, password : -String), logout();
```

- `Responsible for:` is one sentence, under twenty-five words, with no "and" joining two jobs. If you need an "and," you've found two classes; write two blocks.
- `Knows:` is attributes, each `name: type`, separated by semicolons. A guess at a type is fine. A missing type is not.
- `Does:` is method signatures, each `name(parameters): returnType`, separated by semicolons. No method bodies. If a class does nothing, write `Does: nothing, see step 3`.

**Step 3: Where you'd put a hierarchy or an interface.** Pick the two or three sets of classes that have the most in common. Exactly these three columns:

```
| Classes | What I would do | Why |
|---|---|---|
| Member, Hold | nothing | they both carry an id and share nothing else |
```

**What I would do** is one of `abstract class <Name>`, `interface <Name>`, or `nothing`. **Why** is one sentence. `nothing` is a real answer and needs a Why like any other.

**Then section 2: what you're not sure about.** Name the decision and what you couldn't settle. *"Two classes needed the same three fields and I couldn't tell whether they shared a parent or just looked alike"* is useful. *"Unsure about structure"* is not.

**A verdict on every row of step 1 beats three perfect class blocks and nine entities you never reached.** Finish step 1 before you start step 2.

**Commit before group work starts:** `week-06/individual-sketch.md`

    