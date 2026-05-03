# Computer Security Lab

This organization groups related CTF and dashboard repositories by year and purpose.

## Repository Naming Pattern

- `Lab2026`: Contains source files, assets, and configuration for the CTF event conducted in 2026.
- `Lab<year>`: Each year has its own repository for that years CTF files and materials.

## What Each Repository Holds

### `Lab2026`
- Contains the files related to the CTF event for 2026.
- This includes challenge materials, write-ups, event configuration, and any other CTF-specific resources.

### `Dashboard`
- The `Dashboard` repository holds the web dashboard for the event.
- `main` branch: a simple static website built with Flask for easy deployment.
- `react` branch: frontend-only React code for a more modern frontend.

### `Dashboard-backend`
- When using the `Dashboard` frontend from the `react` branch, the backend API is provided by the separate `Dashboard-backend` repository.
- `Dashboard-backend` is implemented with Strapi and serves the data for the React frontend.

## Recommended Setup

- For a lightweight deployment or demo: use `Dashboard` on the `main` branch.
- For a proper frontend/backend architecture: use `Dashboard` on the `react` branch for the frontend and `Dashboard-backend` for the backend.

## Backend Credentials

- Do not store credentials in source control.
- Put backend secrets and credentials in environment variables, a `.env` file excluded from version control, or a secure secret manager.
- For example, store any `Dashboard-backend` admin/API credentials in the backend repository's `.env` or in a secure vault, not in `Dashboard` source files.

## Backend Database

- `Dashboard-backend` is configured with PostgreSQL.
- Store database connection details in the backend environment configuration, not in source code.
- Use a `.env` file with PostgreSQL settings, or configure the database in a secrets manager/hosting provider vault.

## Summary

- `Lab2026` = CTF event files for 2026.
- `Dashboard` = dashboard website repository.
- `Dashboard` main branch = static Flask site.
- `Dashboard` react branch = React frontend only.
- `Dashboard-backend` = backend API for the React frontend.
- Store credentials securely outside the repository.
