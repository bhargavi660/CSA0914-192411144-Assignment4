# Task 5 – Currency Converter Event Styles

## Problem Statement
Implement one converter using four event-handling approaches.

## Implementations
- `CurrencyConverterActionListener`
- `CurrencyConverterInnerClass`
- `CurrencyConverterAnonymous`
- `CurrencyConverterLambda`

All use demonstration USD-based rates and are not live financial rates.

## Supported Events
Convert button, Enter in amount field, clear button, invalid/zero/negative amounts, same-currency conversion, result label, result dialog, and WindowAdapter closing confirmation.

## Execution
```powershell
javac -d bin (Get-ChildItem src\*.java | % FullName)
java -cp bin CurrencyConverterActionListener
java -cp bin CurrencyConverterInnerClass
java -cp bin CurrencyConverterAnonymous
java -cp bin CurrencyConverterLambda
```

## Complexity
Conversion uses constant-time map lookup and arithmetic: O(1) time and O(1) space. Parsing a text input is O(n) in input length.

## Screenshots
Capture each version plus valid conversion, invalid amount, clear, and result dialog.
