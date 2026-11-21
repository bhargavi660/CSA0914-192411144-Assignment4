# CSA09-192411144-Assignment4

**Student:** Bhargavi N.  
**Register Number:** 192411144  
**Course:** Programming in Java (CSA09)  
**Assignment:** Assignment 4 – CO4, Event-Driven GUI Design

## Environment
- Java 26.0.2.1 and `javac` verified.
- Maven was not installed; direct `javac` instructions are provided below.
- MySQL and MySQL client were not installed or available on `PATH` during compilation.
- MySQL Connector/J 9.4.0 is stored in `Task06/lib/` for JDBC compilation.

## Technologies
Java Swing, AWT, JDBC, MySQL Connector/J, MySQL, Maven configuration, Mermaid documentation.

## Structure
Each `Task01` through `Task06` folder contains independent source code, documentation, and screenshot folders. Task 6 additionally contains SQL and database configuration examples.

## Compile and Run
Open a Windows PowerShell at the workspace root.

```powershell
javac -d Task01\bin (Get-ChildItem Task01\src\*.java | % FullName)
java -cp Task01\bin FeePaymentApp
```

Repeat:
```powershell
javac -d Task02\bin (Get-ChildItem Task02\src\*.java | % FullName)
java -cp Task02\bin HospitalAppointmentApp

javac -d Task03\bin (Get-ChildItem Task03\src\*.java | % FullName)
java -cp Task03\bin LibrarySearchApp

javac -d Task04\bin (Get-ChildItem Task04\src\*.java | % FullName)
java -cp Task04\bin DrawingPadApp

javac -d Task05\bin (Get-ChildItem Task05\src\*.java | % FullName)
java -cp Task05\bin CurrencyConverterActionListener
java -cp Task05\bin CurrencyConverterInnerClass
java -cp Task05\bin CurrencyConverterAnonymous
java -cp Task05\bin CurrencyConverterLambda
```

Task 6:
```powershell
javac -cp Task06\lib\mysql-connector-j-9.4.0.jar -d Task06\bin (Get-ChildItem Task06\src\*.java | % FullName)
java -cp "Task06\bin;Task06\lib\mysql-connector-j-9.4.0.jar" Main
```

## MySQL Setup
1. Install and start MySQL.
2. Execute `Task06/sql/campus_event_registration.sql`.
3. Copy `Task06/config/database.properties.example` to `Task06/config/database.properties`.
4. Replace the example user and password with local credentials. The real file is ignored by Git.
5. Run Task 6.

The demonstration committee account is intentionally a placeholder hash; replace it and the login implementation with a real password-hash library for production use.

## Execution Status
- Tasks 1–5: source compiled successfully with Java 26.
- Task 6: source compiled successfully with Connector/J 9.4.0.
- GUI launch and MySQL integration could not be verified in this environment because no interactive desktop/MySQL service was available; exact launch steps and screenshots are provided.

## Submission
No Git remote or GitHub URL was created. After review, initialize and publish with:
```powershell
git init
git add .
git commit -m "Complete Java Assignment 4"
git branch -M main
git remote add origin https://github.com/<username>/CSA09-192411144-Assignment4.git
git push -u origin main
```
