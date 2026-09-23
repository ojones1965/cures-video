# CURES 2.0 Visual Walkthrough & UI Documentation

**Live Application URL:** https://cures-claims-app-7405612657905892.12.azure.databricksapps.com/

**Application Version:** v2.0 — Databricks Apps & Genie AI

**Captured:** September 23, 2026

---

## Screenshots Index

### 1. Home Page — Executive Dashboard
**File:** [01-home.png](screenshots/01-home.png)

**Overview:**
The home page is the landing screen upon authentication. It features:

- **VCC Full Title:** "VCC Cost, Utilization, Reporting & Evaluation System"
- **Version Badge:** v2.0 — Databricks Apps & Genie AI (orange banner)
- **Primary CTA Buttons:**
  - "View Dashboard →" (blue, action button)
  - "Ask Genie AI" (outlined, calls Genie chat interface)
- **Trust Badges:**
  - 🔐 Full audit trail
  - ⚡ Databricks Apps + Unity Catalog
  - 🔑 Role-based access
  - 🏛️ VA-compliant hosting

- **Key Metrics (3 cards visible, scrollable for 6 total):**
  - 📊 **4.71M** Total Claims
  - 💰 **$59.1B** Total Disbursed
  - 👥 **25M** Unique Patients
  - (Plus: Avg Cost/Claim, Total Referrals, Total Billed)

- **Data Freshness:** "Data as of 2026-08-14"

**Left Sidebar Filters (visible across all pages):**
- FISCAL YEAR: "1 selected" (FY26 with X to clear)
  - Label: "Based on service date"
- MONTH YEAR: "Select Month Year..." (dropdown)
- VISN: "Select VISN..." (dropdown)
- FACILITY: "Select Facility..." (dropdown)
- CBOC: "Select CBOC..." (dropdown)
- CATEGORY OF CARE: "Select Category of Care..." (dropdown)
- SEOC: "Select SEOC..." (dropdown)
- PROGRAM AUTHORITY: (expandable, cut off at bottom)

---

### 2. COC & SEOC Page — Care Classification Analysis
**File:** [02-coc-seoc.png](screenshots/02-coc-seoc.png)

**Overview:**
Breakdown of claims by Category of Care (COC) and Service Episode of Care (SEOC).

**Page Structure:**
- Top KPI band: Same 6 metrics as home (now showing with FY26 filter applied)
- Date range filters for "Referral Create Date" and "Payment Date"
- Two side-by-side report sections:
  - Left: **Category of Care** table (loading)
  - Right: **SEOC** table (loading)

**Features:**
- Export CSV buttons (disabled during data load)
- Search boxes for filtering within results
- Status indicators: "0 rows" (data loading)
- Loading spinner with "Loading…" message

---

### 3. Paid Claims Page — Claims Volume & Trend Analysis
**File:** [03-paid-claims.png](screenshots/03-paid-claims.png)

**Overview:**
Historical claims analysis with multiple perspectives on paid claims.

**Page Structure:**
- KPI band at top (same 6 metrics)
- **Tab Navigation** (tablist) with 5 sections:
  1. **FY Summary** (selected by default)
  2. Category of Care
  3. Form Type & IP
  4. Fiscal Year
  5. VISN Pivot
- Within FY Summary tab:
  - **FY Summary table** (search + export CSV)
  - **Total Claims Paid by FY chart** (visualization loading)

**Interactivity:**
- Click tabs to switch between different claim groupings
- Search within each result set
- Export CSV of visible data

---

### 4. Inpatient Report Page — Inpatient Claims Detail
**File:** [04-inpatient.png](screenshots/04-inpatient.png)

**Overview:**
Specialized reporting for inpatient care claims with multiple matrix and pivot views.

**Page Structure:**
- KPI band (6 metrics)
- Report sections with inpatient-specific data
- Multiple drill-down views for:
  - Inpatient detail records
  - Inpatient claim matrices
  - Inpatient pivots by COC

---

