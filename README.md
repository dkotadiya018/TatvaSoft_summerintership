#DHRUV

# 🔐 Login Page with PostgreSQL + EF Core + Visual Studio (by Dhruv)

## Extract this zip file and open with visual studio communnity 2022

## 📘 Overview

This project is a .NET Core Web API application built to demonstrate a **Login Page** integrated with a **PostgreSQL database**, using **Entity Framework Core**.  
It supports real-time database updates viewable via **DBeaver** and is developed in **Visual Studio Community Edition**.

---

## 📦 Tech Stack

- ASP.NET Core Web API  
- Entity Framework Core  
- PostgreSQL (with Npgsql)  
- DBeaver (GUI for PostgreSQL)  
- Visual Studio 2022+

---

## 📂 Project Structure

#🔌 Configure Connection String
#Edit Mission.Api/appsettings.json:

#json
#Copy
#Edit
"ConnectionStrings": {
  "DefaultConnection": "Host=localhost;Port=5432;Database=missiondb;Username=postgres;Password=your_password"
}


# If EF tools not installed
dotnet tool install --global dotnet-ef

# Apply migrations
dotnet ef database update --project Mission.Entities --startup-project Mission.Api
