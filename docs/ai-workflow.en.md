# Nuclear Construction News Collection and AI-Assisted Engineering Workflows

**[English](ai-workflow.en.md) · [简体中文](ai-workflow.md) · [Product overview](../README.en.md)**

Nuclear Build Log connects the interpretation of engineering information with controlled software execution. AI assists semantic decisions and editorial work; software collects sources, validates evidence, stores traceable records and updates linked views. Users control news confirmation and report adoption. This guide describes the functionality checked on 29 October 2026 and does not disclose private implementation, prompts or credentials.

## 1. From source articles to a verifiable news ledger

1. Scheduled or on-demand collection finds domestic nuclear construction news. Users can also import ordinary web links, import WeChat links or supplement a source with pasted article text. WeChat access-verification cases remain separate until body text is available; the system does not pretend a verification page is an article it has read.
2. Software reads and cleans article bodies, removes identifiable advertising and navigation, and extracts publication dates, body-text dates, candidate units and engineering topics. Publication and event dates are stored separately. An absent event date is not invented from the publication date.
3. Software first handles URL and content duplicates. Unique milestones such as first fuel loading are distinguished from repeatable activities such as equipment deliveries, which require comparison of the equipment, module or work object. When configured, AI can help assess a limited set of ambiguous duplicate candidates, subject to software checks.
4. News enters the ledger, organized by publication month. Users can inspect original evidence, summaries and dates and make corrections. News-card summaries retain their existing program-generated logic; the presence of AI assistance elsewhere does not mean every summary invokes an API.

## 2. From news confirmation to units, charts and the map

Background AI pre-review can cache semantic decisions before a user confirms an article. Confirmation reuses a matching cached decision where available or requests a review when needed. The review asks what the article actually reports, whether the event occurred or is only planned, which units directly participated, which date belongs to that event, whether it represents an applicable milestone, and whether it identifies a genuinely new project.

Software checks that evidence comes from the source, that the date is supported, that the unit matches the evidence and that the result meets the conditions for use. A valid high-confidence AI decision can correct a rule-based result. If the model is unavailable, evidence is invalid or confidence is insufficient, rules supply the fallback. The user receives an update or no-update result without an additional AI approval queue.

For existing units, software applies supported milestones and retains traceable news effects. New units are added when the available evidence and application checks support them. Entirely new sites also need location identification and the applicable verification before mapping. A background event at another unit must not be treated as the current unit's event, and an ordinary structural-module lift must not automatically be treated as a nuclear island dome lift.

The project ledger drives the linked views:

- **Project status** displays engineering stage, reactor type, company, location and milestone dates.
- **Progress visualization** reads dates and stages from the ledger and calculates elapsed time. Planned units are excluded, and commercially operating units do not display ECT.
- **The nuclear project map** uses site locations and unit stages, with selection and positioning by province, site and project. AI assists upstream interpretation; software performs location handling and map rendering.
- Manual additions and edits feed the same views. Automatic changes caused by confirmed news have corresponding notifications; manual maintenance is not presented as an AI discovery.
- Withdrawing news confirmation reverses its corresponding automatic effects, subject to the application's protection of other news evidence and manual edits.

### Engineering terms used in the workflow

| Term | Meaning in the workspace |
| --- | --- |
| FCD | First concrete date used as the start of the construction-duration calculation |
| COD | Commercial operation date used as the duration end date for a commercially operating unit |
| ACT | Actual elapsed duration in months: total elapsed days divided by 30.4375; the end date is the current date or COD as applicable |
| ECT | Planned total construction duration shown as a comparison for eligible units |
| Milestone | A dated engineering event; an event does not necessarily change the unit's overall stage |
| NI / CI | Nuclear island / conventional island and BOP terminology used in engineering reporting |

## 3. Regulatory document identification, classification and retention

The regulatory archive is a separate workflow. Routine checks run every three days and cover documents from 1 January 2025 onward across relevant official columns, paginated lists and document pages of China's National Nuclear Safety Administration and Ministry of Ecology and Environment.

Software first checks dates and candidate content. When an API is configured, AI helps identify whether the subject is a primary nuclear plant or unit, whether the document is an environmental impact assessment report, construction licence or operating licence, and which attachments are relevant in a notice containing multiple projects. Standalone supporting facilities and environmental impact report forms are outside the present scope.

The model cannot create download links or assert that a file exists without evidence. Software checks source and attachment evidence, downloads actual official attachments, validates formats and hashes, retains web snapshots and file versions, and archives material by category. Several notices can reference the same attachment; deleting one notice must not remove a file still referenced by another. Failures are recorded for retry, and an unavailable official link does not automatically delete a healthy local archive.

Here, organizing regulatory information means scoped identification, classification and retention. It does not mean the platform already provides legal interpretation or automatically generated policy analysis.

## 4. From article selection to an engineering editorial report

Users select news in batches from the ledger or import links into an independent report. Software supplies original evidence, engineering dates, unit information, months since FCD and available images. Local translation can provide a draft. With an API, the model corrects translation and produces engineering-focused editorial content, retaining the main engineering message while reducing unrelated organizational, meeting or promotional content.

The model generates titles, leads, body text, keywords, semantic highlighting, captions and image-layout suggestions within the report requirements. Software enforces fonts, title highlighting, lead-box styling and document validation, and provides basic fallbacks. Users can edit facts, engineering dates, text and images before exporting an individual article or complete issue in either engineering editorial or full-translation form.

Exports are ordered by engineering event date, with undated articles last and page breaks between articles. Report edits and generation do not change news confirmation or directly update unit status.

See the [actual exported progress chart](../assets/progress-chart.png) and [Lufeng Unit 1 engineering editorial PDF](../examples/lufeng-1-editorial-example.pdf). The example re-exports existing generated content; its body was not rewritten for the showcase.

## 5. Controls and practical limits

AI calls depend on an available configured API; not every click triggers a request. Background processing, content caches and candidate selection reduce repeated calls. Rule-based paths remain available without an API or during an API failure. Rules and AI reduce errors together, but the platform does not promise exhaustive internet coverage or perfect interpretation of every news article.

Original sources still matter. Access verification, network failures, removed historical attachments and articles without a clear date or unit are practical limitations. The platform preserves sources and evidence to help identify and correct errors rather than presenting model output as official fact.

[Contact the maintainer](../README.en.md#contact)
