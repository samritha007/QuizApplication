# JDBC Quiz Application

A Java console application using JDBC and Oracle Database to store and manage quiz results.

## Features

- Insert quiz results
- Store student ID, quiz name, total questions, and score
- Calculate percentage automatically
- Display the highest score
- List students scoring above 80%
- Display all quiz attempts

## Technologies

- Java 25
- JDBC
- Oracle Database Free
- Oracle JDBC Driver

## Database Table

The application automatically creates the `QUIZ_RESULTS` table with the following columns:

- ID
- STUDENT_ID
- QUIZ_NAME
- TOTAL_QUESTIONS
- SCORE
- PERCENTAGE

## Compile and Run

Place the Oracle JDBC driver inside the `lib` folder.

For example:

```text
lib/ojdbc17.jar
```

Compile:

```powershell
javac -cp ".;lib/ojdbc17.jar" QuizApplication.java
```

Before running, set the Oracle database password:

```powershell
$env:QUIZ_DB_PASSWORD="your_password"
```

Run:

```powershell
java -cp ".;lib/ojdbc17.jar" QuizApplication
```

## Application Menu

```text
1. Add Quiz Result
2. Display Highest Score
3. Display Results Above 80%
4. Display All Results
5. Exit
```

## Database Connection

The application connects to the Oracle `FREEPDB1` database using the `QUIZUSER` account.

The database password is stored as an environment variable and is not included in the source code.