# Spotify Chart Analytics
### Power BI · Music Analytics · Report Design

A Power BI portfolio project for exploring a music-chart dataset. The repository combines the report, source data, a business requirements document, and design assets so reviewers can inspect both the analytical deliverable and its supporting material.

## Explore

| Asset | Review purpose |
| --- | --- |
| [Spotify Dashboard.pbix](Spotify%20Dashboard.pbix) | Open the report and inspect its pages, model, and measures |
| [Source CSV](spotify-top-50-world.csv) | Review the supplied chart dataset |
| [Business requirements](Bussiness%20Requirements.docx) | Compare intended questions with report coverage |
| [Design image](Group%2012.png) | Inspect the accompanying visual asset |

## Analytical approach

Start by establishing the source grain: a track, a track on a chart date, and a track in a market are different units of analysis. Confirm the actual columns before defining popularity, ranking, or trend measures.

Repeated appearances of the same track can be valid observations. Track names alone are unsafe identifiers when remixes, collaborations, or different releases are present. Chart position is an ordinal measure; summing ranks does not produce a meaningful popularity KPI.

## Reproduce and review

1. Download the repository and open the requirements document.
2. Open the PBIX in Power BI Desktop.
3. Inspect Power Query and update source paths to the supplied CSV.
4. Confirm data types, date coverage, track identifiers, and relationships.
5. Refresh and compare report totals with the loaded dataset.
6. Test filters and document how chart appearances differ from distinct tracks.

## Quality and reporting checks

- Check missing identifiers and unexpected duplicates at the confirmed source grain.
- Separate missing chart observations from zero values.
- Record date coverage and refresh timestamp.
- Compare rankings under identical date and market filters.
- Use a documented tie rule for top-N displays.

## Current scope and next steps

A PBIX, dataset, requirements file, and design image are available. Internal measures and report behaviour have not been independently runtime-tested in this documentation refresh. This project does not claim a live Spotify API integration or a published service.

Next improvements: export measure definitions, add a labelled dashboard screenshot, map each requirement to a report page, and document the data source and reuse terms.

---
[Explore the full Power BI, Fabric & Data Engineering portfolio](https://github.com/Osama-data/Power-Bi-Projects)
