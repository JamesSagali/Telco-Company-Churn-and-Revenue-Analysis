 # Telco Churn & Revenue Analysis Dashboard

## 1. Background and Overview

This project provides a comprehensive analysis of customer churn and its financial impact for a telecom company. The objective is to help business leaders, product managers, and customer experience teams understand **why customers leave**, identify **high-risk segments**, and implement **data-driven strategies to improve retention and maximize revenue**.  

The analysis integrates customer demographics, product usage, billing behavior, and support interactions to provide a holistic view of churn drivers.  

**Key Goals of the Project:**
- Quantify the revenue at risk due to churn and identify high-ticket customers.  
- Understand customer demographics, behavior, and service usage patterns associated with higher churn.  
- Evaluate the impact of support interactions (tech and admin tickets) on churn and revenue.  
- Analyze contract type, billing, and monthly charges to identify financial and behavioral risk factors.  
- Provide actionable recommendations to reduce churn, improve customer retention, and optimize revenue.

**Tools and Technologies Used:**
- **Jupyter Notebooks:** For data cleaning, preprocessing, and exploratory analysis.  
- **Power BI:** For creating interactive dashboards, visualizations, and executive-level insights.  
- **Python Libraries:** Pandas for initial analysis and plotting before visualization.  

**Key Areas of Insight and Recommendations:**
- **Customer Demographics & Churn:** Gender, age, partner/dependent status, and tenure trends.  
- **Product Usage:** Phone, internet, streaming services, and security/backup subscriptions.  
- **Support Services & Ticket Analysis:** Tech and admin tickets, escalation patterns, and revenue impact.  
- **Contract & Billing Behavior:** Contract type, payment methods, monthly charges, and paperless billing.  
- **Revenue & Financial Impact:** Revenue at risk, average monthly charges, and customer lifetime value.  
- **Retention Strategies:** Recommendations for targeted retention, upselling, support optimization, and revenue risk monitoring.  

This project provides both **high-level executive summaries** and **deep-dive insights**, enabling stakeholders to make informed, strategic decisions regarding customer retention and revenue growth.  
 

---

## 2. Data Structure Overview

The dataset for this project was provided in an **Excel file** containing detailed customer, service, billing, and support information. Prior to conducting the analysis, a series of **data quality checks and exploratory inspections** were performed to ensure accuracy, consistency, and familiarity with the dataset. This included checking for missing values, verifying data types, and understanding distributions across key fields.  

**Key Columns in the Dataset:**
- `customerID` – Unique identifier for each customer  
- `gender` – Customer gender  
- `SeniorCitizen` – Whether the customer is a senior citizen (0 = No, 1 = Yes)  
- `Partner` – Whether the customer has a partner  
- `Dependents` – Whether the customer has dependents  
- `tenure` – Number of months the customer has been with the service  
- `PhoneService`, `MultipleLines` – Telephony services  
- `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies` – Internet and additional services  
- `Contract` – Contract type (Month-to-Month, One Year, Two Year)  
- `PaperlessBilling` – Whether the customer uses paperless billing  
- `PaymentMethod` – Payment method for monthly charges  
- `MonthlyCharges` – Customer’s monthly bill  
- `TotalCharges` – Total revenue from the customer  
- `numAdminTickets` – Number of administrative support tickets  
- `numTechTickets` – Number of technical support tickets  
- `Churn` – Whether the customer churned (Yes/No)  


| Field | Description |
|-------|-------------|
| customerID | Unique identifier for each customer |
| gender | Male / Female |
| SeniorCitizen | 1 = Yes, 0 = No |
| Partner | Yes / No |
| Dependents | Yes / No |
| tenure | Months since customer joined |
| PhoneService | Yes / No |
| MultipleLines | Yes / No |
| InternetService | DSL / Fiber optic / No |
| OnlineSecurity | Subscription flag (Yes/No) |
| OnlineBackup | Subscription flag (Yes/No) |
| DeviceProtection | Subscription flag (Yes/No) |
| TechSupport | Subscription flag (Yes/No) |
| StreamingTV | Subscription flag (Yes/No) |
| StreamingMovies | Subscription flag (Yes/No) |
| Contract | Month-to-month / One-year / Two-year |
| PaperlessBilling | Yes / No |
| PaymentMethod | Bank transfer, credit card, electronic check, etc. |
| MonthlyCharges | Monthly subscription fee (USD) |
| TotalCharges | Lifetime charges (USD) |
| numAdminTickets | Number of administrative tickets |
| numTechTickets | Number of technical tickets |
| Churn | Yes / No |

