# Task 2 – Hospital Appointment Desk

## Problem Statement
Convert outpatient appointment requirements into an event-driven Swing design and working application.

## Objective
Demonstrate component containment, event tables, department-dependent doctors, validation, booking, dialogs, and window methods.

## Classes
`HospitalAppointmentApp`.

## Event and Component Design
Department and doctor controls use item/action events. Date uses `JSpinner`. Booking and clear use `ActionListener`; opening uses constructor/setVisible; closing uses Swing's default close operation and window events.

## Implementation
Doctors are cached in a `Map<String,List<String>>`. Changing department refreshes the doctor combo. Patient ID, name, phone, department, doctor, and date are checked before confirmation. A local set prevents duplicate bookings for the simulated session.

## Complexity
Doctor refresh is O(d), where d is the doctors in one department. Map lookup is average O(1). Booking duplicate lookup is average O(1). Rendering confirmation is O(k).

## Execution
```powershell
javac -d bin (Get-ChildItem src\*.java | % FullName)
java -cp bin HospitalAppointmentApp
```

## Evidence
Capture appointment window, department refresh, validation error, and booking confirmation.
