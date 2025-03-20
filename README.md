# Cura - Virtual Health Assistant

Cura is a Virtual Health Assistant powered by Generative AI. It helps users manage their medication schedules, receive reminders, and get AI-powered medical assistance through an interactive chatbot. The project is developed by **Team Nexus** for **SalamHack 2025**.

## Project Structure

The Cura project is divided into four main parts:

- **Cura.API** - The backend API built using ASP.NET Core.
- **Cura.AiModel** - AI model responsible for chatbot responses and medical assistance.
- **Cura.Flutter** - The mobile application built using Flutter.
- **Cura.UI** - Screenshots and design references for the application.

## Features

- AI-powered chatbot for medical assistance.
- Medication reminders and notifications.
- Secure user authentication and role management.
- Future enhancements: chat saving, appointment booking, and more.

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

### AI Model
- Python 3
- Required dependencies are listed in `requirements.txt` inside `Cura.AiModel`

### Flutter Application
- Flutter SDK

## How to Run

### Backend (Cura.API)
1. Navigate to `Cura.API` directory.
2. Update `appsettings.json` with your SQL Server connection string.
3. Run the following command to apply migrations:
   ```sh
   dotnet ef database update
   ```
4. Start the API:
   ```sh
   dotnet run
   ```

### AI Model (Cura.AiModel)
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

---

## Team Nexus
- **Mahmoud Abdulmawlaa** - Backend Engineer
- **Ahmed Waleed** - AI Engineer
- **Rana Mohy** - Flutter Developer
- **Menna Fathy** - UI/UX Developer
- **Shahd Gomma** - Business Developer