For a detailed record of the **data cleaning, preparation, and exploratory analysis**, please refer to the [Jupyter Notebook](link-to-your-notebook-here).  
This structured approach ensured that all analyses and visualizations in Power BI were based on **clean, reliable, and well-understood data**, allowing for accurate insights and recommendations.

---

## 3. Executive Overview

The dataset covers over 7,000 customers, with a total monthly revenue of $16 million and an overall churn rate of 26.58%. Customer distribution shows peaks at 0 months (new customers) and 72 months (long-tenure), with longer-tenure and two-year contract customers contributing the most revenue. Churn is higher among month-to-month customers, those without partners or dependents, and those lacking protective services, as well as customers with Phone Service or Fiber Optic Internet. Financially, churned customers represent a monthly revenue risk of approximately $140,000, with an average CLV of $2,100 and ARPU of $64.8. Support ticket analysis indicates that high-value, tech-heavy customers submit more tickets, highlighting opportunities for targeted retention strategies.

---

## 4. Insights Deep Dive


## Overview
### a) Tenure Distribution (Customer Mix)
- The largest customer cohort is at 0 months tenure (613 customers), indicating a high volume of new customer onboarding.
- There is also a significant concentration of long-tenured customers at 72 months (362 customers), showing the presence of a stable, loyal customer base.

#### Findings
- The distribution suggests a bimodal pattern: customers either churn very early or stay for a long time.
- Early-stage experience and onboarding quality are critical drivers of long-term retention.

#### Actions
- Strengthen first-90-day onboarding, including proactive support and clearer service education.
- Closely monitor early support tickets as leading indicators of churn.

### b) Tenure vs Revenue Contribution
- Customers with 24+ months tenure contribute 59.4% of total monthly revenue.
- The 7–12 month tenure band contributes the least (9.12%), despite passing initial onboarding.

#### Findings
- Revenue contribution increases significantly with tenure, confirming that retention directly protects revenue.
- Customers who fail to progress beyond the first year represent lost lifetime value.

#### Actions
- Prioritize retention strategies for customers approaching the 6–12 month mark.
- Introduce targeted offers or service interventions to move customers into longer tenure bands.
- Treat long-tenured customers as a revenue protection segment, not just “retained users.”

### c) Contract Type & Tenure
- Customers on 2-year contracts have the longest average tenure, outperforming monthly and shorter-term contracts.

#### Findings
- Longer contract commitments are strongly associated with higher retention and longer customer lifetime value (CLV).
- Contract structure plays a predictive role in churn behavior.

#### Actions
- Incentivize migration to longer-term contracts, especially after the first successful months of service.
- Use usage and support stability signals to identify the right moment to upsell 2-year contracts.

#### Executive Sumamry
- Customer value increases sharply with tenure. Most revenue comes from customers retained beyond two years, while early-tenure customers represent the highest churn risk. Strengthening onboarding, managing early support issues, and promoting longer contracts are key levers for protecting revenue and increasing lifetime value.

  <img width="1323" height="762" alt="image" src="https://github.com/user-attachments/assets/b947b1aa-b5f4-46d4-b9dd-0e8c0bafeee5" />


## Customer Demographics Analysis
### a) Gender vs Churn
- Churn is evenly split between male and female customers, with no meaningful difference in churn rates by gender.

#### Findings
- Gender is not a strong predictor of churn in this customer base.

#### Actions
- Avoid gender-based retention strategies.
- Focus resources on behavioral and lifecycle factors (tenure, contracts, support interactions) instead.

### b) Senior Citizen Status & Churn
- Higher churn is observed among non–senior citizens compared to senior customers.