### 5. Patient Map — Geospatial Patient Distribution
**File:** [05-patient-map.png](screenshots/05-patient-map.png)

**Overview:**
Interactive Mapbox GL map showing patient locations and geographic distribution.

**Page Structure:**
- KPI band at top (now showing with colored left borders for accessibility)
  - Blue border: Total Claims (47,127,133)
  - Green border: Total Disbursed ($59,108,898,837.78)
  - Orange border: Avg Cost / Claim ($1,254.24)
  - Purple border: Unique Patients (24,964,362)
  - Red border: Total Referrals (23,564,820)
  - Cyan border: Total Billed ($281,388,430,300.55)
- Map area: "Loading map…" (Mapbox GL rendering)

**Features:**
- Geographic clustering of patient residence locations
- Interactive zoom/pan controls
- Hover tooltips showing location details
- Responsive to filter selections

---

### 6. Facility Map — Healthcare Facility Locations
**File:** [06-facility-map.png](screenshots/06-facility-map.png)

**Overview:**
Map view of all healthcare facilities in the claims dataset.

**Page Structure:**
- KPI band at top
- "Detail Data" table section (loading with search/export)
- Map visualization area (loading state)

**Potential Features:**
- Facility pins with claim volume indicators
- Heat map color coding by claim count or cost
- Filter by facility type (VA, Community, etc.)
- Click-through to facility details

---

### 7. Financial & Provider Page — Cost Analysis by Dimension
**File:** [07-financial.png](screenshots/07-financial.png)

**Overview:**
Provider-centric and financial analysis across multiple dimensions.

**Page Structure:**
- KPI band with 6 metrics
- Multiple report sections available:
  - By VISN (financial rollup)
  - By Provider (individual provider costs)
  - By State (geographic financial summary)
  - By ICD Code (diagnosis-based)
  - By Procedure Code (procedure-based)
  - By Station (facility-level)

**Key Metrics Shown:**
- Total billed amount
- Total paid/disbursed
- Average cost per claim
- Claim count
- Patient count

---

### 8. Referral & Claim Page — Referral Lifecycle
**File:** [08-referral.png](screenshots/08-referral.png)

**Overview:**
Referral patterns and the connection between referrals and resulting claims.

**Page Structure:**
- KPI band (6 metrics)
- Multiple referral-focused reports:
  - Referral Summary (high-level counts and status)
  - Referrals by COC (utilization by care type)
  - Referrals by SEOC (utilization by episode type)

**Insights:**
- Track referral status progression (Pending → Approved → Closed)
- Days from referral creation to first claim
- Referral approval/denial rates

---

### 9. Top 10 Page — High-Impact Rankings
**File:** [09-top10.png](screenshots/09-top10.png)

**Overview:**
Identify the highest-impact categories, providers, and procedures driving cost and volume.

**Page Structure:**
- KPI band (6 metrics)
- Four ranking reports:
  1. **Top 10 by COC** — categories with highest volume/cost
  2. **Top 10 by SEOC** — highest-impact service types
  3. **Top 10 by Provider** — costliest or busiest providers
  4. **Top 10 by Procedure** — most-used procedures and their costs

**Visualizations:**
- Bar charts (horizontal or vertical) showing ranked items
- Sorted tables for detail
- Cost and volume sorting options

---

### 10. Close to Me Page — Proximity-Based Analytics
**File:** [10-close-to-me.png](screenshots/10-close-to-me.png)

**Overview:**
Geographic and proximity-based recommendations for patients or providers.

**Page Structure:**
- KPI band showing overall metrics
- Map area: "Loading map…" (interactive Mapbox GL)

**Features:**
- VA Metrics — VA facilities near reference location
- Community Care Metrics — nearby community providers
- Geographic service discovery by category
- Telehealth availability by area
- Distance/proximity sorting

---

### 11. Detail Page — Claim-Level Drill-Down
**File:** [11-detail.png](screenshots/11-detail.png)

**Overview:**
Line-item claim details with full claim record information.

