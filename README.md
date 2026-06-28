# ☠ Den Den Mushi — One Piece REST API

> Access One Piece universe data programmatically. Characters, bounties, chapters, episodes, arcs and more — all through a clean REST API.

---

## 🌊 What's in the dataset?

| Type | Count |
|------|-------|
| Characters | 1,548 |
| Chapters | 1,186 |
| Episodes | 1,031 |
| Arcs | 49 |
| **Total pages** | **3,859** |

Coverage: Chapters 1–1185 · Episodes 1–1031 · up to the Elbaph Arc.

---

## 🚀 Quick Start

**1. Get a free API key**

Visit [API Docs](https://onepiece-api-for-sadiq-production.up.railway.app/api-docs.html) → Sign up → Generate key from dashboard.

**2. Make your first call**

```bash
curl https://onepiece-api-for-sadiq-production.up.railway.app/v1/character/Nami \
  -H "X-API-Key: ddm_free_your_key_here"
```

**Response:**
```json
{
  "title": "Nami",
  "type": "character",
  "sections": {
    "Bounty": "366,000,000 berries",
    "Appearance": "Nami is a slim young woman...",
    "Personality": "..."
  }
}
```

---

## 📡 Endpoints

| Endpoint | Description |
|----------|-------------|
| `GET /v1/character/{name}` | Full character page |
| `GET /v1/character/{name}/bounty` | Bounty only |
| `GET /v1/character/{name}/section/{section}` | Single section e.g. `abilities-and-powers` |
| `GET /v1/chapter/{number}` | Chapter summary |
| `GET /v1/episode/{number}` | Episode summary |
| `GET /v1/search?q=zoro&type=character` | Search pages |
| `GET /v1/random?type=character` | Random page |
| `GET /v1/types` | Dataset stats |

Pass your key in every request header:
```
X-API-Key: ddm_free_your_key_here
```

---

## ⚡ Rate Limits

| Tier | Requests/day | Price |
|------|-------------|-------|
| 🟢 Free | 5 | Free forever |
| 🔵 Basic | 1,000 | Coming soon |
| 🟡 Pro | 10,000 | Coming soon |

Every response includes rate limit headers:

```
X-RateLimit-Limit: 5
X-RateLimit-Used: 1
X-RateLimit-Remaining: 4
X-RateLimit-Reset: 2026-06-28T23:59:59Z
```

---

## 🔑 Get an API Key

1. Visit the [API Docs](https://onepiece-api-for-sadiq-production.up.railway.app/api-docs.html)
2. Click **Get Free API Key**
3. Sign up with your email and password
4. Log in and generate your key from the dashboard

Keys look like: `ddm_free_abc123xyz`

---

## ❌ Error Codes

| Code | Meaning |
|------|---------|
| `404 not_found` | Character, chapter, or episode not in dataset |
| `429 rate_limit_exceeded` | Daily limit reached, resets at midnight UTC |
| `401 invalid_api_key` | Key is invalid or inactive |
| `400 invalid_query` | Search query too short |

---

## ⚠️ Disclaimer

One Piece © Eiichiro Oda / Shueisha / Toei Animation. This is a fan-made project, not affiliated with or endorsed by the original creators. Data sourced from the [One Piece Wiki](https://onepiece.fandom.com/wiki/One_Piece_Wiki).

---

*Built with ❤️ for the One Piece community*
