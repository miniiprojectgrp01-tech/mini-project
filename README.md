# 🛡️ Web Application Vulnerability Scanner

### Python + Flask | JCE Cyber Security — Group 1

---

## HOW TO RUN

```bash
# 1. Go into project folder
cd vuln_scanner

# 2. Activate virtual environment
source venv/bin/activate

# 3. Run!
python app.py

# 4. Open browser → http://127.0.0.1:5000
```

No API key needed. All scanning is done by Python directly.

---

## FIRST TIME SETUP (Do this once only)

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

---

## OPTIONAL — AI Summary (Groq)

The scanner works fully without an API key.
If you want AI-written summaries, optionally set a free Groq key:

```bash
export GROQ_API_KEY=gsk_your_key_here
```

Get a free key at https://console.groq.com (Google login, no credit card)

---

## WHAT IT DETECTS (9 checks)

- Missing security headers (CSP, HSTS, X-Frame-Options, and 4 more)
- Information leakage (server version disclosure)
- No HTTPS / unencrypted connection
- Cookie security flags (HttpOnly, Secure, SameSite, loose domain)
- Reflected XSS (input reflection probe)
- SQL Injection indicators (error message detection)
- robots.txt exposure
- Missing security.txt
- Missing rate-limit headers

---

## HOW IT WORKS

1. User enters a URL
2. Python fetches real HTTP headers from the target website
3. Python checks all headers directly — 100% accurate, no AI guessing
4. Results saved to SQLite database
5. Results page shows vulnerabilities, risk score, OWASP Top 10 mapping

---

## PROJECT STRUCTURE

```
mini-project/
├── app.py              ← Flask backend (all scanning logic)
├── requirements.txt    ← Python packages
├── Procfile            ← Render deployment config
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── results.html
│   ├── history.html
│   └── 404.html
└── static/
    ├── css/style.css
    └── js/main.js
```

---

## TEAM

- Akshay Girish — JCE23CC007
- Athira Raveendran — JCE23CC014
- Renisha Febhin P J — JCE23CC024

Guide: Mr. Ambarish A
Department of CS&E (Cyber Security), JCET — 2025-2026
