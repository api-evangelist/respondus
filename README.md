# Respondus (respondus)

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
