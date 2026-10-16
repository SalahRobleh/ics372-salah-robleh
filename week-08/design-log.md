# Week 8: Design Log
### ICS372 | Object-Oriented Design and Implementation

- **Part 1:** Tonight wasn't "write constructors." Say what the problem actually was.
- **Part 2:** Describe how your group's final code gets its menu: which classes use it, how each one gets it, and where it's created, for the shop and for the test. Name the files.
- **Part 3:** Pick one row from your sketch's table. Say how you chose to get that object, what made that look right at the time, and what the test setup would have cost if you'd chosen differently.
- **Part 4:** Argue for the Singleton. Name one class in Brew & Byte where having exactly one copy that any class can reach could be defended, and make the strongest case for it, fairly enough that someone who wanted it would recognize their own argument.
- **Part 5:** Name one thing about how your objects get created and connected that you still can't say for certain, and what you'd need to see to decide it.

####
The problem for tonight was making sure our classes worked well together when it comes to passing or requesting data to one another while making sure the classes can be built properly from the constructors.
####
Our group's current code menu class is used by our interface classes, inventory classes, and orderManager class. The classes get access to the menu class via constructor injection and the shop class gets it aswell via constructor injection. The files incluse: `Menu.java`, `customerInterface`, `BaristaInterface`, `ManagerInterface`, `Invetory`, `OrderManager`.
####
| Class | Calls | How it gets it | Where that object comes from |
|---|---|---|---|
| `Menu` | `removeItem` | called by a missing barista interface | ingredient selected from barista interface and `handed in on the call` |

This row from my individual sketch table was chosen in UC-4: Mark an ingredient as out. This row was supposed to represent the menu removing an item that used that missing ingredient and at the time I thought the barista interface class should call it using construction injection. Reflecting on this sketch I still believe the barista interface class removing the method is correct because it holds a list of all active menu items. I'm not sure how else I could have tested this setup of a menu removing this item except for having another class call the menu remove item.
####
The one class that I believe could be a good singleton class would be the saveLoadManager class. There shouldn't be too much testing done with this class and I don't see any scenario where I would need more than one instance of this class. The static methods allow for any object to get a reference to the class and then serialize.
####
One thing about how my objects get created and connected that I still can't say for certain is how the user input can be done for the barista, manager, and customer to interact with the system either via terminal or with a gui.



    