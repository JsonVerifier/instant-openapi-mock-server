# instant-openapi-mock-server

I was tired of setting up Stripe sandbox accounts just to test if my frontend doesn't break on a 429. So I found this thing called Connexions and honestly it kind of changed how I work.

Drop your OpenAPI spec in a folder. Push to GitHub. Get a working API. That's literally it.

---

## What I use this for

- Testing my frontend against Stripe without a real Stripe account
- Simulating slow responses to see if my loading states actually work
- Running integration tests in CI without calling any real APIs
- Showing the backend team what I expect before they build anything

---

## How to get started

1. Hit **Use this template** up top
2. Drop your `.yaml` spec into `openapi/`
3. Push to main
4. Download the binary from Releases and run it

```bash
./your-repo-name
```

Your API is running. Go test something.

---

## The folder structure

```
openapi/
  stripe.yaml     →  available at /stripe/
  binance.yaml    →  available at /binance/
  whatever.yaml   →  available at /whatever/
```

Multiple APIs, one server, one port. I used to run three separate Prism instances for this. Never again.

---

## You also get a public URL

Push to main and Mockzilla gives you a hosted version automatically:

```
https://api.mockzilla.org/gh/{your-org}/{your-repo}/
```

Open PRs get their own preview URL too. Pretty useful for sharing with teammates.

---

## Powered by

- [Connexions](https://github.com/mockzilla/connexions) — the engine doing the heavy lifting
- [Mockzilla](https://mockzilla.org) — hosting and the GitHub Action

---

*Not affiliated with Stripe, Binance, or any other API you throw at this.*
