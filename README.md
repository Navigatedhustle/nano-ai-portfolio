# Nano AI Portfolio

Carlos Sanchez's collection of local AI applications, evidence-oriented demos and research tools. The projects were inspected on the original NVIDIA GB10 ARM64 workstation and prepared as independent sanitized source snapshots. All repositories start private; public sharing requires a separate review and explicit owner approval.

| Project | Value | Verified maturity |
| --- | --- | --- |
| [Atlas Claude](https://github.com/Navigatedhustle/atlas-claude) | An independently built local voice-analytics assistant with deterministic calculations, numeric grounding, synthetic knowledge retrieval and a restricted developer mode. | 75 tests / 7 model-dependent skips; local analytics demo |
| [Atlas GPT](https://github.com/Navigatedhustle/atlas-gpt) | A local voice assistant for synthetic enterprise and university analytics, with grounded numeric answers, exact-row knowledge provenance, and a constrained developer sandbox. | 24 tests; local analytics demo |
| [Beat the Guard](https://github.com/Navigatedhustle/beat-the-guard) | An offline higher-education policy game. | Synthetic parser/game/ASGI smoke; model verdicts not rerun |
| [CampusCompass Local](https://github.com/Navigatedhustle/campuscompass-local) | A synthetic university-advising demonstration that reconciles degree-audit evidence, approved substitutions and policy records into a cited brief for human review. | 22 tests + UI build; synthetic advising demo |
| [EDUCAUSE Demo Hub](https://github.com/Navigatedhustle/educause-demo-hub) | A local demo launcher and lifecycle controller that serializes heavyweight workloads and exposes readiness, stop and failure handling in native and browser menus. | 4 isolated failure checks; live transitions not rerun |
| [Genesis Observatory](https://github.com/Navigatedhustle/genesis-observatory) | A persistent artificial ecology and local language-agent investigation environment. | 21 tests; research prototype |
| [Jarvis Local](https://github.com/Navigatedhustle/jarvis-local) | A local executive-assistant codebase with evidence-backed mail/calendar reads, memory, internal drafting, research, voice and payload-bound action approvals. | 578 synthetic tests; live provider acceptance excluded |
| [Research Observatory](https://github.com/Navigatedhustle/research-observatory) | A local multi-feed vision demonstration that detects objects, summarizes events with a local language model and stores searchable event memory. | Mock control-plane smoke; camera/model checks pending |
| [Sentinel / ResearchGuard](https://github.com/Navigatedhustle/sentinel-researchguard) | A research workspace for synthetic policy curricula, strict evidence-conditioned decisions, adapter training and challenge evaluations. | Source syntax checked; research archive |
| [ZGX Demo Center](https://github.com/Navigatedhustle/zgx-demo-center) | A demo catalog and installer/launcher suite with vision, document translation, healthcare, PII, robotics and other examples that share installation and lifecycle tooling. | Source syntax checked; historical integration suite |

## Engineering evidence

Each repository documents its architecture, setup, startup/shutdown, dependencies, model/data acquisition, security boundaries, known limitations and roadmap. Source is separated from model weights, environments, runtime databases, business records and generated outputs. Commit and push hooks scan staged blobs and history with Gitleaks and reject unsafe artifacts.

Tests use synthetic data. Source-only checks and mocked integrations are labeled; no latency, camera, provider operation or model-quality claim is inferred from a scaffold. Jarvis database workflows used a separate ephemeral PostgreSQL instance; the production database was untouched.

## Sharing and licensing

See [public-sharing proposal](docs/PUBLIC-SHARING.md). Existing source/dependency notices remain applicable. No new source license is applied automatically. Model licenses and source ownership are separate; third-party weights, unknown media and original operation records are omitted. Working runtime projects and historical experiments remain local.

## Updating

Work in the runtime project's normal development location, then copy only reviewed source changes into its publication repository. Stage explicit files, run relevant tests, run `python3 scripts/security_check.py --history`, and use `bash scripts/push-private.sh`. Never import original histories or synchronize private data. Details are in each project's SECURITY.md. The local recovery/organization guide is intentionally outside Git.
