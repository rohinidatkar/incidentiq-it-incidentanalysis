# IncidentIQ: IT Incident Management Analysis

Analysis of an ITSM incident event log by **priority, impact, assignment group and contact channel**, with SLA compliance (`made_sla`), routing and reassignment analysis, resolution times and knowledge-base recommendations.

**Skills demonstrated:** ITSM incident analysis, SLA compliance, ticket routing, contact-channel analysis, recurring-incident analysis, Python and Pandas.

## Data

The notebook expects the incident event log at `data/incident_event_log.csv`. It is not included in this repository. It was written for the public *Incident management process enriched event log* dataset (141,712 event records).

## How to run

```bash
pip install -r requirements.txt
# put incident_event_log.csv in the data/ folder
jupyter notebook incidentiq_it_incident_analysis.ipynb
```

Choose **Run All**. Every table and chart is produced from your data, and the charts are saved to `charts/`.

## What the notebook produces

- SLA compliance overall, **per record and per unique incident**
- SLA by priority, impact, contact channel and the top 10 assignment groups
- Effect of reassignments on SLA (routing)
- Resolution time by priority
- Most frequent incident types (knowledge-base candidates) and SLA with and without a knowledge-base article
- Findings and recommendations generated from the results

## Note on records vs incidents

An event log has several rows per incident. The headline SLA figure depends on whether it is counted per record or per unique incident, so the notebook reports both. When you quote a figure (for example "about 93.5% met SLA"), check which basis it comes from and say so.
