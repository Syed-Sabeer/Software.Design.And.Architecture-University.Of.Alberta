FOr the technical design we need to arrange every component of our software system , each component do have its responsiblities and components. 


CRC CARD: 
- Class Name 
- Responsilibites 
- Collaborators

Class-responsibility-collaboration (CRC) cards are a physical or digital brainstorming tool used in object-oriented software design to model classes, their responsibilities, and how they interact.

----------------------------------------
               CLASS NAME 
----------------------------------------
RESPONSIBILITIES   |    COLLABORATORS


CRC cards help you to organize your components into classes, identify the responsibilities and determine how they will collaborate with each other.
CRC cards are used to record, organize and refine the components in your design.



Collaborators: 
Collaborators are other classes that the class interacts with to fulfill its responsibilities.

In the collaborator section we mention other components which are linked or connected with our component to fulfill its requirements.


the advantage of using CRC is that it allows us to physically reorganize the design. when we start making components through CRC cards its make our scope clear to identify what further components are required to design our system . 

Example: Bank System 
Now, let's consider the scenario of the bank machine authenticating our bank customer.
- You can imagine enacting our bank customer's insert card responsibility. This in turn, collaborates with the bank machine and triggers its responsibility to authenticate the bank customer. Once authenticated, the bank machine enacts its responsibility to display the task options.



This is our Bank Customer Component CRC Card
----------------------------------------------------
Bank Customer 
----------------------------------------------------
Responsiblities          |  Collaborator
- Insert back card       |  - Bank Machine or ATM
- Choose Operation       |



This is our Bank Machine or ATM CRC Card
----------------------------------------------------
Bank Machine or ATM
----------------------------------------------------
Responsiblities                |  Collaborator
- Authenticate Bank Customer   |  - Bank Customer 
- Display Task Options         |
- Deposit and Withdraw         |
- Check Balances               | 


