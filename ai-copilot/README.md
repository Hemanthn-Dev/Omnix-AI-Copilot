# Omnix AI Copilot

Spring Boot chat application with a JSP frontend, Spring Data JPA, MySQL, and Google Gemini API integration.

## Prerequisites

- JDK 17
- MySQL with a database named `copilot`
- A newly generated Gemini API key
- Maven, or use the included Maven Wrapper

## Configure environment variables

The application reads these environment variables and does not require secrets to be stored in source files:

- `GEMINI_API_KEY`: your Gemini API key
- `DB_URL`: JDBC URL, for example `jdbc:mysql://localhost:3306/copilot`
- `DB_USERNAME`: MySQL username
- `DB_PASSWORD`: MySQL password
- `SERVER_PORT`: optional, defaults to `8080`

On Windows PowerShell, set them in the terminal you will use to start the app:

```powershell
$env:GEMINI_API_KEY = "YOUR_NEW_GEMINI_API_KEY"
$env:DB_URL = "jdbc:mysql://localhost:3306/copilot"
$env:DB_USERNAME = "root"
$env:DB_PASSWORD = "YOUR_MYSQL_PASSWORD"
```

Use your own values. Never commit real credentials.

## Run

From this directory:

```powershell
.`mvnw.cmd` spring-boot:run
```

Or, if Maven is installed:

```powershell
mvn spring-boot:run
```

Open [http://localhost:8080/chat](http://localhost:8080/chat).

## Tests

```powershell
.`mvnw.cmd` test
```

The test profile uses H2 when the test configuration is active.
