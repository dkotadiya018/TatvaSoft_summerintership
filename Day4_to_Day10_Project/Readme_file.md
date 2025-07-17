# Dhruv Kotadiya

👋 Hello there! Welcome to my full-stack project. Thank you for taking the time to check it out. Below are the complete instructions to run this project smoothly on your local machine. It includes both **Frontend (React)** and **Backend (.NET + PostgreSQL)** setup guides.

---

## 📁 Project Setup Guide

### 🚀 Frontend Setup (React)

1. Open the terminal and navigate to the frontend folder:
   ```bash
   cd frontend
If npm is not installed, install Node.js from the official site:
👉 https://nodejs.org

Install all necessary dependencies:

```bash
npm install

Start the React development server:

```bash
npm start


🖥️ Backend Setup (.NET Core - Visual Studio 2022)
Requirement: Visual Studio Community 2022 with .NET 7 SDK and Entity Framework Core Tools

Open the Mission.sln file in Visual Studio 2022.

Set Mission.Api as the startup project.

Open the terminal inside Visual Studio (or use CMD) and run:

```bash
dotnet restore

```bash
dotnet build


Create a new PostgreSQL database manually using pgAdmin or CLI.

Example: Create a database named Mission2206


Configure PostgreSQL connection string:

Navigate to Mission.Api/appsettings.Development.json

Replace the existing connection string with the one matching your PostgreSQL setup:

json
Copy
Edit
"ConnectionStrings": {
  "DefaultConnection": "Host=localhost;Port=5432;Database=Mission2206;Username=postgres;Password=postgres;Search Path=public"
}


🔐 Default Admin Configuration
Open the MissionDbContext.cs file in Mission.Entities project.

Modify the default admin user details as per your requirement (for example: email, username, or role if predefined in seed method).

🧱 Database Migration & Update
Open terminal in the solution root directory and run the following commands:

```bash
dotnet ef migrations add InitialCreate --project Mission.Entities --startup-project Mission.Api

```bash
dotnet ef database update --project Mission.Entities --startup-project Mission.Api


Make sure the dotnet-ef tool is installed. If not, install it with:


```bash
dotnet tool install --global dotnet-ef


▶️ Run the Backend API Server

```bash
dotnet run --project Mission.Api