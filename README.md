# Klu (klu-ai)

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

Klu (klu.ai) is an LLM app platform for designing, deploying, evaluating, and observing prompt-driven AI applications. The Klu Engine exposes a REST API at https://api.klu.ai/v1 (Bearer API key) where an Action encapsulates a prompt template, model config, context (RAG), and output parsing, and is invoked to generate completions, with data, feedback, sessions, and models managed alongside it.

> NOTE — product development appears dormant. The official `klu` SDK last shipped in March 2025 and the founding team's recent open-source work has shifted toward xAI / Grok tooling. See `review.yml` for the honest status assessment.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/klu-ai/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/klu-ai/refs/heads/main/apis.yml)

## Tags

- AI
- LLM
- LLM App Platform
- Prompt Engineering
- Evaluation
- Observability

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Klu Actions / Prompt API

Runs a Klu Action by GUID against input variables, returning a generated completion plus a feedback URL. Supports streaming, async execution, response caching, session memory, context metadata filtering, and experiments. This is the core generative endpoint of the Klu Engine.

- **Human URL:** [https://docs.klu.ai/resources/api-actions](https://docs.klu.ai/resources/api-actions)
- **Base URL:** `https://api.klu.ai/v1`

#### Tags

- Actions
- Prompt
- Completions
- Generation

#### Properties

- [Documentation](https://docs.klu.ai/resources/api-actions)
- [API Reference](https://docs.klu.ai/resources/api-basics)
- [OpenAPI](openapi/klu-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/klu-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/klu-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Klu Data / Feedback API

Captures and manages the data points generated by Actions - each holding the prompt, completion, and metadata - and the feedback (ratings, corrections, issues) attached to them. Data can be imported and exported as JSONL/CSV for evaluation and fine-tuning. Context libraries for retrieval-augmented generation are managed here.

- **Human URL:** [https://docs.klu.ai/guides/data](https://docs.klu.ai/guides/data)
- **Base URL:** `https://api.klu.ai/v1`

#### Tags

- Data
- Feedback
- Ratings
- Datasets

#### Properties

- [Documentation](https://docs.klu.ai/guides/data)
- [API Reference](https://docs.klu.ai/resources/api-context)
- [OpenAPI](openapi/klu-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/klu-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/klu-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Klu Models API

Manages the LLM providers and models available in a workspace and the default model used by Actions. Klu brokers across 50+ models and providers (OpenAI, Anthropic, and others) so an Action's model config can be changed without rewriting integration code.

- **Human URL:** [https://docs.klu.ai/key-concepts](https://docs.klu.ai/key-concepts)
- **Base URL:** `https://api.klu.ai/v1`

#### Tags

- Models
- Providers
- Configuration

#### Properties

- [Documentation](https://docs.klu.ai/resources/api-basics)
- [OpenAPI](openapi/klu-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/klu-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/klu-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Klu Sessions API

Stores and retrieves session memory across multiple Action generations, enabling multi-turn conversational experiences such as copilots and coaches that retain context between requests via a session GUID.

- **Human URL:** [https://docs.klu.ai/key-concepts](https://docs.klu.ai/key-concepts)
- **Base URL:** `https://api.klu.ai/v1`

#### Tags

- Sessions
- Memory
- Conversations

#### Properties

- [Documentation](https://docs.klu.ai/resources/api-basics)
- [OpenAPI](openapi/klu-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/klu-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/klu-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Klu Apps / Workspaces API

Organizes work into Workspaces and Apps (projects) that group related Actions, context, and experiments. Apps are the top-level container for an AI use case; experiments run prompt-vs-prompt evaluations and A/B tests within them.

- **Human URL:** [https://docs.klu.ai/key-concepts](https://docs.klu.ai/key-concepts)
- **Base URL:** `https://api.klu.ai/v1`

#### Tags

- Apps
- Workspaces
- Projects
- Experiments

#### Properties

- [Documentation](https://docs.klu.ai/resources/api-basics)
- [OpenAPI](openapi/klu-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/klu-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/klu-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/klu-ai)
- [LinkedIn](https://www.linkedin.com/company/klu-ai)
- [Website](https://klu.ai)
- [Documentation](https://docs.klu.ai)
- [Plans](plans/klu-ai-plans-pricing.yml)
- [Rate Limits](rate-limits/klu-ai-rate-limits.yml)
- [Fin Ops](finops/klu-ai-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
