Backend Structure of Sport Event Manager
The backend of the Sport Event Manager application is organized into three distinct layers:

EventPlannerAPI:

Purpose: Serves as the main entry point for the application, handling HTTP requests and routing them to the appropriate services and controllers.
Key Dependencies:
Microsoft.AspNetCore.Authentication.JwtBearer: Provides JWT (JSON Web Token) authentication, ensuring secure user access to the API.
Microsoft.AspNetCore.Identity: Manages user authentication and authorization.
Microsoft.EntityFrameworkCore.Tools: Includes tools for Entity Framework Core, aiding in database migrations and schema management.
BusinessLayer:

Purpose: Contains the core business logic and service implementations. It acts as an intermediary between the Data Access Layer and the API controllers.
Key Dependencies:
AutoMapper.Extensions.Microsoft.DependencyInjection: Simplifies object-object mapping, transforming data transfer objects (DTOs) into domain models and vice versa.
MailKit and MimeKit: Used for email functionalities, allowing the application to send and process emails.
Serilog.AspNetCore: Implements logging, providing structured logging capabilities to track and diagnose application behavior.
DataAccessLayer:

Purpose: Manages data persistence and retrieval, interacting directly with the database.
Key Dependencies:
EntityFrameworkCore: An ORM (Object-Relational Mapper) framework that facilitates database operations using .NET objects.
Microsoft.EntityFrameworkCore.SqlServer: Provides SQL Server database provider functionality for Entity Framework Core.
Microsoft.EntityFrameworkCore.Design: Supports design-time features like scaffolding, which is useful for creating database schemas.
Microsoft.AspNetCore.Identity.EntityFrameworkCore: Integrates ASP.NET Core Identity with Entity Framework Core, handling user-related data operations.
Summary
The backend is organized into three layers to ensure a clean separation of concerns:

EventPlannerAPI handles the API endpoints and routing.
BusinessLayer contains the business logic and services.
DataAccessLayer manages data operations and interactions with the database.
This layered architecture enhances maintainability, scalability, and testability by clearly separating different aspects of the application.
