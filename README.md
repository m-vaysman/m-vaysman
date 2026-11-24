## Michael Vaysman

C#/.NET engineer, 17 years in capital markets — time spent both **on** trading desks and
inside engineering teams. Merrill Lynch, Société Générale, Avenue Capital, Balyasny,
Alphadyne, Ellington.

Desk-side, that meant owning the problem outright: an orphaned $1B total-return swap book
that ops wouldn't support, or 80,000 lines of front-office code that had to become a
maintainable C# add-in. On engineering teams it meant the work underneath — build and
release pipelines, data warehousing, moving a 15-year SVN repo onto Bitbucket and
TeamCity and cutting deployment time 70%.

Having done both, I can usually tell which problem a desk actually has.

**Domain** — bank debt, CLOs, total-return swaps, CDS, securities lending and repo,
front-to-back trade lifecycle.

**Stack** — .NET 8, C#, SQL Server, EF Core, Dapper · WPF, ASP.NET Core, RabbitMQ,
SignalR · Excel-DNA · TeamCity, Azure DevOps, SSDT.

Also run a home server — kids ask, I deliver, the apps are vibe-coded.

<!-- RecDiffy feature block for github.com/m-vaysman profile README -->

<p align="center">
  <a href="https://github.com/m-vaysman/recdiffy.net">
    <img alt="RecDiffy.NET" src="https://raw.githubusercontent.com/m-vaysman/recdiffy.net/main/RecDiffy.NET/resources/logos/columns-dark.jpg" width="520" />
  </a>
</p>

### [RecDiffy.NET](https://github.com/m-vaysman/recdiffy.net)

An open-source, general-purpose .NET reconciliation engine for matching, comparing and
explaining differences between datasets from independent systems.

Designed for situations where records represent the same underlying activity but differ
in identifiers, formats, granularity or grouping — including trades, positions, cash
balances, settlements, inventory and accounting records.

Reconciliation behavior is defined through configurable JSON profiles or a strongly
typed, fluent C# API. The core engine is domain-independent, with extensible
normalization rules and specialized trading support.

**Pipeline:** Normalize → Consolidate → Match → Compare → Explain

Matching establishes which records belong together. Comparison determines whether their
values agree. A successful match does not imply the absence of a break.

The engine emphasizes deterministic results, explicit matching policies, configurable
tolerances, traceable decisions and the preservation of unresolved differences.

**Status:** Stable release. The public API has been stable since v1.2.0. Packages are
available on NuGet.org, with ongoing development and preview releases for new
capabilities. Supports .NET 8 and .NET 10.

#### Where it stands

**Available**
- Profile-driven, multi-pass reconciliation engine
- Fluent C# API and declarative JSON profiles
- Record normalization, lifecycle consolidation and grouped matching
- Field-level comparison, configurable tolerances and break explanations
- CSV and Excel ingestion
- Formatted Excel reports, DataTables and HTML output
- Trading-specific normalization rule pack
- Public NuGet packages and automated release workflows
- Browser-based demonstration and scheduled reconciliations of public financial datasets
- Extensive automated testing, performance benchmarks and static analysis
- Native AOT host, developer documentation, runnable samples and AI-agent documentation
- MIT license

**Preview and active development**
- Excel add-in
- FIX protocol ingestion and reconciliation scenarios
- Incremental batch reconciliation and snapshots
- Matching enhancements and large-scale parallel reconciliation
- Blind profile discovery and external dataset evaluation

RecDiffy is an embeddable reconciliation engine rather than a complete operational
workflow platform. It provides the reconciliation logic and explainable results for
developers building their own applications, controls and operational tools.

---

### Cobbler Hill Technologies

Since September 2023 I've been building a market-data and analytics platform end to end —
ingestion, storage, analytics, and the desktop tools that sit on top. It runs on real
hardware against real market data. It isn't a portfolio exercise, which is why the
rough edges are still in it.

| Repo | What it is |
|---|---|
| **[RecDiffy](https://github.com/m-vaysman/recdiffy.net)** | .NET 10 reconciliation library: compares two datasets and explains every match, break, and unmatched row. Pre-release, with a trading rule pack. |
| **[MarketData.DB](https://github.com/m-vaysman/MarketData.DB)** | SQL Server warehouse for prices, quotes, ETF holdings, SEC 13F filings and Treasury curves. Range partitioning across physical volumes, clustered columnstore, In-Memory OLTP, and a SQL CLR aggregate — versioned as an SSDT project, deployed as a dacpac. |
| **[omsloans](https://github.com/m-vaysman/omsloans)** | WPF (.NET 8) MVVM order management system for syndicated loan trading and operations, on EF Core 9 + SQL Server. |
| **[cobbler.options](https://github.com/m-vaysman/cobbler.options)** | Options analytics in C#. |

Most of the platform is still private — ETL framework, analytics services, shared
libraries. Happy to walk through any of it.

---

### Options as types

An experiment in pushing model correctness onto the compiler: every symbol in
Black-Scholes gets its own C# type, so the notation from the papers survives and
swapping volatility for the rate stops compiling. It half worked, which is the
interesting part.

[Repo](https://github.com/m-vaysman/options-as-types) &nbsp;·&nbsp; [Writeup](https://m-vaysman.github.io/options-as-types/)

---

### CLASS OPEN FOR EXTENSION CLOSED FOR MODIFICATION AGENT SKILL

Forces coding agents to extend shipped code rather than edit it. New behavior goes through existing seams; locked classes stay untouched. Smaller diffs, fewer regressions, less architectural drift.

[Skill](https://github.com/m-vaysman/skills-and-prompts/tree/main/skills) &nbsp;·&nbsp; [Writeup](https://m-vaysman.github.io/skills-and-prompts/the-model-will-open-the-class/)

---

📍 Fairfield, CT &nbsp;·&nbsp; ✉️ [mvaysman@pm.me](mailto:mvaysman@pm.me)
