# gtc-ml-project1-hotel-bookings
Data cleaning and feature engineering on the Hotel Bookings dataset, including handling duplicates, encoding, and creating new features for ML readiness

2. Data Overview & Quality Assessment
Dataset Structure
Shape: 119,390 rows × 32 columns.
Variables: Cover booking details (arrival date, nights, special requests), financial metrics (ADR), customer demographics (country, children), and booking channels (agent, company).
Quality Checks
Duplicates: 31,992 exact duplicate rows identified.
Justification: Duplicates bias descriptive statistics (e.g., inflated cancellation percentages).
Action: Dropped before visualization.
Missing Values: Present in children, country, agent, company.
children: Imputed with mode; children are key for family travel insights.
country: Missing rows excluded for geographical plots.
agent: Left as “unknown,” representing direct or self-service bookings.
company: Dropped due to extreme sparsity.
Visual Confirmation
Figure A: Missing Values Bar Plot (Seaborn) – showed distribution of NaN counts.
Figure B: Duplicate Records Detection – confirmed large redundancy.
Outcome: The cleaned dataset was representative, unbiased, and ready for EDA.


4. Exploratory Analysis & Insights
3.1 Cancellation Behavior (Figure 1: Cancellation Rate by Hotel Type)
Insight: City Hotels had significantly higher cancellation rates than Resort Hotels.
Justification: City stays are short-term, cheaper, and easily replaced. Resorts require longer planning and greater commitment.
Business Implication: City Hotels should introduce non-refundable options or deposits to protect revenue.

3.2 Seasonality in Bookings (Figure 2: Monthly Booking Trend – Line Plot)
Insight:
Bookings peak in July–August (summer holidays).
Lowest demand in November–February (off-season).
Justification: Summer aligns with school vacations and tourism flows. Winter sees reduced travel.
Business Implication:
Increase staffing & marketing in peak months.
Offer discounts & local events in off-season to stabilize demand.


3.3 Pricing Behavior – ADR (Figure 3: ADR Distribution by Hotel Type – Boxplot)
Insight:
City Hotels: Lower ADR, more volatility.
Resort Hotels: Higher stability, spikes during holidays.
Justification: City Hotels compete in dense urban markets → frequent price changes. Resorts capture holiday tourism → stable but seasonal surges.
Business Implication:
City Hotels → dynamic pricing models.
Resorts → off-season package deals.

3.4 Guest Engagement – Special Requests (Figure 4: Special Requests vs. Cancellation – Countplot)
Insight: Guests with multiple requests are less likely to cancel
Justification: Special requests signal strong booking intent an emotional commitment.
Business Implication: Encourage personalization at booking (e.g., room preferences, meals) → lower cancellations, higher loyalty.


3.5 Lead Time Analysis (Figure 5: Lead Time Histogram)
Insight: Distribution is skewed:
Many last-minute bookings.
Significant portion months in advance.
Justification: Two customer profiles emerge – spontaneous travelers vs. early planners.
Business Implication:
Flash deals & mobile offers for last-minute travelers.
Loyalty discounts for advance planners.

3.6 Geographic Trends (Figure 6: Bookings by Country – Choropleth Map)
Insight: A few countries contribute the majority of bookings (e.g., Portugal, UK, France).
Justification: Travel accessibility, cultural ties, and tourism flows.
Business Implication: Target campaigns in key origin countries with tailored promotions.

3.7 Stay Duration Patterns (Figure 7: Length of Stay by Hotel Type – Violin Plot)
Insight:
City Hotels → shorter stays, typically 1–3 nights.
Resort Hotels → longer vacations (4–10 nights).
Justification: Business vs. leisure motivation.
Business Implication:
Promote weekend offers for City Hotels.
Create extended-stay packages for Resorts.

3.8 Booking Channels (Figure 8: Bookings by Market Segment – Bar Plot)
Insight:
Majority of bookings come through agents and online travel agencies (OTAs).
Agent bookings show higher cancellation rates.
Justification: OTA users book flexibly, cancel when cheaper alternatives appear.
Business Implication: Hotels should:
Negotiate better terms with OTAs.
Incentivize direct bookings via discounts or loyalty points.


4. Strategic Recommendations
From the findings:
Cancellation Risk Management
City Hotels: stricter deposit policies.
Encourage special requests at booking stage.
Demand Forecasting & Seasonality
Focus promotions in off-season months.
Align staffing with monthly peaks.
Revenue Optimizatio
City Hotels: real-ime dynamic pricing.
Resort Hotels: off-season discounts & family packages.
Customer Segmentation & Marketing
Last-minute bookers: flash sales, mobile deals.
Early planners: loyalty-based discounts.
Distribution Strategy
Reduce reliance on OTAs by promoting direct bookings.
Leverage country-level insights for geo-targeted advertising.

5. Conclusion
The analysis of the Hotel Bookings dataset provides a comprehensive view of customer behavior, cancellations, and pricing dynamics. By tying every finding to a visualization and justifying why it matters, the study highlights how data-driven strategies can reduce cancellation risk, optimize pricing, and improve guest satisfaction
