# CURES 2.0 Video Script

**Format:** Executive product overview and guided application tour  
**Target length:** 5:30-6:00  
**Audience:** VA leadership, program managers, analysts, and technical stakeholders  
**Narration style:** Clear, confident, and factual  
**Visual assets:** Existing files in `screenshots/`

## Production Notes

- Use slow pans and subtle zooms on screenshots rather than static frames.
- Highlight the active page, key metrics, filters, and calls to action as they are mentioned.
- Keep on-screen text brief. Do not duplicate the full narration.
- Mask or crop any patient-level information if live data is shown during production.
- Use captions throughout and provide an audio-described version when required.

## Script

### Scene 1 - Opening (0:00-0:20)

**Visual:** VA title card. Fade into `screenshots/01-home.png`, with a slow push toward the CURES 2.0 heading.

**On-screen text:**

> CURES 2.0  
> Community Care Utilization & Reporting Enterprise System

**Narration:**

> Community care claims contain the information leaders need to understand utilization, manage cost, and improve access. CURES 2.0 brings that information together in one secure analytics experience, built for the scale and complexity of VA community care.

### Scene 2 - Mission and Scale (0:20-0:50)

**Visual:** Continue on `screenshots/01-home.png`. Highlight the KPI cards one at a time, then briefly show the left filter panel.

**On-screen text:**

> Claims | Cost | Patients | Referrals

**Narration:**

> The home page gives executives and operational teams an immediate view of the claims portfolio. Current dashboard metrics represent more than 47 million claims, 59.1 billion dollars disbursed, nearly 25 million unique patients, and more than 23 million referrals. Shared filters let users focus the entire application by fiscal year, VISN, facility, category of care, service episode, and other business dimensions.

### Scene 3 - Care and Claims Analysis (0:50-1:25)

**Visual:** Cross-dissolve from `screenshots/02-coc-seoc.png` to `screenshots/03-paid-claims.png`. Zoom into the report tabs, search control, and CSV export action.

**On-screen text:**

> Understand utilization from multiple perspectives

**Narration:**

> CURES organizes utilization by Category of Care and Service Episode of Care, helping teams see where services are delivered and where demand is concentrated. The Paid Claims workspace adds year-over-year trends, claim form and inpatient comparisons, fiscal-year summaries, and VISN-level pivots. Search, sorting, and CSV export make each view useful for both rapid review and deeper analysis.

### Scene 4 - Inpatient Insight (1:25-1:45)

**Visual:** Show `screenshots/04-inpatient.png`. Pan from the KPI band into the inpatient report area.

**On-screen text:**

> Dedicated inpatient reporting

**Narration:**

> A dedicated inpatient workspace provides detailed records, summary matrices, and care-category pivots. Analysts can compare claim volume, billed and paid amounts, patient counts, and average cost while retaining the same filters used throughout the application.

### Scene 5 - Geographic Access (1:45-2:20)

**Visual:** Move through `screenshots/05-patient-map.png`, `screenshots/06-facility-map.png`, and `screenshots/10-close-to-me.png`. Use map-pin callouts and a subtle route animation between locations.

**On-screen text:**

> See where care is needed and delivered

**Narration:**

> Geographic views turn claim activity into a picture of access. Patient and facility maps reveal patterns by location, while Close to Me reporting compares nearby VA and community care options. Together, these views help users evaluate service availability, identify geographic concentrations, and consider telehealth where distance may create barriers.

### Scene 6 - Financial Drivers (2:20-2:55)

**Visual:** Show `screenshots/07-financial.png`, followed by `screenshots/09-top10.png`. Highlight provider, state, diagnosis, procedure, and ranking areas.

**On-screen text:**

> Find the drivers behind cost and volume

**Narration:**

> Financial and provider reporting explains what is driving the totals. Users can analyze billed and disbursed amounts by VISN, provider, state, diagnosis, procedure, or station. Top 10 views then surface the categories, service episodes, providers, and procedures with the greatest impact, making priorities and outliers easier to identify.

### Scene 7 - Referral Lifecycle (2:55-3:20)

**Visual:** Show `screenshots/08-referral.png`. Animate a simple sequence: Referral, Care, Claim, Payment.

**On-screen text:**

> Referral > Care > Claim > Payment

**Narration:**

> Referral and claim reporting connects authorization activity to downstream utilization. Teams can review referral volume and status, compare activity by category or service episode, and better understand the path from referral creation through claim payment.

### Scene 8 - Detail and Documentation (3:20-3:50)

**Visual:** Transition from `screenshots/11-detail.png` to `screenshots/12-documentation.png`. Highlight table controls, then the document library.

**On-screen text:**

> Traceable detail. Shared definitions.

**Narration:**

> When summary metrics require investigation, the Detail workspace provides claim-level drill-down with dates, codes, providers, facilities, and financial fields. A centralized documentation library keeps executive guidance, business processes, standard operating procedures, workflows, and the data dictionary close to the analysis.

### Scene 9 - Genie AI (3:50-4:35)

**Visual:** Show `screenshots/13-adhoc.png`. Type the example prompt on screen: "Show total claims by VISN for FY25." Animate the status from pending to executing query to completed, then reveal a representative results table.

**On-screen text:**

> Ask questions in plain English

**Narration:**

> CURES 2.0 also opens ad hoc analysis to users who do not write SQL. In the Genie-powered report builder, a user can ask, "Show total claims by VISN for fiscal year 2025," or, "What are the top categories by disbursed amount?" Genie interprets the question, generates and executes the query, and returns structured results. Follow-up questions turn one report into a continuing analytical conversation.

### Scene 10 - Architecture and Performance (4:35-5:05)

**Visual:** Replace the application view with a clean architecture animation: Browser to React application to FastAPI to Databricks SQL Warehouse and Unity Catalog. Add Genie AI beside the warehouse. Show three small cache labels.

**On-screen text:**

> React + FastAPI + Databricks

**Narration:**

> Behind the experience is a Databricks-native architecture. A React and TypeScript interface communicates with a FastAPI service, which executes governed queries through a Databricks SQL Warehouse and Unity Catalog. Three caching tiers accelerate reports, filter options, and forecast workloads while reducing repeated warehouse computation.

### Scene 11 - Security and Governance (5:05-5:30)

**Visual:** Show the home-page trust badges, then display simple icons for identity, audit, and governed data access.

**On-screen text:**

> Workspace identity | Auditability | Governed data

**Narration:**

> Authentication is delegated through the Databricks workspace, with data governance supported by Unity Catalog and platform audit logging. This model keeps credentials out of the application while supporting controlled access to sensitive healthcare and financial information.

### Scene 12 - Closing (5:30-5:55)

**Visual:** Return to `screenshots/01-home.png`, then montage the map, financial, and Genie pages. End on the CURES 2.0 title card.

**On-screen text:**

> CURES 2.0  
> From claims data to actionable insight

**Narration:**

> From executive KPIs to claim-level detail, geographic access, financial drivers, and natural-language exploration, CURES 2.0 gives VA teams one place to understand community care. It turns claims data into timely, governed, and actionable insight for the people responsible for planning and delivering care.

## Optional End Card

**On-screen text:**

> CURES 2.0  
> VCC Community Care Claims Data Services  
> Powered by Databricks Apps and Genie AI

**Audio:** Music resolves and fades out over two seconds.