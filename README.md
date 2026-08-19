## Michael Vaysman

C#/.NET engineer, 17 years, embedded **on** trading desks rather than adjacent to them —
Merrill Lynch, Société Générale, Avenue Capital, Balyasny, Alphadyne, Ellington.

The work is usually the same shape: a desk has a process that breaks, doesn't scale, or
"can't be automated," and I build the thing that fixes it. Orphaned $1B swap book with no
ops support. 80,000 lines of front-office VBA that needed to become a maintainable C#
add-in. Voice trades getting hand-keyed into the OMS at two hours a day per trader.

**Domain** — bank debt, CLOs, total-return swaps, CDS, securities lending and repo,
front-to-back trade lifecycle.

**Stack** — .NET 8, C#, SQL Server, EF Core, Dapper · WPF, ASP.NET Core, RabbitMQ,
SignalR · Excel-DNA · TeamCity, Azure DevOps, SSDT.

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

📍 Fairfield, CT &nbsp;·&nbsp; ✉️ [mvaysman@pm.me](mailto:mvaysman@pm.me)
