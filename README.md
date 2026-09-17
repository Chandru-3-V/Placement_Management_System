
# Placement Management System

A mini CRUD-based web application built for the VSB Skill Vault "Mini Web Application" activity.

## What it does

The app lets a placement cell manage student placement records with full **Create, Read, Update, and Delete (CRUD)** functionality:

- **Create** — add a new student placement record through a validated form
- **Read** — view all records in a sortable table, with live search and status filtering
- **Update** — edit any existing record; changes save immediately
- **Delete** — remove a record with a confirmation prompt

It also shows a small live dashboard (total students tracked, number placed, placement rate, average package) that updates automatically as records change.

## Technology used

- **HTML, CSS, JavaScript** — single self-contained file, no build step or server required
- **Browser Local Storage** — acts as the persistent data store, so records survive a page refresh or browser restart on the same device/browser

This keeps the project easy to run and demonstrate anywhere, while still implementing every CRUD operation, client-side validation, search/filter, and a responsive layout, as required by the activity guidelines.

## How to run it

1. Double-click `placement-management-system.html` (or open it from your browser with **File → Open**).
2. No installation, server, or internet connection is required to use the app.
3. Start adding, editing, and deleting placement records right away.

> Note: data is stored locally in that specific browser. Opening the file in a different browser, or clearing browser storage, will not carry records over. To reset the app to its original sample data, clear your browser's local storage for the file or open it in a private/incognito window.

## Fields tracked per student

| Field | Notes |
|---|---|
| Student name | required |
| Register number | required, must be unique |
| Department | required, dropdown |
| CGPA | required, 0–10 |
| Email | required, validated format |
| Company | optional, filled once a drive result is known |
| Package (LPA) | optional, numeric |
| Status | Not Placed / In Process / Placed |

## Validation implemented

- Required-field checks for name, register number, department, CGPA, email, and status
- Duplicate register number prevention
- CGPA range check (0–10)
- Email format validation
- Non-negative numeric check on package
- Inline error messages shown under each invalid field

## Files in this submission

- `placement-management-system.html` — the working application
- `Placement_Management_System_Report.docx` — project report
- `README.md` — this file

## Possible future enhancements

- Move data storage to a real backend (Django REST Framework or Spring Boot) with a MySQL/PostgreSQL database
- Add authentication for placement-cell staff
- Add CSV/Excel export of placement records
- Add pagination for large batches of students
