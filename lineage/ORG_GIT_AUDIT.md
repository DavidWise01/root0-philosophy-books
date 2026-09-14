# Organization Git Audit: Anthropic and OpenAI

Snapshot: 2026-09-14  
Historical evidence cutoff: 2025-12-31  
Scope: public GitHub repository metadata/files and first-party policy/research pages.  
Status: observation-only; this is not an audit of private systems, finances, or intent.

## Ingest and hash gate

The uploaded corpus is catalogued in the corpus lineage ledger, but attachment bytes are not readable by the GitHub connector in this session. Therefore no SHA-256 values are asserted here. GitHub repository object SHAs are not substitutes: Git object identifiers and SHA-256 file digests are different measurements.

The next admissible ingest record must contain, for each source byte stream:

1. original filename and MIME type;
2. byte length;
3. SHA-256 digest computed locally from the original bytes;
4. format metadata (EPUB/DOCX/Markdown/image);
5. source/derivative relationship;
6. cutoff classification;
7. a signed commit or release that carries the manifest.

Until those fields exist, incoming attachments remain catalogued but unverified.

## Same measure

The comparison uses four observable axes. They measure public outputs, not private motives.

| Axis | What counts as evidence |
|---|---|
| Safety / existential-risk governance | constitutions, scaling policies, preparedness frameworks, red-team or catastrophic-risk evaluations |
| Operational controls | guardrails, security files, trust-boundary warnings, deployment gates, reproducible evaluation code |
| Developer / commercial surface | SDKs, API examples, agents, plugins, hosted-product integration, open-weight distribution |
| Provenance / reproducibility | license, source availability, changelog/eval data, repository structure, and sampled commit-signature status |

A repository may score on more than one axis. A large developer surface is not proof of a profit motive, and a safety document is not proof that the controls work in deployment.

## Snapshot geometry

The organization-level repository search returned 15 visible Anthropic matches and 73 visible OpenAI matches for the respective organization/name queries on 2026-09-14. These are search-result observations, not complete organization inventories and not a fair moral score.

    public policy/research
             |
    evals ---+--- safety controls
             |
    SDKs ----+--- agents/plugins/API
             |
        commercial deployment

Anthropic and OpenAI both occupy all four regions. OpenAI's visible repository mesh is broader; Anthropic's public safety language is more concentrated in a smaller set of policy/research artifacts.

## Anthropic: representative lineage

