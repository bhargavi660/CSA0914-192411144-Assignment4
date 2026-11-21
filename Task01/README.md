# Task 1 – Fee-Payment GUI Design Review

## Problem Statement
Analyze a poor fee-payment design and implement a corrected event-driven Swing application.

## Objective
Separate UI, validation, simulated payment, and receipt generation; use dedicated event handlers and input validation.

## Design Approach
`FeePaymentFrame` owns components and user interaction only. `FeeValidator` validates strings and amounts. `FeeService` processes a simulated payment. `PaymentResult` carries success data. `ReceiptService` formats a receipt.

## Classes
`FeePaymentFrame`, `FeeService`, `FeeValidator`, `PaymentResult`, `ReceiptService`, `FeePaymentApp`.

## Implementation
The Pay, Reset, Receipt, and Exit buttons have separate lambda handlers. Invalid input produces inline status text and an error dialog. No database or real financial transaction is used.

## Design Problems
A shared listener becomes ambiguous with growth, combines unrelated actions, and creates tight coupling. Mixing UI and logic blocks reuse and testing. String `==` compares object identity rather than text. Missing validation permits malformed input. Direct database operations block Swing and leak resources. `Thread.sleep()` freezes the Event Dispatch Thread. No feedback confuses users. Receipt logic is omitted. Concatenated SQL enables injection. Unclosed JDBC resources leak connections. Broad or silent exception handling hides useful failures.

## Comparisons
Separate listeners improve isolation and maintainability. Named or Swing `Action` objects can reuse behavior; anonymous listeners are concise but less reusable. Moving payment logic into `FeeService` permits unit testing and prevents UI state from becoming business state.

## Complexity
Per payment, validation and amount parsing are O(n) in string length and O(n) temporary string/storage space; overall typical case O(n) time and O(n) space.

## Execution
```powershell
javac -d bin (Get-ChildItem src\*.java | % FullName)
java -cp bin FeePaymentApp
```

Test valid payment, invalid/negative amount, missing name, missing ID, reset, receipt, and exit.

## Screenshot Checklist
`fee_payment_window.png`, `payment_success.png`, `validation_error.png`, `payment_receipt.png`.
