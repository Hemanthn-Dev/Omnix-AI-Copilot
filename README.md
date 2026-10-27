# Omnix AI Copilot

A Java and Spring Boot AI chat application with a JSP interface, MySQL persistence, and Google Gemini API integration.

## Features

- AI-powered chat responses through the Gemini API
- Conversation/session management and chat history
- Spring Boot backend with JSP, HTML, CSS, and JavaScript
- MySQL persistence through Spring Data JPA
- Maven build and automated tests

## Tech stack

- Java 17
- Spring Boot
- JSP, HTML, CSS, JavaScript
- Spring Data JPA and MySQL
- Google Gemini API
- Maven

## Project structure

The Spring Boot application is in `ai-copilot/`.

## Prerequisites

- JDK 17
- MySQL
- A Google Gemini API key from Google AI Studio
- Maven (or use the included Maven Wrapper)

## Configuration

The app reads credentials from environment variables. Do not commit API keys or database passwords.

Required environment variables:

| Variable | Purpose | Example |
| --- | --- | --- |
| `GEMINI_API_KEY` | Google Gemini API key | Set your own key locally |
| `DB_URL` | JDBC connection URL | `jdbc:mysql://localhost:3306/copilot` |
| `DB_USERNAME` | MySQL username | `root` |
| `DB_PASSWORD` | MySQL password | Set your own password |
| `SERVER_PORT` | Optional HTTP port | `8080` |

Create a MySQL database named `copilot` before starting the application.

### Windows PowerShell example

Set these values in the terminal where you will run the app. Replace the example values with your own secrets:

```powershell
$env:GEMINI_API_KEY = "YOUR_NEW_GEMINI_API_KEY"
$env:DB_URL = "jdbc:mysql://localhost:3306/copilot"
$env:DB_USERNAME = "root"
$env:DB_PASSWORD = "YOUR_MYSQL_PASSWORD"
```

Do not paste real secrets into README files, source code, screenshots, issues, or commits.

## Run the application

From the repository root:

```powershell
cd ai-copilot
.`mvnw.cmd` spring-boot:run
```

If Maven is installed globally, you can use:

```powershell
mvn spring-boot:run
```

Open [http://localhost:8080/chat](http://localhost:8080/chat).

## Run tests

From `ai-copilot/`:

```powershell
.`mvnw.cmd` test
```

The test configuration is set up to use an in-memory H2 database where configured.

## Screenshots

![Omnix Chat Interface](https://github.com/user-attachments/assets/9bb4812f-18ab-4834-b68d-5426d69adfde)

![Session Management](https://github.com/user-attachments/assets/8e765c39-1ab2-459e-974d-6c2b1bddddf5)

![Chat History](https://github.com/user-attachments/assets/df3061ae-18de-4f12-9972-e2fafdec2384)

![Auto Rename Feature](https://github.com/user-attachments/assets/358a4e08-c647-4f92-9eb9-6d147c9afcb8)

## Security note

If a credential was ever committed to this public repository, rotate or revoke it immediately. Removing it from the latest version does not remove it from Git history.