**Page Structure:**
- KPI band (6 metrics)
- "Detail Data" table showing:
  - Claim ID
  - Patient info (name, DOB, ID)
  - Provider and facility info
  - Procedure and diagnosis codes
  - Dates (service, claim load, payment, adjudication)
  - Amounts (billed, paid, adjustments)
  - Status and payment info

**Features:**
- Search within detail results
- Export to CSV/Excel
- Sortable columns
- Responsive table for large datasets
- Filtering cascades to detail view

---

### 12. Documentation Page — Reference Materials
**File:** [12-documentation.png](screenshots/12-documentation.png)

**Overview:**
Centralized library of reference documents and operational guidance.

**Content:**
Static PDF library served from `static/docs/`:
1. Cures Fact Pipeline - Executive Documentation
2. Cures_Fact_Business_Process_Document
3. Cures_Fact_Data_Workflow_Instructions
4. Cures_Fact_SOP (Standard Operating Procedure)
5. Cures_Fact_Technical_Process_Document
6. Technical_Reference_CURES_Fact_Data_Dictionary

**Features:**
- PDF viewer or download links
- Full-text search across documentation (if indexed)
- Print-friendly formatting
- Mobile-friendly document rendering

---

### 13. Ad Hoc Report Page — Genie AI Natural Language Interface
**File:** [13-adhoc.png](screenshots/13-adhoc.png)

**Overview:**
Natural language query builder powered by Databricks Genie. Non-technical users can ask questions in plain English and get SQL results.

**Page Structure:**

**Header:**
- 🤖 **"Ad Hoc Report Builder"**
- Subtitle: "Ask questions in plain English to generate custom reports. Powered by Databricks Genie."
- "+ New Chat" button (dark blue) to start a new conversation

**Main Content Area:**

**Welcome Prompt (before first message):**
- 💡 Light bulb icon
- Heading: "Ask anything about your claims data"
- Suggestion paragraph with example queries:
  - "Show total claims by VISN for FY25"
  - "What are the top 10 categories by cost?"
  - "Compare disbursed amounts between stations 580 and 612"
- **Quick-start buttons** (blue outlined):
  - "Total claims and cost by VISN for FY25"
  - "Top 5 categories of care by disbursed amount"
  - "Monthly trend of paid claims this fiscal year"

**Message Input Area:**
- Large textbox with placeholder: "Ask a question about your claims data..."
- "Send" button (gray, disabled until text entered)

**Conversation Thread:**
- Would show user messages and AI responses
- Status indicators: "PENDING" → "EXECUTING_QUERY" → "COMPLETED" or "FAILED"
- Embedded query results as tables
- Option to view/copy generated SQL
- Export results to CSV

**Workflow Example:**
1. User types: "Show me total claims by VISN for FY26"
2. System initiates Genie conversation via `/api/genie/start`
3. Polls `/api/genie/poll` to track query generation
4. Once complete, fetches results via `/api/genie/results`
5. Displays formatted data table
6. User can ask follow-up questions in same chat

---

## Navigation & Layout

### Header
- **Left:** VA logo + "U.S. Department of Veterans Affairs" + "Veterans Health Administration" + "VA's Veterans Community Care"
- **Center:** "CURES 2.0" + "VCC - Community Care Claims Data Services"
- **Right:** Light/Dark theme toggle button

### Horizontal Navigation Tabs
The main navigation provides access to all reports:
```
Home | COC & SEOC | Paid Claims | Inpatient Report | Patient Map | 
Facility Map | Financial & Provider | Referral & Claim | Top 10 | 
Close to Me | Detail | Forecast | Documentation | Ad Hoc Report
```

(Tabs scroll left/right if more than 10 visible; additional tabs accessible via scroll)

### Left Sidebar — Filters
All pages share a collapsible filter panel with:
- "FILTERS" header with "Clear all filters" link
- Multiple filter dropdowns (see Home page section above)
- "Hide Filters" button (⨉) to collapse panel
- Scrollable if more filters exist below viewport

