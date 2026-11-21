# Task 3 – Campus Library Search Layout

## Problem Statement
Build a responsive campus library search screen using Swing layout managers.

## Objective
Implement nested layouts, title/search areas, expandable JTable, pagination, reservation status, and three resizing tests.

## Classes
`LibrarySearchFrame`, `LibrarySearchService`, `LibraryBook`, `LibrarySearchApp`.

## Layout
`BorderLayout` is used for the major top/center/bottom regions. `FlowLayout` retains search controls and bottom buttons. `GridLayout` is not required by the final frame but can be used for compact equal-size forms. `JScrollPane` makes the results table expand.

## Execution
```powershell
javac -d bin (Get-ChildItem src\*.java | % FullName)
java -cp bin LibrarySearchApp
```

## Resizing
Test 800x600, 1100x750, and 1400x900. The centre table must expand; search and navigation controls must remain usable.

## Complexity
Search examines n records: O(n) time and O(r) result storage. Pagination displays at most k rows: O(k) time and space.

## Screenshots
`library_800x600.png`, `library_1100x750.png`, `library_1400x900.png`.