#### Findings
- Younger or working-age customers appear to be more price-sensitive or more likely to switch providers.
- Senior customers may value stability and are less likely to churn once onboarded.

#### Actions
- Develop flexible plans, bundles, or loyalty incentives targeting non-senior customers.
- Use early churn prediction signals (support tickets, tenure, usage) more aggressively for this segment.

### c) Dependents & Churn
- Customers without dependents show higher churn rates than those with dependents.

#### Findings
- Customers with dependents may have higher switching costs and stronger service reliance.
- Customers without dependents may be less locked-in and more willing to change providers.

#### Actions
- Position value-based or lifestyle-driven offers for customers without dependents.
- Reinforce stickiness through bundles, convenience features, or contract incentives.

### d) Partner Status & Churn
- Customers without partners churn at higher rates than those with partners.

#### Findings
- Partnered customers tend to have greater household dependency and longer-term usage patterns.
- Single customers are more likely to optimize for price or flexibility.

#### Actions
- Target single customers with personalized plans, discounts, or flexible contracts.
- Encourage bundling or add-ons that increase perceived value and switching cost.

#### Executive Summary
- Churn is driven less by gender and more by household stability indicators—customers without partners or dependents, and non-senior customers, are significantly more likely to churn.
  
  <img width="1322" height="744" alt="image" src="https://github.com/user-attachments/assets/e72b4130-1942-4afc-8e6b-ef111fdc6932" />


## Product Usage Analysis
### a) Phone Service & Churn
- Customers with phone service show higher churn compared to those without.

#### Findings
- Phone service subscribers may expect more value or features and switch quickly if dissatisfied.
- Customers without phone service may have simpler needs, leading to more stable retention.

#### Actions
- Evaluate phone service satisfaction and plan offerings.
- Introduce loyalty perks, bundle incentives, or feature upgrades to reduce churn among phone service users.

### b) Internet Service & Churn
- Fiber optic customers account for 64% of churn.
- Churn is lowest among customers without any internet subscription.

#### Findings
- High-end internet subscribers (fiber optic) may have higher expectations or better alternatives.
- Customers without internet are less exposed to competitive options.

#### Actions
- Consider retention campaigns, service quality checks, and value-adds for fiber optic users.
- Explore cross-sell/up-sell opportunities with tailored packages to increase stickiness.

### c) Streaming Services (TV & Movies)
- Churn is balanced among streaming TV and movie subscribers.

#### Findings
- Streaming services do not appear to drive churn independently.
- Likely secondary factor relative to core services like phone and internet.

#### Executive Summary
- Customers lacking key support services—security, backup, device protection, and tech support—exhibit higher churn, highlighting support features as critical levers for retention.

#### Actions
- Focus retention efforts on core subscription services, while using streaming offerings as value-adds.
- Monitor streaming usage for engagement trends that may indicate early churn signals.

#### Executive Summary
- Churn is concentrated among higher-tier subscribers (phone and fiber internet), while streaming services have little impact, highlighting core services as the key levers for retention.

  <img width="1321" height="756" alt="image" src="https://github.com/user-attachments/assets/a3b8f501-f382-4ef8-a925-cd65c6834f51" />


## Support Services Churn Analysis
### a) Online Security & Churn
- Customers without online security are churning more than those with it.

#### Findings
- Lack of security features reduces customer confidence, increasing likelihood of churn.

#### Actions
- Promote online security packages as part of core offerings.
- Educate customers on security benefits to increase perceived value and trust.

### b) Device Protection & Churn
- Higher churn among customers without device protection.

#### Findings
- Absence of protection may make customers feel vulnerable, prompting churn.

#### Actions
- Offer device protection add-ons or bundles, especially targeting at-risk segments.

### c) Online Backup & Churn
- Customers without online backup show elevated churn.

#### Findings
- Lack of backup services reduces overall service stickiness.

#### Actions
- Include online backup incentives in retention campaigns for mid- and high-tier subscribers.

### d) Technical Support & Churn
- Customers without tech support are churning more.

#### Findings
- Access to responsive technical support is critical for retention, particularly among multi-service users.

