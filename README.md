```
# 📘 DemoFirst Setup Cheatsheet

## Project Structure
DemoFirst/
 ├── client/       # React frontend
 └── server/       # .NET backend
      ├── server.sln
      ├── dataaccess/
      │     └── dataaccess.csproj
      └── service/
            └── service.csproj

## 1️⃣ Create the frontend (React with Vite)
mkdir client
cd client
npm create vite@latest
cd ..

# Explanation:
# - mkdir client → create folder for frontend
# - cd client → go inside it
# - npm create vite@latest → generate a Vite React project
# - cd .. → back to root

## 2️⃣ Create the backend solution
mkdir server
cd server
dotnet new gitignore
dotnet new sln

# Explanation:
# - mkdir server → create backend folder
# - cd server → go inside
# - dotnet new gitignore → generate .NET .gitignore
# - dotnet new sln → create solution file

## 3️⃣ Create backend projects
mkdir dataaccess service
cd dataaccess
dotnet new classlib
cd ../service
dotnet new console
cd ..

# Explanation:
# - mkdir dataaccess service → make 2 subfolders
# - dotnet new classlib → create class library project
# - dotnet new console → create console app project
# - cd .. → return to server root

## 4️⃣ Add projects to the solution
dotnet sln add dataaccess/dataaccess.csproj
dotnet sln add service/service.csproj

# Explanation:
# - dotnet sln add → register projects inside the solution
```
