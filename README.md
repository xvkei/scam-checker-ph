# Scam Checker PH: Expert System for Cybercrime Legal Advice

A browser-based expert system that helps Filipino internet users identify whether they have been scammed online, what Philippine law applies to their situation, and what steps to take next.

> For academic purposes only. This does not constitute actual legal advice.

---

## Features

- Covers **17 scam types** relevant to Filipino users including GCash fraud, phishing, romance scams, job scams, SIM swap attacks, and more
- Identifies the **applicable Philippine law** for each scam type
- Outputs a **severity rating** (High / Medium / Low risk)
- Shows **which expert rules fired** to reach the verdict
- Provides a **numbered list of recommended action steps** (which agencies to report to, what evidence to gather)
- Back button to undo answers and try different paths
- Fully **offline** — runs entirely in the browser with no server or API needed

---

## Scam Types Covered

| Rule | Scam Type |
|---|---|
| R001 | Emergency scam (Budol Fund / GCash emergency request) |
| R002 | Identity impersonation / vishing (fake bank or e-wallet support) |
| R003 | Romance scam |
| R004 | SMS phishing / smishing |
| R005 | Social media money scam (Facebook/Instagram DM) |
| R006 | Online selling scam / Facebook Marketplace fraud |
| R007 | E-commerce non-delivery (Shopee, Lazada, TikTok Shop) |
| R008 | Fake online store |
| R009 | Bank / e-wallet phishing |
| R010 | Credit card phishing |
| R011 | OTP theft / account compromise |
| R012 | Low-risk data harvesting |
| R013 | Job scam / pyramiding |
| R014 | Investment / Ponzi scam |
| R015 | Suspicious job offer (red flags, no payment yet) |
| R016 | SIM swap attack |
| R017 | Unauthorized account access |

---

## Laws Referenced

- **RA 10175** - Cybercrime Prevention Act of 2012
- **RA 8484** - Access Devices Regulation Act
- **RA 7394** - Consumer Act of the Philippines
- **RA 8792** - Electronic Commerce Act
- **RA 10173** - Data Privacy Act of 2012
- **RA 11934** - SIM Registration Act
- **RA 8799** - Securities Regulation Code
- BSP Consumer Protection regulations

---

## How to Use

1. Open `index.html` in any modern browser (Chrome, Firefox, Edge)
2. Answer the branching questions about what happened to you
3. The system will identify the scam type, show which rule fired, cite the relevant law, and give step-by-step action items
4. Click **Start over** to reset and try a different scenario

No installation, no internet connection, no server required.

---

## How It Works

The system uses a **rule-based inference engine** implemented in vanilla JavaScript.

```
User answers question
        ↓
Inference engine reads currentKey from knowledge base (flows object)
        ↓
Is this node a question or a verdict?
        ↓                    ↓
  Show next question     Show verdict (scam type, severity,
  and update history     rules fired, law, action steps)
```

Each node in the knowledge base is either a **question node** (with branching answer paths) or a **verdict node** (with the final output). No server, no database, no API calls — pure client-side JavaScript.

---

## Tech Stack

- **JavaScript** - inference engine, state management, DOM rendering
- **HTML5 + CSS3** - UI and styling
- Single file: `index.html`

---

## Academic Context

Built for **CS301 - Expert Systems Activity**
Lyceum of the Philippines University Cavite | April 2026

---

> This system is for academic purposes only. For actual legal concerns, consult a licensed lawyer or contact NBI, PNP-ACG, or the relevant government agency directly.
