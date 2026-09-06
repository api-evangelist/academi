# Academi

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

**ACADEMI** was the 2011–2014 name of the American private military, security and training
company founded on 26 December 1996 in North Carolina by Erik Prince and Al Clark as
**Blackwater**. It was renamed **Blackwater Worldwide** in October 2007 after the Nisour Square
shooting in Baghdad, then **Xe Services LLC** in February 2009. In December 2010 Prince sold his
equity to **USTC Holdings** — an investor consortium led by Forté Capital Advisors and Manhattan
Strategic Ventures — and the company was rebranded **ACADEMI** in December 2011 under chairman
Red McCombs. In June 2014 **Academi Training Center, LLC** was merged with Triple Canopy,
Constellis Ltd., Strategic Social, Tidewater Global Services, National Strategic Protective
Services and International Development Solutions to form **Constellis Holdings**, acquired by
Apollo Global Management in September 2016 and headquartered in Herndon, Virginia.

**The brand is retired.** Constellis' own Constellis Training Center page states it plainly:

> *"Academi remains part of historical, legal, and contractual records, but Constellis does not
> operate under the Academi name."*

> *"While the Constellis Training Center includes the facility formerly associated with
> Blackwater, Xe Services, and Academi, Constellis does not market or conduct business under
> those names."*

The Moyock, North Carolina campus — the largest private training facility in the United States —
now trades as the **Constellis Training Center**.

**There is no Academi API surface to enrich.** The business sells physical services — firearms,
driving, maritime, K-9, UAS/C-UAS and advanced security and military training, protective
security details, and logistics and complex program management for US government customers — not
software. As probed on 2026-09-06:

| Probe | Result |
|---|---|
| `https://academi.com/` | TLS handshake failure on 443 — no certificate covers the hostname |
| `http://academi.com/` and every path probed | `409` with a Cloudflare `error code: 1001` body — unconfigured host |
| `http://academi.com/.well-known/*` (7 paths), `/llms.txt`, `/openapi.json`, `/robots.txt` | `409` |
| `api.academi.com`, `developer.academi.com`, `docs.academi.com` | NXDOMAIN |
| `academi.com` DNS | DNSSEC signed, Proofpoint MX, SPF, DMARC `p=reject` with `rua=mailto:itsec@constellis.com` — mail-retained, web-retired, administered by Constellis |
| `https://constellis.com/.well-known/*` (successor host) | `404` on every path |
| `https://api.github.com/orgs/academi` | `200`, but an empty shell org created 2014-01-21 — 0 repos, no name/blog/email; not attributable |
| `https://api.github.com/orgs/constellis` | `404` |
| npm search `academi constellis` / `https://pypi.org/pypi/academi/json` | 0 packages / `404` |

Constellis (the parent) does market an *"API Integration"* technology-services offering and a
LEXSO platform whose API-ICD documentation and sandbox are available only to partners under an
executed MNDA. **Those are Constellis surfaces and are deliberately not credited to Academi
here** — Constellis is a separate company record.

This profile is retained as a historical record.

**Sources**
- Constellis Training Center — https://constellis.com/constellis-training-center/
- Constellis, *Advanced Security & Military Training* — https://constellis.com/what-we-do/training-services/advanced-security-military-training/
- Blackwater (company), Wikipedia — https://en.wikipedia.org/wiki/Blackwater_(company)
- Constellis, Wikipedia — https://en.wikipedia.org/wiki/Constellis
- Secondary-market listing this record was harvested from — https://equityzen.com/company/academi
