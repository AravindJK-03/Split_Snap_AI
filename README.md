# Split Snap

Split Snap helps friends split a restaurant bill fairly. The planned workflow lets people review bill items, assign them to diners, account for taxes and charges, and copy a summary to share on WhatsApp.

This repository currently contains only the Step 1 project skeleton. Bill uploads, AI extraction, and split calculations are not implemented yet.

## Requirements

- Node.js 20+
- npm

## Run the client

```sh
cd client
npm install
npm run dev
```

The Vite development server uses `http://localhost:5180` and proxies `/api` requests to the backend on port 4000.

## Run the server

```sh
cd server
npm install
Copy-Item .env.example .env
npm run dev
```

The server listens on `http://localhost:4000`. Its health endpoint is available at `/api/health`. The environment example contains placeholders only; do not commit `.env` or put secrets in client code.
