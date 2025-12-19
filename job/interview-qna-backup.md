# 30 Interview Questions and Answers for Senior Back-End/Full-Stack Engineer with Payments Experience

## .NET & C# Core Concepts

**1. What are the key improvements in .NET 6+ compared to earlier versions?**

*Answer:* .NET 6+ introduces: **Minimal APIs** for lightweight HTTP APIs with reduced boilerplate, performance improvements (30-40% faster), hot reload for faster development, unified platform for all workloads, C# 10 features (global usings, file-scoped namespaces, record structs), native HTTP/3 and gRPC support, improved async performance, ARM64 support, and better cloud diagnostics. .NET 8 adds Native AOT compilation, improved JSON serialization, enhanced container support, and better Blazor capabilities.

**2. Explain async/await and why it's crucial for scalable back-end systems.**
*Answer:* `IEnumerable` executes the query in memory (client-side evaluation). It fetches all data from the database and then filters it. `IQueryable` executes the query on the server (database side) by translating the LINQ query into SQL. Use `IQueryable` for database queries to minimize data transfer.

**3. What is the difference between `Task` and `Thread`?**
*Answer:* A `Thread` is a lower-level OS concept. A `Task` is a higher-level abstraction from the Task Parallel Library (TPL) that represents an asynchronous operation. A Task may or may not run on a separate thread; it uses the thread pool efficiently. `async/await` works with Tasks.

**4. How does Garbage Collection (GC) work in .NET?**
*Answer:* GC manages memory allocation and release. It works on the Managed Heap. It has three generations (0, 1, 2). New objects go to Gen 0. If they survive a collection, they move to Gen 1, then Gen 2. GC checks for objects that are no longer reachable by the application root and frees their memory.

**5. What is Middleware in ASP.NET Core?**
*Answer:* Middleware are software components assembled into an application pipeline to handle requests and responses. Each component chooses whether to pass the request to the next component in the pipeline and can perform work before and after the next component. Examples: Authentication, Logging, Exception Handling.

**6. Explain `async` and `await`. Why should we use them?**
*Answer:* They are markers for asynchronous programming. `async` marks a method as asynchronous, and `await` pauses the execution of the method until the awaited task completes, without blocking the main thread. This improves application scalability and responsiveness, especially for I/O-bound operations (DB calls, API calls).

**7. What are the different service lifetimes in .NET Core DI?**
*Answer:*
- **Transient:** Created each time they are requested.
- **Scoped:** Created once per client request (connection).
- **Singleton:** Created the first time they are requested (or when the app starts) and every subsequent request uses the same instance.

