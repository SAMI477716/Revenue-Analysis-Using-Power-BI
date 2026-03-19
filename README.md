# Ethiopia Regional Revenue & Social Support Dashboard

## Project Overview
This Power BI project provides a comprehensive analysis of revenue collection and family support distribution across various regions in Ethiopia, including Sidama, South Ethiopia, Central Ethiopia, and South West Ethiopia. The dashboard translates raw transactional data into actionable insights regarding regional performance, seasonal trends, and demographic support reach.

## Key Features & Insights
*   **Revenue Performance:** Tracked a total revenue of **8.97M**, with South Ethiopia contributing the largest share (60.89%).
*   **Geographic Analysis:** Detailed breakdown by Town (Sodo, Hawassa, Arba Minch, etc.) and Region using Treemaps and Donut charts.
*   **Temporal Trends:** Monthly and Quarterly revenue tracking, identifying peak collection periods in Quarter 1 (over 3M).
*   **Social Impact Metrics:** Integration of "Distributed to Families" and gender-based support tracking (Male vs. Female supported) alongside financial data.

## Technical Architecture

### Data Model
The project utilizes a **Star Schema** to ensure optimal performance and filter propagation:
*   **Fact Table (`RevData`):** Contains transactional records including `Revenue collected`, `CollectionDate`, and support metrics.
*   **Dimension Table (`Profile`):** Contains regional metadata, `Town_ID`, and `Revenue Target`.
*   **Relationship:** A One-to-Many (1:*) relationship is established between `Profile` and `RevData` linked via `Town_ID`.

### Data Engineering (Power Query)
*   **Data Cleaning:** Handled date formats and regional naming conventions.
*   **Schema Optimization:** Separated static town profiles from dynamic revenue data to reduce redundancy.

### Visualization Strategy
*   **Waterfall Chart:** Used to visualize the cumulative revenue contribution by region.
*   **Dual Axis Charts:** Compared Revenue Collected against Female Support metrics to observe correlations between economic activity and social aid.
*   **Gauges & KPIs:** Provided high-level "At-a-glance" totals for stakeholder reporting.

## How to Use
1. Clone this repository.
2. Open the `.pbix` file in Power BI Desktop.
3. Use the **Month Slicer** to filter the entire report for specific timeframes.
