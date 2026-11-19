# SmartStudyPlanner (team version)

A study planner built as a team project in Blazor (ASP.NET Core, .NET 8). Students register, log in, create subjects, and add, edit and track study tasks for each subject.

This repository is my fork of the team repository, [Nehiz/SmartStudyPlanner](https://github.com/Nehiz/SmartStudyPlanner). My own rebuilt version, which schedules the work automatically and runs entirely in the browser, is [hlaolil/SmartStudyPlanner](https://github.com/hlaolil/SmartStudyPlanner) ([live](https://smart-study-planner-opal.vercel.app)).

## Features

- **Accounts:** registration, login and logout with ASP.NET Core Identity, using a custom `User` model and password rules. See [AUTHENTICATION_SETUP.md](AUTHENTICATION_SETUP.md).
- **Subjects:** each user creates their own study subjects (`/planner/subjects`).
- **Tasks:** add, edit and track tasks within a subject (`/planner`, `/planner/add`, `/planner/edit/{id}`).
- **Data:** Entity Framework Core with SQLite. Deleting a user also deletes their subjects and tasks.

## Run it locally

Requires the [.NET 8 SDK](https://dotnet.microsoft.com/download).

```bash
dotnet run
```

The database file (`SmartStudyPlanner.db`) is created on first run; its connection string is in `appsettings.json`.

## Deployment

`.github/workflows/main_smartstudyplanner1.yml` builds the app and deploys it to an Azure Web App on every push to `main`.
