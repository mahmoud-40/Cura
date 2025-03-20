# Cura - Virtual Health Assistant

Cura is a Virtual Health Assistant powered by Generative AI. It helps users manage their medication schedules, receive reminders, and get AI-powered medical assistance through an interactive chatbot. The project is developed by **Team Nexus** for **SalamHack 2025**.

## Project Structure

The Cura project is divided into four main parts:

- **Cura.API** - The backend API built using ASP.NET Core (Runs on port **5164**).
- **Cura.AiModel** - AI model responsible for chatbot responses and medical assistance (Runs on port **8080**).
- **Cura.Flutter** - The mobile application built using Flutter.
- **Cura.UI** - Screenshots and design references for the application.

## Features

- AI-powered chatbot for medical assistance.
- Medication reminders and notifications.
- Secure user authentication and role management.
- Future enhancements: chat saving, appointment booking, and more.

## Demo

https://github.com/user-attachments/assets/93ca4641-6d36-45eb-bdc3-cc6110407d9c

## API Endpoints

### Notification
- `GET /api/Notification/{userId}` - Get user notifications.
- `DELETE /api/Notification/{userId}` - Delete user notifications.
- `PUT /api/Notification/{notificationId}` - Mark a notification as read.
- `POST /api/Notification` - Send a notification.

### Message
- `POST /api/Message/send` - Send a message to the AI model.

## UI/UX Design

The UI design is available on **[Figma](https://www.figma.com/design/YelgBTpdxbwS7nmAHuGUvX/Slack?node-id=0-1&t=KEl2cCTIPInWkBhB-1)**.
A screenshot of the design is also available in `Cura.UI`.

## Database

The **Entity Relationship Diagram (ERD)** is available in `Cura.API` (ERD.png). The database schema is implemented using SQL Server, and will be optimized further when new features are added (e.g., saving chats).

## Mobile Application

An APK file (`CuraApp.apk`) is available in `Cura.Flutter` for testing the mobile application.

## Requirements

### API
- .NET 7 or later
- SQL Server
- Entity Framework Core

#### Required NuGet Packages
Before running the API, install the following NuGet packages:
```sh
 dotnet add package AutoMapper.Extensions.Microsoft.DependencyInjection
 dotnet add package Microsoft.AspNetCore.Identity.EntityFrameworkCore
 dotnet add package Microsoft.EntityFrameworkCore
 dotnet add package Microsoft.EntityFrameworkCore.Design
 dotnet add package Swashbuckle.AspNetCore
 dotnet add package Swashbuckle.AspNetCore.Annotations
 dotnet add package Microsoft.EntityFrameworkCore.SqlServer
 dotnet add package Microsoft.EntityFrameworkCore.Proxies
```

### AI Model
- Python 3
- Required dependencies are listed in `requirements.txt` inside `Cura.AiModel`

### Flutter Application
- Flutter SDK

## How to Run

### Backend (Cura.API) - Runs on port **5164**
1. Navigate to `Cura.API` directory.
2. Update `appsettings.json` with your SQL Server connection string.
3. Install required NuGet packages using:
   ```sh
   dotnet restore
   ```
4. Apply database migrations:
   ```sh
   dotnet ef database update
   ```
5. Start the API:
   ```sh
   dotnet run
   ```

### AI Model (Cura.AiModel) - Runs on port **8080**
1. Navigate to `Cura.AiModel` directory.
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Run the AI server:
   ```sh
   python main.py
   ```

### Flutter App (Cura.Flutter)
1. Navigate to `Cura.Flutter` directory.
2. Install dependencies:
   ```sh
   flutter pub get
   ```
3. Run the app:
   ```sh
   flutter run
   ```
4. **Alternatively, install and test the APK (`CuraApp.apk`) directly.**

---

## Team Nexus
- **Mahmoud Abdulmawlaa** - Backend Engineer
- **Ahmed Waleed** - AI Engineer
- **Rana Mohy** - Flutter Developer
- **Menna Fathy** - UI/UX Developer
- **Shahd Gomma** - Business Developer