#### Actions
- Strengthen technical support offerings for at-risk customers.
- Introduce tiered or proactive support programs for users without tech support.

#### Executive Summary
- Customers lacking key support services—security, backup, device protection, and tech support—exhibit higher churn, highlighting support features as critical levers for retention.


  <img width="1317" height="759" alt="image" src="https://github.com/user-attachments/assets/63a20227-5cd6-4cab-a67e-ae8722eb0f22" />


## Contract & Billing Behaviour
### a) Contract Type & Churn
- Highest churn: Month-to-month contracts.
- Lowest churn: Two-year contracts.

#### Findings
- Longer contracts reduce churn and increase stability.
- Month-to-month customers are more sensitive to price and dissatisfaction.

#### Actions
- Incentivize longer-term contracts with discounts or added benefits.
- Focus retention efforts on high-paying, month-to-month customers.

### b) Payment Method & Churn
- Highest churn: Electronic check.
- Lowest churn: Automatic payments via credit card or bank transfer.

#### Findings
- Automatic payments reduce churn risk by increasing convenience.
- Manual payments introduce friction and missed payments.

#### Actions
- Encourage auto-pay adoption.
- Offer incentives for electronic check customers to switch.

### c) Billing Method & Churn
- Higher churn among paperless billing customers.

#### Findings
- Could indicate lower engagement or perceived value among paperless billing users.

#### Actions
- Engage paperless billing customers with proactive retention messaging or value-added communications.

### d) Monthly Charges & Churn
- Month-to-month: Churn rises sharply at $70+ monthly charge (up to 54.6%).
- One-year contracts: Churn increases at $100–110 (25–27%).
- Two-year contracts: Low and stable churn even at higher charges (10% at $100, 4% at $110).

#### Findings
- Shorter contracts are more sensitive to price; longer contracts buffer churn risk.
- Contract length, payment method, and monthly charges are strong predictors of churn: month-to-month and electronic check customers are most at risk, especially at higher monthly charges, while long-term, auto-pay customers remain highly stable.

#### Actions
- Introduce tiered pricing incentives for short-term contract holders.
- Implement personalized retention strategies for high-paying, short-term customers.
- Consider bundling services or loyalty benefits for high-value, short-term customers.

  <img width="1320" height="761" alt="image" src="https://github.com/user-attachments/assets/9b3347cf-af5c-4fb7-aa1f-8529b5e17985" />


## Support & Ticket Analysis

### a) Ticket Volume by Churn Status
- Average tickets:
  - Tech tickets: 1.16 for churned vs 0.15 for retained
  - Admin tickets: 0.47 for churned vs 0.51 for retained

#### Findings
- Churned customers generate significantly more tech tickets than retained customers.
- Admin tickets show little correlation with churn, suggesting tech issues are a stronger driver of customer dissatisfaction.

#### Actions
- Focus on resolving recurring technical issues proactively.
- Analyze patterns in tech tickets to prevent churn among high-value users.

### b) Tech Tickets vs Tenure
- Observation: Churned customers with longer tenure tend to log more tech tickets.
- Retained customers: Tech ticket volume remains low and stable, regardless of tenure.

#### Findings
- Long-tenured churned customers may be experiencing unresolved technical issues over time.

#### Actions
- Implement proactive technical outreach for long-tenured customers with repeated tickets.
- Use predictive analytics to flag high-risk customers based on ticket patterns.

### c) Tech Tickets vs Monthly Charges
- Observation: Churned customers with monthly charges above $90 report more tech tickets.
- Highest average: $110 monthly charge customers with ~4.97 tech tickets.

#### Findings
- High-paying customers are disproportionately affected by technical issues, increasing revenue at risk.

#### Actions
- Prioritize tech support and dedicated interventions for high-value, high-ticket customers.
- Consider personalized support or escalation pathways for customers with large monthly charges.

### d) Revenue Impact by Ticket Bands
- Churned customers with 0 admin tickets: Contribute significantly to revenue loss.
- Churned customers with multiple tech tickets (2–3): Represent higher revenue loss than retained customers within the same ticket bands.

