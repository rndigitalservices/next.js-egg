# Next.js Pelican & Pterodactyl Egg

A professional **Next.js egg** for both **Pelican** and **Pterodactyl** game panels,

The eggs are optimized for **all current Next.js versions** and are ready to use as a
template for hosting production-grade Next.js applications.

## Features

- Supports all current Next.js versions.
- Clean production build using `next build` and `next start`.
- Works with both Pelican and Pterodactyl panels.
- Separate eggs for each panel for easy management.
- Structured for Git-based deployments or uploaded project files.

## Folder structure

- `pelican/`  
  Contains all **Pelican eggs**.  
  Import these JSON files into the Pelican panel via the Eggs/Import interface.
- `pterodactyl/`  
  Contains all **Pterodactyl eggs**.  
  Import these JSON files into the Pterodactyl panel via the Nests → Import Egg interface.

## Requirements

- A running Pelican or Pterodactyl panel installation.
- Docker/Wings configured according to the panel documentation.
- A valid Next.js project with at least:
  - `package.json`
  - `pages/` or `app/` directory

## How to use (Pelican)

1. Open your Pelican admin area and go to **Eggs**.
2. Click **Import** and choose:
   - **From file**: select the JSON from the `pelican/` folder in this repo; or
   - **From URL**: paste the raw URL to the JSON file hosted from this repo.
3. Assign the egg to the desired Nest.
4. Create a new server and select the imported Next.js egg.
5. Point the server to your Next.js project files (Git repo or uploaded files).
6. Start the server; Pelican will install dependencies and run the app.

## How to use (Pterodactyl)

1. Open your Pterodactyl admin area and go to **Nests** → **Eggs**.
2. Click **Import Egg** and upload a JSON from the `pterodactyl/` folder.
3. Confirm the Nest and save the new egg.
4. Create a new server and select the imported Next.js egg.
5. Provide your Next.js project (Git or upload).
6. Start the server to build and run the Next.js application.

## Environment variables

Common variables you might want to configure:
- `NODE_ENV` – usually set to `production`.
- `NEXT_TELEMETRY_DISABLED` – set to `1` to disable telemetry (optional).
- Any custom env vars required by your Next.js app (API keys, database URLs, etc.).

Set these variables in the panel’s server configuration before starting the server.

## Credits

Banner design and eggs created by **RN Digital Services**.  
Feel free to fork, adapt, and contribute improvements.
