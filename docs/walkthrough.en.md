# From Nuclear Construction News to Project Records and Engineering Reports

**[English](walkthrough.en.md) · [简体中文](walkthrough.md) · [Product overview](../README.en.md)**

This guide uses real application screenshots and exported outputs captured on 29 October 2026. They show the maintained records at that time, not a live official project-status feed. See the [AI-assisted workflow guide](ai-workflow.en.md) for the division of work between AI, software and users. Screenshots retain the Chinese interface as captured.

## Collect and verify engineering news

![Actual news ledger](../assets/news-workspace.png)

The illustrated Lianjiang backfeed article has separate records for its publication date of 26 October 2026 and engineering event date of 22 October. Software reads and processes the body. When an API is configured, background semantic review assists event, unit and milestone interpretation. Users read and confirm the article. [Original source](https://power.in-en.com/html/power-2480128.shtml).

## Maintain project status after confirmation

![Actual project ledger](../assets/project-status.png)

The Lufeng units shown are at different stages. Confirmation does not necessarily advance a stage: the system must assess whether a milestone occurred and which unit it affects. Valid updates enter the project ledger. Progress charts and the map read the same records, and manual edits also feed these views.

## Visualize progress and export the chart

![Actual progress workspace](../assets/progress-workspace.png)

Users can filter stages, locate units and download a complete image. The following is a direct export from the website's drawing function, including the legend and Note box, rather than a chart recreated with another plotting tool.

![Actual exported construction progress chart](../assets/progress-chart.png)

## Retain regulatory documents

![Actual regulatory archive](../assets/regulatory-archive.png)

Software scans official sources, while AI can assist subject, category and attachment identification. Users can inspect official pages, saved web snapshots and downloaded files, filter categories and use the archive recycle bin. A failed official link does not automatically remove a healthy local copy.

## Select, edit and export engineering reports

![Actual report workspace](../assets/report-workspace.png)

The selected article covers condenser installation at Lufeng Unit 1. Its workspace shows an English lead, months since FCD, a photograph and original evidence. With an API, AI participates in translation correction and engineering editing; users retain control over facts and final content. [Original source](https://power.in-en.com/html/power-2480157.shtml).

![Actual one-page engineering editorial output](../assets/editorial-example-page-1.png)

[View PDF](../examples/lufeng-1-editorial-example.pdf) · [Download Word](../examples/lufeng-1-editorial-example.docx)

This is an individual-article export of existing generated content. Only the public copy's internal header attribution and author metadata were adapted for display; the lead and body were not rewritten. News and photographs remain the property of their respective publishers.

The earlier [fictional formatting example](../examples/engineering-report-demo.pdf) remains clearly separate from the real output. Public materials do not include full databases, API keys or private core code.

[Contact the maintainer](../README.en.md#contact)
