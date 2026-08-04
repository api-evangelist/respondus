# Respondus (respondus)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Respondus builds assessment-integrity tools for online exams. Its two flagship products are **LockDown Browser** - a custom browser that locks down the testing environment (disabling copy/paste, printing, other applications, and navigation away from the exam) - and **Respondus Monitor**, an automated webcam-based online proctoring service that layers AI-assisted flagging and review on top of LockDown Browser. Respondus also publishes the Respondus 4 exam authoring tool and StudyMate. More than 2,000 institutions across 50+ countries use Respondus to deliver hundreds of millions of online exams each year.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/respondus/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/respondus/refs/heads/main/apis.yml)

## Access Model — No Public Developer API

Respondus does **not** publish a self-service public developer API. There is no public REST surface, no developer key/console, no OpenAPI definition, and no documented endpoints. Respondus is delivered as licensed institutional software that plugs into a learning management system (LMS), not as an API product. Integration happens three ways, none of which is an open API:

1. **Native LMS plugins / building blocks.** Respondus ships out-of-the-box integrations for major LMS platforms (Blackboard Learn Original and Ultra, D2L Brightspace, Instructure Canvas, Moodle, Sakai, Schoology, and Infinite Campus). A license administrator installs and configures the plugin - typically in about 15 minutes - so instructors enable LockDown Browser / Monitor per exam from inside the LMS. The integration talks server-to-server to the Respondus cloud (for example `https://smc-service-cloud.respondus2.com`); this is a private product integration, not a documented public API.

2. **LTI (Learning Tools Interoperability).** For platforms that support it, Respondus tools are added as an LTI external tool / external app / LTI app rather than a Respondus-specific API. On Blackboard Ultra, Respondus Monitor additionally requires the institution to configure Blackboard's own REST API and a Proctoring Service - i.e. it consumes the LMS's API, it does not expose one of its own. The exam-integrity behavior rides on the LTI launch and the vendor's LMS, not on a Respondus REST API.

3. **LockDown Browser SDK (privately licensed).** For companies that want to embed LockDown Browser into their own assessment or learning platform, Respondus licenses a **LockDown Browser SDK Edition**. It is described as well-documented and covers Windows, Mac, iPadOS, and Chromebook, but it is a commercial, sales-gated SDK obtained by contacting Respondus - not a public developer API with open documentation or self-service keys. Terms and licensing fees are quoted directly.

Because there is no documented public API, this catalog entry is an **honest stub**: no `apis` are listed in `apis.yml`, and no `openapi/`, `plans/`, `rate-limits/`, `finops/`, or `collections/` artifacts are fabricated. If Respondus later publishes a public API or partner developer program, this entry should be expanded with real, sourced endpoints.

## Tags

- Assessment
- Proctoring
- Online Exams
- LockDown Browser
- Respondus Monitor
- EdTech
- LTI
- LMS Integration
- Exam Integrity

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## Pricing

Respondus is licensed to institutions, not metered per API call. For higher education, the annual LockDown Browser fee is tiered by total Student FTE (as reported to IPEDS). Publicly listed example tiers include roughly:

- 1–2,000 students: $2,795/year
- 2,001–2,500 students: $3,195/year
- 2,501–5,000 students: $3,745/year
- 5,001–10,000 students: $4,595/year
- 10,001–15,000 students: $5,045/year

Annual LockDown Browser licensing includes 200 free seats of Respondus Monitor; larger Monitor usage is quoted separately. Licenses renew annually (August 1) and fees are pro-rated on the academic year. K-12 pricing and formal quotes are handled directly by Respondus. See the pricing pages linked below. Values are illustrative and subject to change - confirm with Respondus.

## Common Properties

- [Website](https://web.respondus.com)
- [LinkedIn](https://www.linkedin.com/company/respondus)
- [Support](https://support.respondus.com/hc/en-us)
- [Partners (LMS)](https://web.respondus.com/partners/lms/)
- [LockDown Browser SDK Licensing](https://web.respondus.com/partners/technology/sdk-licensing/)
- [Plans / Pricing](https://web.respondus.com/he/lockdownbrowser/pricing/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