| Node | Date classification | License / structure | Observable signal |
|---|---|---|---|
| [toy-models-of-superposition](https://github.com/anthropics/toy-models-of-superposition) | 2022-09-14, admissible | MIT; archived research notebooks | interpretability research |
| [anthropic-sdk-python](https://github.com/anthropics/anthropic-sdk-python) | 2023-01-17 origin; current tip is live | MIT; LICENSE, CONTRIBUTING, SECURITY, .github | API/developer distribution |
| [anthropic-sdk-typescript](https://github.com/anthropics/anthropic-sdk-typescript) | 2023-01-30 origin; current tip is live | MIT | API/developer distribution; README uses “safety-first” wording |
| [political-neutrality-eval](https://github.com/anthropics/political-neutrality-eval) | 2025-11-12 origin and 2025-11-13 tip, admissible | CC-BY-4.0; public prompts, topics, and eval set | political-even-handedness evaluation |
| [claude-code-base-action](https://github.com/anthropics/claude-code-base-action) | 2025-05-19 origin, admissible | MIT; README warns the action itself does not enforce trust boundaries | automation/developer surface with explicit risk caveat |
| [claude-plugins-official](https://github.com/anthropics/claude-plugins-official) | 2025-11-20 origin, admissible | Apache-2.0; plugins, external_plugins, .github | ecosystem expansion plus explicit third-party trust warning |
| [courses](https://github.com/anthropics/courses) | 2024-05-30 origin, admissible | public course material | prompt evaluation/tool-use training; recommends low-cost Haiku for student API spend |
| [devcontainer-features](https://github.com/anthropics/devcontainer-features) | 2025-03-03 origin; 2025-12-16 push, admissible | MIT | distribution into developer environments |

First-party policy/research lineage is unusually explicit: Anthropic published [Constitutional AI](https://www.anthropic.com/research/constitutional-ai-harmlessness-from-ai-feedback) in 2022, maintains [Claude's Constitution](https://www.anthropic.com/constitution), and publishes a versioned [Responsible Scaling Policy](https://www.anthropic.com/responsible-scaling-policy) whose v1.0 (2023-09-19), v2.0 (2024-10-15), v2.1 (2025-03-31), and v2.2 (2025-05-14) fall on or before the cutoff. Later RSP versions are live observations only. Anthropic's [research index](https://www.anthropic.com/research) also names alignment, economics, and frontier red-team work.

Integrity samples from the current default branches: the 2025-11-13 political-neutrality tip [c5ed679](https://github.com/anthropics/political-neutrality-eval/commit/c5ed67908b56edc0781f47821241ca44114bd4ff) is GitHub-verified; the current Python SDK tip [eb21a435](https://github.com/anthropics/anthropic-sdk-python/commit/eb21a4352015686c30f5759e8c2f02d70f5371e2) is also verified. These are samples, not a claim that every Anthropic commit is signed.

## OpenAI: representative lineage

| Node | Date classification | License / structure | Observable signal |
|---|---|---|---|
| [openai-python](https://github.com/openai/openai-python) | 2020-10-25 origin, admissible | Apache-2.0; official REST SDK | API/developer distribution |
| [openai-cookbook](https://github.com/openai/openai-cookbook) | 2022-03-11 origin, admissible | MIT; examples/guides | API adoption surface |
| [swarm](https://github.com/openai/swarm) | 2024-02-22 origin, admissible | MIT; explicitly experimental and superseded by Agents SDK | agent orchestration research-to-product bridge |
| [model_spec](https://github.com/openai/model_spec) | 2025-02-06 origin, admissible | CC0; public Model Spec, changelog, docs | behavior and governance specification |
| [frontier-evals](https://github.com/openai/frontier-evals) | 2025-03-28 origin, admissible | MIT; public eval projects | frontier capability/risk evaluation |
| [openai-agents-python](https://github.com/openai/openai-agents-python) | 2025-03-11 origin, admissible | MIT; tools, guardrails, handoffs | multi-agent developer platform |
| [openai-guardrails-python](https://github.com/openai/openai-guardrails-python) | 2025-04-09 origin, admissible | MIT; LICENSE, CONTRIBUTING, SECURITY, .github | input/output safety and compliance controls |
| [gpt-oss](https://github.com/openai/gpt-oss) | 2025-06-23 origin, admissible | Apache-2.0 open-weight models | broad distribution/developer access |
| [model_spec_evals](https://github.com/openai/model_spec_evals) | 2026-03-24, live only | MIT | post-cutoff Model Spec compliance harness |
| [privacy-filter](https://github.com/openai/privacy-filter) | 2026-04-17, live only | Apache-2.0; SECURITY.md; on-prem/local operation described | PII protection and enterprise deployment |
| [codex-security](https://github.com/openai/codex-security) | 2026-07-13, live only | Apache-2.0 | security analysis and remediation tooling |

First-party governance lineage is also explicit: the [OpenAI Charter](https://openai.com/charter/) makes broad human benefit and avoidance of harmful concentration a stated mission; the [Preparedness Framework update](https://openai.com/index/updating-our-preparedness-framework/) (2025-04-15) describes tracking and preparing for severe-harm frontier capabilities; and the [Safety page](https://openai.com/safety/) lists red teaming, system cards, preparedness evaluations, safety committees, and staged deployment.

Integrity samples are mixed: the current [openai-python tip](https://github.com/openai/openai-python/commit/e12b81d3bbf644ec7045e152d69bc4b68d69cd48) is GitHub-verified, while the current [model_spec tip](https://github.com/openai/model_spec/commit/7f1cf79fcb656c07f77c8d95b6fbc78dc7fac5b6) is marked unsigned. This is a provenance observation, not a safety judgment.

## Findings

1. **Not “just the money.”** Both organizations publish artifacts directly concerned with harmful capability, model behavior, evaluation, privacy/security, or broad human benefit. Anthropic's Constitutional AI/RSP/Constitution line and OpenAI's Charter/Preparedness/Model Spec line are direct public evidence of ethical and catastrophic-risk concern.
2. **Also not “ethics only.”** Both maintain large API, SDK, agent, plugin, and deployment surfaces. OpenAI has the broader visible GitHub mesh; Anthropic's SDK/plugin/course surfaces are substantial. Product infrastructure and safety infrastructure are interleaved.
3. **Existential language needs care.** The public artifacts mostly operationalize “catastrophic risk,” “severe harm,” alignment, or benefit to humanity. They do not establish that either company has solved existential risk or that its controls are independently effective.
4. **Intent is underdetermined.** A Git repository records published code, policies, and process claims. It cannot reveal whether a private decision was primarily ethical, strategic, competitive, or financial. The defensible conclusion is mixed public incentives with measurable safety commitments, not a hidden-motive verdict.
5. **Provenance is uneven.** Open source licenses, public eval material, and some verified commits improve auditability. Sampled unsigned tips, unverified third-party plugins, voluntary policies, and post-cutoff rewrites remain explicit caveats.

## Reproducibility and next gate

To close the corpus ingest gate, compute SHA-256 locally over the original uploaded files and add a manifest keyed by filename, size, MIME, digest, and source relation. Do not copy GitHub blob SHA values into that field. For the organization audit, pin a future snapshot to commit SHAs and preserve the API responses or signed export used to make any historical claim.

This record is a forward lineage anchor, not proof that a timestamp or a policy claim is true beyond the public evidence observed.
