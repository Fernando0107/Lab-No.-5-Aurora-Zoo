# Lab: The Aurora Zoo

## Overview

Build a **command-line zoo simulator** in **C# with .NET**. When launched, the app must greet the visitor, present **zoo areas** to explore, allow the visitor to pick an area, then **list animals** in that area. After the visitor chooses an animal, the app should display a **fun fact** about it. Emphasize **OOP fundamentals**: classes, properties, attributes/fields, and **interfaces**.

> **Deliverables:** a runnable .NET console app and a short README.

---

## Objectives

- Practice **basic OOP** in C#:
  - Define a domain model for a zoo (areas and animals).
  - Use **classes**, **interfaces**, **properties**, and **encapsulation**.
  - Demonstrate **polymorphism** (e.g., animals share behaviors/contracts via an interface).
- Build a friendly **CLI** that guides a visitor through areas → animals → fun facts.
- Ensure clean structure and defensive input handling.

---

## Requirements

### Core Features

- **Warm Welcome**
  - On start, display a greeting and a short introduction.

- **Areas**
  - The zoo must be divided into **multiple areas** (e.g., Rainforest, Savannah, Aquarium, Aviary, Desert, Mountains, Night House, etc.).
  - Present the list of areas and ask the visitor where they want to go.

- **Animals & Fun Facts**
  - Each area lists available animals.
  - The simulator must include **at least 15 distinct animals** in total (across all areas).
  - After the visitor selects an animal, display a **fun fact** about it (short and engaging).
  - Allow the visitor to **view another animal**, **switch areas**, or **exit**.

- **CLI UX**
  - Menu-driven flow with clear prompts and input validation (reject invalid or out-of-range inputs).
  - Add small touches like ASCII dividers or brief pauses to make the experience pleasant.

---

## OOP Expectations

- **Classes & Properties**
  - Represent core entities (areas, animals) using classes.
  - Use **properties** with validation when necessary (e.g., non-empty names).
  - Keep internal state encapsulated (use private fields and public properties).

- **Interfaces**
  - Define at least one **interface** that animals implement (for example, an interface that defines a method for returning fun facts).
  - Demonstrate **polymorphism** by handling different animals through that interface.

- **Modular Design**
  - Organize your code cleanly, separating concerns (domain model, CLI, data seeding, etc.).
  - There is no prescribed folder layout — you decide the structure.

> **Note:** You must design your own architecture, classes, and interfaces. Document your design choices in the README.

---

## Data & Content

- Include **at least 15 animals** spread across various areas.
- Each animal must have:
  - A **name** (common name is fine),
  - An **area** association,
  - A **fun fact** (one or more).
- You can hard-code the data or load it from a simple file.

---

## Error Handling

- Validate user input for menus and selections.
- Handle missing animals or empty areas gracefully.
- Never crash on invalid input — show an error and re-prompt.

---

## Example CLI Flow (Illustrative Only)

```
========================================
     Welcome to Aurora Zoo!
========================================
Where would you like to go today?

1) Rainforest
2) Savannah
3) Desert
4) Aviary
5) Aquarium
6) Night House
7) Mountains
8) Exit
> 1

-- Rainforest --
Animals available:
1) Jaguar
2) Capuchin Monkey
3) Poison Dart Frog
4) Ocelot
5) Macaw
> 2

Capuchin Monkey — Fun Fact:
They can use simple tools and learn from each other’s behavior.

What would you like to do next?
1) View another animal in this area
2) Go to another area
3) Exit
> 
```

*(This output is only an example; you should design your own layout and messages.)*

---

## Technical Requirements

- **Language/Framework:** C# with .NET 8.
- **Runtime:** Console app only (no GUI frameworks).
- **No external services:** Everything must run locally.
- **No external packages** required (optional is fine, if explained in the README).

---

## Git Requirements

1. Initialize a Git repository.
2. Commit in small, meaningful steps (e.g., classes, data setup, CLI loop).
3. Use descriptive, task-oriented commit messages.

---

## Evaluation Criteria (100 pts)

| Criterion                                               | Points | Description |
|---------------------------------------------------------|--------|-------------|
| OOP design (classes, interfaces, encapsulation)         | 25     | Uses well-structured classes and interfaces to model areas, animals, and shared behavior. Applies encapsulation with private fields and public properties. |
| Properties & basic validation                           | 10     | Uses C# properties with validation (e.g., non-empty names, valid values). |
| Polymorphism via interfaces (shared behavior)           | 15     | Demonstrates polymorphism using at least one interface shared by animals. |
| Areas → Animals → Fun Facts flow                        | 20     | Implements a full visitor experience from area selection to viewing animal fun facts. Includes options to switch area or explore again. |
| CLI UX (menus, prompts, error handling)                 | 15     | CLI is friendly and robust. Validates input, handles errors gracefully, and includes small UX touches (dividers, pauses). |
| Code organization (structure you designed)              | 10     | Code is cleanly organized across files/classes. Logical separation of concerns (e.g., data, domain, UI). |
| Git usage                                               | 5      | Git is used with **meaningful commit messages** and commits made in small, logical steps (e.g., class creation, CLI setup, area navigation). |

---

### Git Requirements

- ✅ Commit frequently, after major tasks (e.g., domain classes, CLI skeleton, logic for areas/animals).  
- ✅ Use **descriptive, task-based commit messages** (not just "update", "works" or "final version").  

---

### README and Usability (Required)

A separate `README.md/Markdown file` (not this instruction file) must be included. It should:

- Clearly explain what the program does.  
- Provide **step-by-step instructions on how to build and run the app** (e.g., `dotnet build`, `dotnet run`).  
- Summarize your OOP design: how classes and interfaces are used, and your reasoning behind the structure.  
- List the zoo areas and sample animals included.  
- Document any optional or bonus features implemented.  
- *(Optional)* Include a screenshot or CLI demo snippet for polish.

⚠️ **Important:** Please do not forget to include how to run the code in your README — this will be explicitly graded.

---

### Bonus (Optional)

- Multiple fun facts per animal, randomly selected.
- Ability to search/filter animals by name.
- Mark favorite animals.
- Simple save/load feature to remember last visited area or favorites.

---

## Suggested Timeline (1 Week)

- **Day 1:** Design your domain model and interfaces; outline the CLI flow.
- **Day 2:** Implement base classes, properties, and seed animal data.
- **Day 3:** Build the main CLI menu and navigation logic.
- **Day 4:** Add polish to prompts, loops, and validation.
- **Day 5:** Add optional features and refine your OOP design.
- **Day 6:** Test thoroughly and write the README.
- **Day 7:** Final review and submission.

---

## Deliverables

- **Source code** for the .NET console app.
- **README** including:
  - How to build and run the app (`dotnet build`, `dotnet run`).
  - Your design rationale (classes, interfaces, etc.).
  - The list of areas and animals included.
  - Optional or bonus features implemented.
- *(Optional)* A short demo screenshot or GIF of the CLI.
