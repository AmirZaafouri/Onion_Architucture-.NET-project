# Project Name

## 📖 Project Overview
This solution follows the **Onion Architecture** principle to ensure a clean separation of concerns, better maintainability, and future scalability. The project is structured around a **Domain-Driven Design** where the core business logic is independent of frameworks and external technologies.

The solution contains:
- **Core Project**: Domain entities and interfaces
- **Infrastructure Project**: Handles database access (Entity Framework Core)
- **Application Project**: Business rules and services
- **Web Project**: ASP.NET Core MVC project that consumes services and presents data through Views and Controllers

## 🛠 Setup and Configuration
### Database Setup
- Database connection configured using Entity Framework Core
- Migrations were created and applied to generate database tables (`Add-Migration`, `Update-Database`)
- Database connection strings are stored in `appsettings.json`

### Web Project Setup
- ASP.NET Core MVC project added to the solution
- Views (Index, Create, Edit, Delete, Details) auto-generated using Scaffolded Items
- Controllers and views generated for CRUD operations on database entities

## 🧱 Architecture: Why Onion Architecture?
| Layer              | Components                                                                 |
|---------------------|---------------------------------------------------------------------------|
| **Core**           | Entities, Interfaces                                                     |
| **Application**    | Service interfaces, DTOs, business rules                                 |
| **Infrastructure** | Repositories, Database Context (EF Core)                                 |
| **Presentation**   | ASP.NET Core MVC UI, communicates with Application Layer                 |

### 🔥 Key Benefits
- **Decoupled Code**: Clear layer responsibilities, no direct infrastructure-core dependencies
- **Testability**: Business logic can be unit-tested independently
- **Flexibility**: Easy to swap UI frameworks or databases
- **Maintainability**: Simplified feature additions without system breakage

## 📂 Solution Structure
/Solution
│
├── Core
│ └── Entities/
│ └── Interfaces/
│
├── Application
│ └── Services/
│ └── DTOs/
│
├── Infrastructure
│ └── Data/
│ └── Repositories/
│
├── Web (ASP.NET Core MVC)
│ └── Controllers/
│ └── Views/
│ └── Entity/ (Index.cshtml, Create.cshtml, Edit.cshtml, etc.)
│ └── wwwroot/
│ └── Program.cs
│ └── Startup.cs
│
└── README.md

## 🚀 How to Run the Project
1.Clone the repository.

2.Update the appsettings.json connection string.

3.Run Update-Database if needed.

4.Launch the Web project as the startup project.

5.Access the web UI to view, create, edit, and delete data.


## 🔗 Technologies Used
• .NET Core

• ASP.NET Core Razor Pages

• Entity Framework Core

• SQL Server

• Onion Architecture


