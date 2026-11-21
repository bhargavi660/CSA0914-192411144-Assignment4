# Task 4 – Drawing Pad Event Forensics

## Problem Statement
Create a drawing pad that stores mouse positions and redraws dots consistently.

## Objective
Use `MouseAdapter`, `ArrayList<Point>`, `repaint()`, and `paintComponent()` while explaining incorrect handlers and repaint failures.

## Classes
`DrawingPadFrame`, `DrawingPanel`, `DrawingPadApp`.

## Implementation
Every click appends `MouseEvent.getPoint()` to an `ArrayList<Point>` and calls `repaint()`. `paintComponent()` first invokes `super.paintComponent()` and then redraws every dot.

## Why @Override Matters
`@Override` ensures the method signature exactly matches a listener callback. A misspelled or wrong-signature method will fail compilation, preventing the silent “handler never executes” defect.

## Comparison
Stored points preserve a simple vector representation and use O(n) memory. A `BufferedImage` requires width*height pixels, but is often faster for many static paints. Points suit this small click-only pad.

## Execution
```powershell
javac -d bin (Get-ChildItem src\*.java | % FullName)
java -cp bin DrawingPadApp
```

## Test
Open, click, confirm dot and counter updates, minimise, restore, and confirm dots remain.

## Evidence
`drawing_before_minimize.png`, `drawing_after_restore.png`.
