## Michael Vaysman

C#/.NET engineer, 17 years in capital markets — time spent both **on** trading desks and
inside engineering teams. Merrill Lynch, Société Générale, Avenue Capital, Balyasny,
Alphadyne, Ellington.

Desk-side, that meant owning the problem outright: an orphaned $1B total-return swap book
that ops wouldn't support, or 80,000 lines of front-office VBA that had to become a
maintainable C# add-in. On engineering teams it meant the work underneath — build and
release pipelines, data warehousing, moving a 15-year SVN repo onto Bitbucket and
TeamCity and cutting deployment time 70%.

Having done both, I can usually tell which problem a desk actually has.

**Domain** — bank debt, CLOs, total-return swaps, CDS, securities lending and repo,
front-to-back trade lifecycle.

**Stack** — .NET 8, C#, SQL Server, EF Core, Dapper · WPF, ASP.NET Core, RabbitMQ,
SignalR · Excel-DNA · TeamCity, Azure DevOps, SSDT.

Also run a home server — kids ask, I deliver, the apps are vibe-coded.

---

### Cobbler Hill Technologies

Since September 2023 I've been building a market-data and analytics platform end to end —
ingestion, storage, analytics, and the desktop tools that sit on top. It runs on real
hardware against real market data. It isn't a portfolio exercise, which is why the
rough edges are still in it.

| Repo | What it is |
|---|---|
| **[MarketData.DB](https://github.com/m-vaysman/MarketData.DB)** | SQL Server warehouse for prices, quotes, ETF holdings, SEC 13F filings and Treasury curves. Range partitioning across physical volumes, clustered columnstore, In-Memory OLTP, and a SQL CLR aggregate — versioned as an SSDT project, deployed as a dacpac. |
| **[omsloans](https://github.com/m-vaysman/omsloans)** | WPF (.NET 8) MVVM order management system for syndicated loan trading and operations, on EF Core 9 + SQL Server. |
| **[cobbler.options](https://github.com/m-vaysman/cobbler.options)** | Options analytics in C#. |

Most of the platform is still private — ETL framework, analytics services, shared
libraries. Happy to walk through any of it.

---

### Homelab that ships

Kids ask. I deliver. The apps are vibe-coded.

I run a home server that hosts what they actually use. The public ones are **HTTPS** on
[cobblerhill.net](https://cobblerhill.net) — not by punching holes in the router. I specify
the product and the constraints, an AI coding agent writes and rewrites the client, I put
it on the box and keep it up.

What I own end-to-end: the server, DNS, TLS, the tunnel. Not a hand-written JavaScript
specialty.

`cloudflared` opens an **outbound-only** Cloudflare Tunnel. No inbound ports, no exposed
home IP, TLS terminated at the edge.

| App | What it is |
|---|---|
| **[2nd Grade Spelling Stars](https://words.cobblerhill.net)** | Study, type, quiz, streaks. Built for my son. On an iPad he writes the word by hand with a pen; OCR reads it back and marks it right or wrong. Good enough for a spelling list, not a research project. |
| **[Tetris Duel](https://tetris.cobblerhill.net)** | Solo, local 2-player, online multiplayer, leaderboards. |
| **[Block Bash](https://bbash.cobblerhill.net)** | Grid puzzle — combos, palettes, a global top 50. |
| **Kids chatroom** — family only, no public link | Skibidi-themed real-time chat the kids actually use. WebSockets, room cap, rate limits, mini-games. An AI bot talks in the room, and a command turns a description into a generated image via OpenAI and posts it back. A moderation model hosted on Groq screens messages for profanity and unintended malice before they go out. |

---

📍 Fairfield, CT &nbsp;·&nbsp; ✉️ [mvaysman@pm.me](mailto:mvaysman@pm.me)
