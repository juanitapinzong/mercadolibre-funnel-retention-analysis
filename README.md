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

Example insights (replace with your actual results later):

- The largest drop-off occurs between **add_to_cart and begin_checkout**, suggesting friction during the checkout initiation process.
- Mobile users show lower conversion rates compared to desktop users.
- Paid search generates high traffic but lower purchase conversion.
- Retention drops significantly after **Day 7**, indicating that early engagement is critical for long-term retention.

---

## Dashboard / Results

(Add screenshots of funnel charts or retention cohort tables here)

---

## Author

Juanita Pinzón
