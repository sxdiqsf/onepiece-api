# ☠ Den Den Mushi — One Piece REST API

> Access One Piece universe data programmatically. Characters, bounties, chapters, episodes, arcs and more — all through a clean REST API.

---

## 🌊 What's in the dataset?

Characters, chapters, episodes, arcs, bounties, Devil Fruits, lore and more — covering the One Piece universe up to the Elbaph Arc.

---

## 🚀 Quick Start

**1. Get a free API key**

Visit [API Docs](https://api.dendenmushi.space/api-docs.html) → Sign up → Generate key from dashboard.

**2. Make your first call**

```bash
curl https://api.dendenmushi.space/v1/character/Nami \
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
| 🟢 Free | 3 | Free forever |
| 🔵 Basic | 50 | Coming soon |
| 🟡 Pro | 100 | Coming soon |

Every response includes rate limit headers:

```
X-RateLimit-Limit: 3
X-RateLimit-Used: 1
X-RateLimit-Remaining: 2
X-RateLimit-Reset: 2026-06-28T23:59:59Z
```

---

## 🔑 Get an API Key

1. Visit the [API Docs](https://api.dendenmushi.space/api-docs.html)
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
