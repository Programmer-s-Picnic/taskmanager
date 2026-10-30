# Programmer's Picnic Task Manager · Node.js from 0 to Infinity

Live frontend (when GitHub Pages is enabled): https://programmer-s-picnic.github.io/taskmanager/

Full course: https://programmer-s-picnic.github.io/taskmanager/learn/

GoDaddy Node.js backend source: https://github.com/Programmer-s-Picnic/nodeuse

Intended GoDaddy hosting hostname: `cserver.learnwithchampak.live`

## Architecture

- **This repository** hosts the static GitHub Pages frontend: Dashboard, Task Entry, All Tasks, and a guided 0 → ∞ tutorial.
- **nodeuse** is the standalone GoDaddy Node.js server (Hello World, JSON API, health check, CORS).
- The frontend's Connect & test panel starts with `https://cserver.learnwithchampak.live` as a **suggested, unverified** base address. It only reports success when the server returns our expected Hello World response.
- Tasks currently use browser `localStorage`, and **are not stored or shared by the backend**. Do not use localStorage as a multi-device task service.

## Start the website

You can simply open `index.html` or serve the repository with any static file server.

For GitHub Pages, enable **Settings → Pages → Deploy from a branch → main / (root)** if Pages is not already enabled. Relative URLs are compatible with the repository subpath `/taskmanager/`.

## Node.js connection

1. Deploy the **nodeuse** repository, not this frontend repository, through GoDaddy Node.js Apps.
2. Preview and publish your GoDaddy app to a real public HTTPS URL.
3. Open the Task Manager dashboard or the course's live lab.
4. Enter the **published** app URL and click **Connect & test**.
5. If the app is published at `https://cserver.learnwithchampak.live`, you can use that as the base URL.

If the server is mapped to another subdomain or a path, use that exact published app URL. CORS must allow the GitHub Pages origin `https://programmer-s-picnic.github.io` (without a path).

## Navigation

- `/index.html` — dashboard, live test, local task entry
- `/task_entry/index.html` — create or edit a local task
- `/all_task/index.html` — list, search, filter and update local tasks
- `/learn/index.html` — 13-chapter Node.js 0-to-Infinity course

## Security notes

The browser frontend contains no GoDaddy credentials. Avoid placing passwords in GitHub Pages. The current GoDaddy backend does not expose task write endpoints; future database-backed task APIs must validate user identity, authorization and inputs.

Developed and maintained by Champak Roy.