#### Findings
- Even low admin-ticket churners are financially impactful, while multiple tech-ticket churners signal urgent intervention needs.

#### Actions
- Segment customers by ticket type and revenue to target retention initiatives.
- Address recurring tech issues in high-revenue segments proactively.
  
### Executive Summary
- Technical support tickets are a strong predictor of churn and correlate with revenue risk — particularly among high-value, long-tenured customers. Proactive technical support and ticket pattern analysis are key to reducing churn and protecting revenue.

  <img width="1316" height="760" alt="image" src="https://github.com/user-attachments/assets/d9c96691-f9c5-478d-9cc3-d0d8b87d6a75" />



## Revenue & Financial Impact
### a) Overall Revenue at Risk
- Monthly revenue lost due to churn: $140k
- Average monthly charge:
  - Churned customers: $74.44
  - Retained customers: $61.31

#### Findings
- High-paying customers are leaving at a higher rate than low-paying customers, indicating that churn disproportionately affects revenue.

#### Actions
- Prioritize retention strategies for high-value customers.
- Implement targeted campaigns or loyalty incentives for customers with above-average monthly charges.

### b) Service Type Impact
- Phone service churn: Highest revenue impact, losing $132.75k monthly.
- Internet service: Fiber optic subscribers contribute to 82% of revenue loss due to churn.
- Customers without internet subscription: Minimal revenue impact.

#### Findings
- Revenue loss is concentrated among high-value services (phone & fiber optic).
- Service type is a strong predictor of financial risk.

#### Actions
- Strengthen retention initiatives for customers with phone and fiber optic services.
- Monitor service bundles and consider loyalty or discount programs for high-value service subscribers.

### c) Contract Type Impact
- Month-to-month contracts: Account for 86% of monthly revenue at risk (highest).
- Two-year contracts: Minimal revenue loss.

#### Findings
- Shorter-term contracts are financially risky due to higher churn rates.
- Longer-term commitments mitigate revenue exposure.

#### Actions
- Encourage month-to-month customers to move to longer-term contracts with incentives or bundled offers.
- Monitor high-value month-to-month customers closely for early retention interventions.

### d) Customer Lifetime Value (CLV) & Average Revenue
- Average CLV: $2,100
- Average monthly revenue per user: $64.80

#### Findings
- Customers with higher monthly charges represent higher CLV.
- Losing high-CLV customers has a significant long-term financial impact.

#### Actions
- Use CLV to segment customers and prioritize retention efforts.
- Focus churn-reduction strategies on high-CLV customers for maximum ROI.


  <img width="1322" height="758" alt="image" src="https://github.com/user-attachments/assets/664c6e1e-4f63-4a32-b804-46d2986105b5" />

---

## 5. Recommendations

Based on the uncovered insights, the following recommendations have been provided:

- **Strengthen early onboarding:** Focus on the first 90 days with proactive support and service education to reduce early churn. Monitor early technical tickets as leading churn indicators.

- **Protect long-tenured, high-value customers:** Treat customers with 24+ months tenure as a revenue protection segment and prioritize retention at the 6–12 month transition point.

- **Promote longer-term contracts:** Incentivize migration from month-to-month to one- and two-year contracts using service stability, usage consistency, and support history as triggers.

- **Target high-risk customer segments:** Focus retention efforts on non-senior customers and those without partners or dependents, using personalized offers, bundles, and loyalty incentives.

- **Prioritize core services:** Direct retention initiatives toward phone and fiber optic customers, who account for the majority of churn and revenue loss; use streaming services as value-adds.

- **Expand support and protection adoption:** Increase uptake of online security, device protection, backup, and tech support to improve stickiness and reduce churn risk.

- **Optimize billing and payments:** Encourage auto-pay adoption and reduce reliance on electronic checks to minimize payment-related churn.

- **Use support tickets predictively:** Leverage technical ticket volume and recurrence to identify at-risk customers early and intervene before revenue-impacting churn occurs.

  

---

**Dashboard & Visuals**
The Power BI dashboard includes histograms, scatter plots, donut charts, and bar charts for each section above. Visuals support executive-level decision-making and highlight actionable insights.  

---


