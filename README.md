# 👗 Dress Rental System - Server Side (REST API)

A Backend system for managing dress rentals, implemented as a modern **REST API** using **ASP.NET 9** and **C#**.  
The system was designed with emphasis on high performance, scalability, and full separation between logic and data layers.

---

## 🏗 Architecture & Project Structure

The project is built with a **3-Layer Architecture**, enabling easy maintenance, quality testing, and dependency decoupling:

1. **Application Layer (Web API)**  
   - Managing Controllers and Routing configurations  
   - Implementing Middlewares for HTTP request handling and error management  
   - Central **Dependency Injection** setup  

2. **Services Layer**  
   - Business logic layer  
   - Mediates between Controllers and Repositories  
   - Performs validations and data processing  
   - Executed **asynchronously** to free server resources  

3. **Repositories Layer**  
   - Data access using the **Repository Pattern**  
   - Uses **Entity Framework Core** with a **Database First** approach  
   - CRUD operations performed **asynchronously** for improved performance and scalability  

---

## 🛠 Technical Features & Highlights

### ⚡ Performance & Scalability
- **Asynchronous Programming:** Using `async/await` across all layers to free Threads and enable high scalability  
- **Dependency Decoupling:** Using **Dependency Injection (DI)** to create modular and flexible code  

### 🔄 Data Management & Mapping
- **DTOs (Data Transfer Objects):** DTO layer to prevent circular dependencies and separate the database from the API  
- **C# Records:** DTOs represented as `records` to ensure Immutable objects and efficient data transfer  
- **AutoMapper:** Automatic mapping between Entities and DTOs to maintain clean code  

### 📊 Monitoring, Logging & Error Handling
- **NLog:** Logging system operations and errors  
- **Error Handling Middleware:** Unified error handling and redirection to logs  
- **Auditing:** All traffic and ratings are stored in the `Rating` table for analysis and tracking  
- **Configuration:** Configurations are stored in `appsettings.json` files outside the code  

---

## 🧪 Testing

- **Unit Tests:** Isolated unit tests for services  
- **Integration Tests:** Integration tests to verify synchronization between all layers and the database  

---

## 📂 Folder Structure

```text
├── DressRental.API          # Controllers, Middlewares, AppSettings
├── DressRental.Services     # Business Logic, Interfaces, AutoMapper Profiles, DTOs
├── DressRental.Repositories # DB Context, Entities (EF), Repository Implementations
└── DressRental.Tests        # Unit & Integration Tests
```