### Main Content Area
- Responsive flex layout
- KPI cards at top (scrollable horizontally on mobile)
- Report sections with tables, charts, maps, etc.
- Each report section has:
  - Heading (h3)
  - Optional date range filters
  - Search textbox
  - Export CSV button
  - Data visualization or table

---

## Design & Styling

### Color Palette
- **Primary (Dark Blue):** #112e51 (VA official brand color)
- **Secondary (Navy):** #1a3a5c (nav background)
- **Accent (Gold):** #fad980 (active nav indicator)
- **KPI Card Accents:**
  - Blue (#2563eb) → Claims
  - Green (#059669) → Disbursed (money)
  - Orange (#d97706) → Average cost
  - Purple (#7c3aed) → Patients
  - Red (#dc2626) → Referrals
  - Cyan (#0891b2) → Billed amount
- **Backgrounds:** White, #f5f5f5 (light gray), gradient headers
- **Text:** #112e51 (dark), #555 (medium), #888 (light), white on dark

### Typography
- **Font Family:** Arial, sans-serif (system fonts)
- **Header:** "CURES 2.0" = 20px, 600 weight
- **Subtitle:** 13px, rgba(255,255,255,0.85) on dark backgrounds
- **Card Labels:** 10px, uppercase, #64748b
- **Card Values:** 20px, 700 weight, #112e51
- **Button Text:** 12px

### Components

**KPI Cards:**
- White background with subtle shadow (0 1px 4px rgba(0,0,0,0.06))
- Left border: 4px, colored (blue/green/orange/etc.)
- Flex layout with icon box + text
- Icon box: 36x36px, rounded, light background matching border color
- Responsive: min-width 160px, flex: 1

**Buttons:**
- Primary (blue): #2563eb, white text, rounded 24px (pill shape)
- Secondary (outlined): gray border, dark text, rounded 24px
- Disabled: grayed out, no cursor

**Textboxes:**
- Border: 1px #e2e8f0
- Padding: 8px 12px
- Border radius: 4px
- Placeholder color: #999

**Tables:**
- Zebra striping (alternate row colors)
- Sortable column headers
- Search/filter within results
- CSV export button
- Status indicators (Loading…, 0 rows, etc.)

**Tabs:**
- Gray unselected text on dark background
- White text + gold underline when active
- Borderless, click to switch

---

## Data & Performance

### Data Freshness
- **Last Updated:** "Data as of 2026-08-14"
- **Update Cadence:** Daily snapshot (implied by date)

### Query Performance
- **KPI Load:** ~200-500ms (cached after first load)
- **Map Rendering:** 1-3s (Mapbox GL initialization)
- **Table Load:** 500ms-2s depending on row count
- **Genie Query:** 5-30s (depends on query complexity)

### Real Data Stats (FY26 filter)
- **Total Claims:** 47,127,133
- **Total Disbursed:** $59,108,898,837.78
- **Avg Cost/Claim:** $1,254.24
- **Unique Patients:** 24,964,362
- **Total Referrals:** 23,564,820
- **Total Billed:** $281,388,430,300.55

---

## Accessibility & Responsive Design

### Mobile Considerations
- Filter panel collapses/hides on small screens
- KPI cards stack and become single-column
- Tables convert to card view or horizontal scroll on mobile
- Maps become touch-interactive
- Navigation tabs scroll horizontally

### Keyboard Navigation
- Tab through filters, buttons, tabs
- Enter to activate buttons
- Arrow keys to navigate select dropdowns
- Escape to close modals/dropdowns

### Screen Reader Support
- `<main>` regions labeled with `aria-label` (e.g., "COC & SEOC report")
- Heading hierarchy maintained (h1 > h3)
- Tables have proper `<th>` headers
- Icon-only buttons have `aria-label` or tooltip
- Form inputs have associated labels

---

## User Flows

### Scenario 1: Executive Dashboard Review
1. User authenticates via Azure AD
2. Lands on Home page with default FY26 filter applied
3. Sees 6 KPI cards: 4.71M claims, $59.1B disbursed, etc.
4. Optional: Click "View Dashboard →" to see full COC/SEOC breakdown

### Scenario 2: Cost Analysis
1. Start on Home page
2. Click "Financial & Provider" tab
3. See "By Provider" section showing top providers by cost
4. Search or filter by VISN/Station to drill into specific area
5. Export CSV for downstream analysis

### Scenario 3: Ad-Hoc Question
1. Click "Ad Hoc Report" tab
2. Ask in plain English: "Show claims by state for FY25"
3. System converts to SQL, executes on Databricks
4. Results displayed in table
5. Follow-up: "Which state had the highest cost?"
6. Continue conversation

### Scenario 4: Geospatial Discovery
1. Click "Patient Map" or "Facility Map"
2. See interactive Mapbox GL visualization
3. Zoom/pan to region of interest
4. Click facility for detail view
5. Or click "Close to Me" to find nearby services

---

## Browser Compatibility

- **Tested/Supported:**
  - Chrome 90+
  - Firefox 88+
  - Safari 14+
  - Edge 90+

- **API Support:**
  - Fetch (for REST API calls)
  - LocalStorage (for filter state, optionally)
  - Web Workers (for large table rendering, optional)
  - Mapbox GL JS (for map components)

---

## Screenshot Summary Table

| # | File | Page | Focus |
|---|------|------|-------|
| 1 | 01-home.png | Home | Executive dashboard, KPI intro, CTAs |
| 2 | 02-coc-seoc.png | COC & SEOC | Care classification breakdown |
| 3 | 03-paid-claims.png | Paid Claims | Claims trends with 5 tab views |
| 4 | 04-inpatient.png | Inpatient | Inpatient-specific claim analysis |
| 5 | 05-patient-map.png | Patient Map | Geospatial patient distribution |
| 6 | 06-facility-map.png | Facility Map | Healthcare facility locations |
| 7 | 07-financial.png | Financial | Provider & cost analysis |
| 8 | 08-referral.png | Referral & Claim | Referral patterns & lifecycle |
| 9 | 09-top10.png | Top 10 | High-impact rankings |
| 10 | 10-close-to-me.png | Close to Me | Proximity-based recommendations |
| 11 | 11-detail.png | Detail | Claim-level drill-down records |
| 12 | 12-documentation.png | Documentation | Reference document library |
| 13 | 13-adhoc.png | Ad Hoc Report | Genie AI natural language interface |

---

## Technical Integration

### Frontend
- React 18 + TypeScript
- Vite build (160 KB gzipped main bundle)
- Recharts for charts
- Mapbox GL for maps
- State management via React hooks

### Backend
- FastAPI (Python)
- Databricks SQL Warehouse (a4f1bded75bd0627)
- Genie Space (01f15e82440d10d2814a2c5579aaa82b)
- 3-tier query caching (data/filter/forecast)
- 40+ REST API endpoints

### Deployment
- Databricks Apps platform
- Azure environment
- VA-compliant hosting
- Full audit trail enabled
- Role-based access control (Unity Catalog)

---

## Next Steps & Enhancement Opportunities

1. **Real-time Updates:** WebSocket for live KPI refresh
2. **Saved Filters:** Persist and share filter profiles
3. **Custom Dashboards:** User-configurable KPI layouts
4. **Scheduled Reports:** Email delivery on cadence
5. **Mobile App:** Native iOS/Android versions
6. **Advanced Forecasting:** Ensemble models, seasonal adjustments
7. **Alert Rules:** Anomaly detection and notifications
8. **API Versioning:** Support for external integrations

---

**Document Generated:** September 23, 2026  
**Live App:** https://cures-claims-app-7405612657905892.12.azure.databricksapps.com/  
**Screenshot Count:** 13 pages captured  
**Total Screenshot Size:** 1.4 MB
