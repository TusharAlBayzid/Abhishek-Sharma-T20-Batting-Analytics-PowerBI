# 🏏 Abhishek Sharma: Deep Post-Mortem Analytics Dashboard

## 📌 Project Overview
This project is an interactive, highly visual Data Analytics dashboard developed using Microsoft Power BI to evaluate a spectacular T20 batting performance by Abhishek Sharma. By processing and modeling raw delivery-by-delivery match data, this dashboard extracts actionable insights regarding his scoring zones, momentum across overs, and a highly advanced breakdown of how he handles specific bowling speeds and variations.

## 📊 Dashboard Elements & Deep Analysis

### 1. Executive KPI Cards (Top-Level Metrics)
Provides instant, executive-level metrics summarizing the explosive innings:
*   **Ball Playing (35):** Total deliveries faced.
*   **Run (108):** Total runs accumulated.
*   **Total 6s (11) & Total 4s (8):** Boundary count highlighting sheer aggression.
*   **Boundary Runs (98):** Shows that 90%+ of his runs came strictly from boundaries.
*   **Strike Rate (308.57):** The ultimate indicator of his destructive pacing.
*   **Dot Balls (8):** A surprisingly low number of un-scored deliveries for such a high-risk innings.

### 2. Comprehensive Visual Insights
*   **Scoring Zones (Donut Chart):** Acts as a 360-degree wagon wheel. It breaks down run distribution across different fielding positions (e.g., Mid On, Cow Corner, Deep Square Leg), highlighting where the batter is most lethal.
*   **Runs Against Bowlers (Bar Chart):** A direct comparative analysis identifying which specific bowlers were targeted the most (e.g., Trent Boult vs. R Ashwin), allowing for opposition strategy evaluation.
*   **Innings Momentum (Area Chart):** Maps the flow of runs over-by-over. It visually demonstrates the phases of play—whether the batter capitalized on powerplay fielding restrictions or accelerated during the death overs.
*   **Shot Control Analysis (Pie Chart):** Evaluates batting risk and execution. By categorizing shots into 'Perfect', 'Mishit', 'In Control', and 'Beaten', it proves whether the high score was a result of calculated striking or lucky edges.
*   **Pace vs Spin: Speed & Wicket Analysis (Custom Line & Clustered Column):** The masterclass visual of this dashboard. It dynamically maps runs scored and balls faced across grouped speed buckets (80 kmph to 150 kmph), separated by bowler type (Spin vs. Pace). Furthermore, it features a custom overlay to pinpoint the exact speed and bowler type that resulted in the batter's wicket.

## 🛠️ Technical Challenges & Solutions

During the development phase, I tackled several advanced data modeling challenges:

**1. Dynamic Speed Bucketing (Categorical Grouping):**
*   **Problem:** Raw data provided exact speeds (e.g., 141 kmph, 83 kmph), making it impossible to see macro-trends against fast vs. slow bowling.
*   **Solution:** Authored a robust custom DAX `SWITCH` statement to group continuous speed data into distinct analytical buckets (e.g., "80-90 (Spin)", "141-150 (Pace)"), creating a sorted, logical axis for comparative analysis.

**2. Visualizing Multi-Dimensional Event Data (Wicket Pinpointing):**
*   **Problem:** Needed to highlight exactly when and how the batter got out within a complex combo-chart, without disrupting the runs/balls visuals.
*   **Solution:** Implemented an advanced DAX measure (`Wicket_Mark`) that calculates the exact coordinate of a dismissal event. Applied this measure as a transparent line with a high-visibility Red Marker overlay directly on the specific speed bucket column.

**3. UI/UX & Thematic Design:**
*   **Problem:** Standard white dashboards fail to deliver a premium sports-broadcasting feel.
*   **Solution:** Designed a custom dark-mode theme utilizing neon and pastel hex codes (Magenta, Cyan, Gold) for maximum contrast. Integrated a transparent player cutout and glowing KPI cards for an immersive, executive-level aesthetic.

## 📁 Repository Contents

*   `Abhishek Sharma.pbix` : The fully functional Power BI dashboard containing the data model, DAX measures, and interactive visuals.
*   `Abhishek Sharma's Dashboard.png` : High-resolution screenshot of the final UI.
*   `Abhishek Sharma.pdf` : A static PDF export for quick executive review.
*   `Abhishek_Sharma_Deep_Analysis.xlsx` : The raw, delivery-by-delivery dataset utilized for this data modeling project.

## 👨‍💻 Author

**Bayzid Mostak**
*Data Analyst & Visualization Expert*

*   [LinkedIn] https://www.linkedin.com/in/bayzid-mostak-data-analyst/
*   [GitHub] https://github.com/TusharAlBayzid
*Note: Download the `.pbix` file and open it in Power BI Desktop to experience the fully interactive cross-filtering capabilities of this dashboard.*
