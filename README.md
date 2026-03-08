# MercadoLibre Funnel & Retention Analysis (SQL)

## Project Overview

In this project, I act as a Product Analyst at MercadoLibre within the Growth & Retention team.

The goal of the analysis is to understand where users drop off in the purchase journey and evaluate how well the platform retains users over time.

Using SQL, I analyzed event-level data to build a multi-step conversion funnel and calculated retention cohorts to identify opportunities to improve user growth and engagement.

---

## Business Questions

1. Where do we lose the most users in the purchase funnel?
2. What are the conversion rates between each step of the funnel?
3. How does the funnel performance vary by country, device, and traffic source?
4. How well do we retain users after signup (D7, D14, D21, D28)?
5. How does retention vary across different countries?

---

## Dataset

Two main datasets were used:

### mercadolibre_funnel
Contains user events during the purchase journey.

Key fields:
- user_id
- session_id
- event_name
- event_date
- country
- device_category
- platform
- referral_source
- product_cat
- price

### mercadolibre_retention
Tracks user activity after signup.

Key fields:
- user_id
- signup_date
- activity_date
- day_after_signup
- active
- country
- device_category
- platform

---

## Tools

- SQL
- Funnel analysis
- Cohort retention analysis
- Data aggregation and CTEs

---

## Funnel Stages

The analysis focused on the following conversion funnel:

1. first_visit
2. select_item / select_promotion
3. add_to_cart
4. begin_checkout
5. add_shipping_info
6. add_payment_info
7. purchase

---

## Methodology

1. Explored the dataset and validated event structure.
2. Built a multi-step funnel using SQL CTEs.
3. Calculated user counts and conversion rates between funnel stages.
4. Identified the largest drop-off points in the purchase journey.
5. Built retention cohorts to analyze user activity over time.
6. Calculated retention rates for D7, D14, D21 and D28.
7. Analyzed differences by country, device, and referral source.

---

## Key Insights

### Funnel Performance

The largest drop-off in the purchase funnel occurs between **select_item and add_to_cart**.

- 76.9% of users select a product.
- Only 11.0% add a product to the cart.

This represents a drop of **−65.9 percentage points**, indicating significant friction between product consideration and purchase intent.

Final purchase conversion is relatively low at approximately **1.25% of users reaching purchase**.

Conversion performance also varies across countries:

- **Mexico (2.48%)** and **Peru (1.82%)** show the highest purchase conversion.
- **Brazil (0.68%)** shows weaker conversion.
- **Colombia and Ecuador reach the payment stage but do not convert to purchase.**
- **Paraguay shows no conversions after checkout.**

This suggests that checkout, payment options, and logistics may be key friction points in several markets.

---

### Retention Insights

User activation is strong during the first week but declines rapidly afterward.

Retention rates for users registered between Jan 1 and Jun 1:

- **D7:** 86%
- **D14:** 55%
- **D21:** 25%
- **D28:** 2.6%

This indicates that while users initially engage with the platform, **long-term engagement drops sharply after the second week**.

Retention patterns are similar across countries, suggesting that the main issue is **product experience rather than market-specific behavior**.

Countries with slightly stronger long-term retention include:

- **Peru (3.2%)**
- **Mexico (3.1%)**

---

### Business Recommendations

Based on the analysis, the most impactful improvement would be optimizing the transition between **select_item → add_to_cart** by:

- improving product page clarity
- displaying shipping costs earlier
- strengthening trust signals (reviews, guarantees)

To improve retention, the platform should focus on **post-signup engagement between Day 7 and Day 21**, using:

- personalized recommendations
- second-purchase incentives
- remarketing campaigns

---

## Dashboard / Results

(Add screenshots of funnel charts or retention cohort tables here)

---

## Author

Juanita Pinzón
