<div align="center">

```text
┌──────────────────────────────────────────────────────────────────────┐
│  MARKET PULSE                                           INTINS / DEMO │
└──────────────────────────────────────────────────────────────────────┘

    define a job ──► find local providers ──► request estimates
          ▲                                      │
          └──── compare replies ◄──── collect ◄──┘
```

# Market Pulse

**A tutorial demo for gathering comparable local service estimates by email.**

[Demo](#run-the-demo) · [Walkthrough](#demo-walkthrough) · [How it works](#how-it-works)

</div>

Market Pulse uses one consistent job profile to find local providers, request estimates and organise replies. The sample campaign uses lawn mowing in three Sydney suburbs.

> This is a front-end demonstration with fictional providers, prices and email replies. It does not send email or connect to business directories, Supabase, Outlook or AI services.

## What you can explore

- Review a standard residential lawn profile with an annotated reference photo.
- Explore a provider table, search and filter businesses, and export sample records as CSV.
- Preview the per-suburb estimate email and simulate sending an enquiry.
- Review fictional replies, price ranges, GST, inclusions and response status.
- See suburb coverage on an illustrative map.

## Run the demo

The demo needs no package installation, accounts or API keys. It uses plain HTML, CSS and JavaScript.

```sh
git clone https://github.com/lockej2005/market-pulse.git
cd market-pulse
python3 -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000) in a browser. Stop the local server with `Ctrl+C`.

## Demo walkthrough

1. Start at **Overview** to show campaign counts, response prices and suburb coverage.
2. Open **Job profile** to show the shared lawn photo, measurements, scope and suburb-specific email preview.
3. Open **Businesses** to search and filter the discovery table, then export the CSV.
4. Open **Outreach** and simulate an enquiry. The activity feed changes, but no message is sent.
5. Return to the response table and open a reply to see the price and evidence summary.

## How it works

The demo data lives in `app.js`. The interface renders the overview, profile, business table and outreach activity in the browser. Search, response filters, CSV export, sample record creation and simulated enquiries work locally for the session.

A production system would need separate integrations for suburb boundaries and business discovery, a real mailbox, an AI extraction service, durable storage and a job runner. This repository does not include those integrations or credentials.

## Repository layout

```text
.
├── index.html
├── styles.css
├── app.js
├── assets/
│   ├── favicon.svg
│   ├── residential-lawn-demo.png
│   └── space-grotesk-medium.ttf
└── README.md
```

## Sample data and contact safety

All named businesses, email addresses, prices and customer details are fictional. The `.example` email domain is reserved for examples. The homeowner, Jamie, is a fictional demo persona. The lawn image is AI-generated and its measurements are illustrative.

The **Simulate** actions only update the in-browser demo. They do not call Outlook or another email provider. Do not treat sample prices as current market quotes.

## Technology

The review demo uses browser-native HTML, CSS, JavaScript and SVG. The proposed production stack is Fly.io for background work, Supabase for data and file storage, Vercel for a hosted dashboard, and Microsoft Graph for a dedicated mailbox.

## License

No license has been selected. The public repository is available for review; reuse and redistribution require permission from the repository owner.