**8. What is the difference between an abstract class and an interface?**
*Answer:* An interface defines a contract (what methods/properties must exist) but no implementation (until C# 8 default implementations). A class can implement multiple interfaces. An abstract class can provide some default implementation and fields, but a class can only inherit from one abstract class. Use interfaces for capabilities (CanDoSomething), abstract classes for "is-a" relationships with shared logic.

**9. How do you handle exceptions globally in ASP.NET Core?**
*Answer:* By using the built-in Exception Handler Middleware (`app.UseExceptionHandler`) or by creating custom middleware that wraps the `next()` delegate in a try-catch block, logging the error, and returning a standardized error response (e.g., ProblemDetails).

**10. What is Entity Framework Core and what is "Code First"?**
*Answer:* EF Core is an ORM (Object-Relational Mapper) for .NET. "Code First" means you define your domain classes (entities) first, and EF Core generates the database schema from them using Migrations.

## JavaScript / TypeScript (React & Svelte)

**11. What is the difference between `var`, `let`, and `const`?**
*Answer:* `var` is function-scoped and can be hoisted. `let` and `const` are block-scoped. `let` allows reassignment, while `const` does not (though object properties in a const object can be changed). Always prefer `const`, use `let` if needed, avoid `var`.

**12. What is the Virtual DOM in React?**
*Answer:* The Virtual DOM is a lightweight copy of the actual DOM in memory. When state changes, React updates the Virtual DOM first, compares it with the previous version (diffing), and then efficiently updates only the changed elements in the real DOM (reconciliation). This improves performance.

**13. Explain the concept of "Props" and "State" in React.**
*Answer:* **Props** (properties) are read-only inputs passed from a parent to a child component. **State** is internal data managed by the component itself that can change over time. When state changes, the component re-renders.

**14. What is Svelte and how does it differ from React?**
*Answer:* Svelte is a compiler, not a runtime framework like React. It compiles components into highly efficient imperative code that directly manipulates the DOM. It doesn't use a Virtual DOM, leading to smaller bundle sizes and faster performance.

**15. What is TypeScript and why use it?**
*Answer:* TypeScript is a superset of JavaScript that adds static typing. It helps catch errors at compile time rather than runtime, provides better tooling (IntelliSense), and makes code more maintainable and self-documenting.

**16. What are React Hooks? Name a few common ones.**
*Answer:* Hooks allow function components to use state and lifecycle features. Common ones: `useState` (manage state), `useEffect` (side effects like data fetching), `useContext` (access context), `useRef` (access DOM elements).

**17. How does data binding differ between React and Svelte?**
*Answer:* React uses **one-way data binding** (parent to child). Svelte supports **two-way data binding** (using the `bind:` directive), which simplifies handling form inputs, though one-way flow is still preferred for state management.

## Azure Cloud

**18. What is an Azure App Service?**
*Answer:* It's a fully managed Platform as a Service (PaaS) for hosting web applications, REST APIs, and mobile backends. It handles auto-scaling, load balancing, and deployment slots.

**19. What are Azure Functions?**
*Answer:* A serverless compute service that lets you run event-triggered code without explicitly provisioning or managing infrastructure. You pay only for the compute time consumed.

**20. Explain the difference between IaaS, PaaS, and SaaS.**
*Answer:*
- **IaaS (Infrastructure as a Service):** You manage OS, runtime, middleware (e.g., Azure VMs).
- **PaaS (Platform as a Service):** You manage data and app, cloud manages OS/runtime (e.g., App Service).
- **SaaS (Software as a Service):** You just use the software (e.g., Office 365).

**21. How would you secure an API in Azure?**
*Answer:* Use Azure API Management (APIM) as a gateway. Implement authentication/authorization using Azure Active Directory (Entra ID) or OAuth 2.0. Use Key Vault to store secrets. Enable HTTPS.

**22. What is Docker and how does it relate to Azure?**
*Answer:* Docker packages an application and its dependencies into a container that runs consistently anywhere. Azure supports Docker via Azure Kubernetes Service (AKS), Azure Container Apps, and App Service for Containers.

## Testing & TDD

**23. What is TDD (Test-Driven Development)?**
*Answer:* A development process where you write a failing test *before* writing the production code. Cycle: Red (Write failing test) -> Green (Write minimal code to pass) -> Refactor (Clean up code).

**24. What are the benefits of TDD?**
*Answer:* It ensures high test coverage, leads to better software design (modular, loosely coupled), reduces bugs, and acts as living documentation. It gives confidence when refactoring.

**25. What is the difference between Unit Testing and Integration Testing?**
*Answer:*
- **Unit Testing:** Testing a small, isolated unit of work (e.g., a method) mocking all dependencies. Fast.
- **Integration Testing:** Testing how different modules work together (e.g., API calling a database). Slower, verifies the system as a whole.

**26. What is Mocking?**
*Answer:* Creating a fake object that simulates the behavior of a real dependency (like a database service) to isolate the unit being tested. We use libraries like Moq in .NET.

## Soft Skills & Behavioral

**27. How do you handle a disagreement with a team member about a technical decision?**
*Answer:* I focus on the problem, not the person. I listen to their perspective, present my arguments with data/pros-cons, and try to find a consensus. If needed, we can build a quick prototype (POC) to compare approaches or ask a senior for input.

**28. Describe a time you had to learn a new technology quickly.**
*Answer:* (Example) "In my last project, we needed to migrate to Azure Functions. I hadn't used them extensively, so I spent the weekend reading documentation, built a small POC, and by Monday I could guide the team on the basic structure."

**29. Why do you want to work at niwadev?**
*Answer:* I appreciate the focus on "quality software" and "eye-level communication". The opportunity to work on individual software solutions from A to Z appeals to me because I enjoy seeing the full lifecycle. Also, the tech stack (C#, Azure, React/Svelte) aligns perfectly with my interests.

**30. How do you ensure code quality?**
*Answer:* By following Clean Code principles, writing unit tests (TDD), performing code reviews, using static analysis tools (SonarQube), and maintaining CI/CD pipelines to catch issues early.