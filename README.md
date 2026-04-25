# DEMO PURPOSE ONLY
### Secure Application Development
Node Secrets Assignment: Scenario 1 - Hard Code Secret <br>
April 25, 2026 <br>
This app is a **Code Secret Demo - Using Fake Secrets.**


# Scenario 1 — Hard Coded Secrets

This repository demonstrates the **worst practice** of storing secrets by hard-coding them directly into the application source code.

<br>

Both secrets are written as plain text at the top of `app.js`.

- `NODE_ENV` = `"development"`
- `API_KEY`  = `"FAKE_1234567890_HARDCODED_KEY"`

Anyone who views this repository on GitHub can see these values immediately.

## How to run this application:

### Requirements

- Node.js latest
- Secret Keys (Already hard coded into the application):

    * `NODE_ENV=development`
    * `API_KEY=<your-api-key-here>`

Once you cd into the application root directory follow these steps:

1.  Install 

        npm install


2. Run the simple server with keys hardcoded in the application

        node app.js


- TEST In the browser

     `http://127.0.0.1:3000` 


## Outcomes:

1. The terminal should display the secret variables and their values. 

```bash
    NODE_ENV: development
    API_KEY : FAKE_1234567890_HARDCODED_KEY
```

2. The browser will display the secret variables and application files. 

```browser

    Environment: development
    API Key    : FAKE_1234567890_HARDCODED_KEY
    -----------------------------
    Files in directory:
    - .git
    - .gitignore
    - README.md
    - app.js
    - package-lock.json
    - package.json

```
### Why this is a worst practice?

1. Secrets are exposed to anyone with repo access.

2. Secrets persist in git history forever, even if later removed.

3. Rotating a secret requires a code change and a new commit.

4. No access control — every developer gets every secret.
