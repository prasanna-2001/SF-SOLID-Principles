# SF-SOLID-Principles

S – Single Responsibility Principle (SRP)

O – Open/Closed Principle (OCP)

L – Liskov Substitution Principle (LSP)

I – Interface Segregation Principle (ISP)

D – Dependency Inversion Principle (DIP)

1. Single Resonsibility Principle : 
“A class should have only one reason to change.”
In simpler terms, every class, module, or function should focus on doing one thing well. When a class has multiple responsibilities, even a minor change in one area can unintentionally affect another.

Instead of cramming all logic into one big class, I:
Defined a common interface that acts as a contract.
Created separate implementation classes, each handling a specific concern.
Built a service class with a map that identifies which implementation to call using the interface.
Finally, used the service class from the controller, keeping it lean and focused on orchestration only.

✅ Result: Code that’s easier to read, test, and extend — whether I need to onboard new logic or update existing ones for specific actors.

📌 Why SRP matters in Salesforce development:
Promotes better separation of concerns
Improves testability and reusability
Simplifies maintenance and debugging

In the Folder structure : Instead of creating a single class to get ata for all the different users create through "CombinedGetDataClass"
Created :1. "GetDataInterface" and interface with "getData()" Method. 2. Created different implementation classes like GetDatForCEO 3. created service class which calls respective implementation class.
