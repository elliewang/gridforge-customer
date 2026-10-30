# GridForge Customer Energy Portal — Static GitHub Pages Demo

A responsive, **fully static**, customer-facing energy service portal and rule-based assistant designed as an independent engineering portfolio project inspired by modern energy utility experiences.

> **Independent demonstration:** Not affiliated with, authorized by, or endorsed by Constellation. All customer identity, accounts, usage readings, bills, service tickets, and support workflows are synthetic. No live customer services or payments are provided.

## Features

- Customer dashboard with billing, usage, efficiency and service request metrics
- Visual monthly energy-use chart (static example readings)
- Billing center, cost breakdown, and CSV export of a **sample** statement
- Service requests that can be created and viewed; saved in browser localStorage
- Help center and contextual assistant recognizing usage, billing, tickets, conservation, emergency, and privacy questions
- Responsive design for mobile and desktop
- No dependencies, no API keys, no build step, no backend and no external scripts

**Assistant limitation:** The assistant is rules-based, not a generative model. It accesses only the synthetic public-in-the-page account data and browser-local tickets. It cannot contact real representatives or act on energy services.

## Run locally

Open `index.html` in a browser, or serve it locally:

```bash
python -m http.server 8000
```

Then open http://localhost:8000.

## Deploy to GitHub Pages

1. Create a GitHub repository, e.g. `gridforge-customer-static`.
2. Commit all files, including `.github/workflows/pages.yml`.
3. Go to **Settings → Pages → Build and deployment** and choose **GitHub Actions**.
4. Push to the default branch (`main`); the workflow publishes the static website.
5. Visit `https://YOUR_USERNAME.github.io/gridforge-customer-static/` after the Pages deployment succeeds.

Alternatively, use the built-in **Deploy from a branch** source and deploy the repository root.

## Safety and production notes

- There is **no authentication, server, or access-control boundary**. Do not place real customer data, secrets, confidential documents, or private API credentials in the HTML/JS.
- localStorage is browser-local and readable by scripts on the same origin. Tickets and chat are demonstrations, not secure customer records.
- Never put an Azure OpenAI, OpenAI, or other LLM API key into a public GitHub Pages site. To add a live LLM, use a secured backend, verified user identity, tool permissions, rate limiting, logging, and data protection.
- Do not treat sample billing amounts, sample dates, or usage data as real statements.
- A production customer portal needs identity verification, real API integration, robust authorization, auditing, security review, accessibility validation, and live support and outage integrations.
