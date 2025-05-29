# TravelTide_v2
Customer Segmentation for TravelTide app

🚀 **Executive Summary:** Travelproject – Personalization and Engagement Strategy Post 04 Jan 2023 up until July 2023
📌 **Objective**
To enhance user engagement and increase conversion by offering personalized perks to travelers based on demographic, behavioral, and transactional patterns derived from post-January 4th, 2023 user activity.

🔍 **User Segmentation Strategy**
The segmentation logic was designed using a **decision-tree-based** approach with key metrics:

Trips completed

User age

Spending habits

Session activity

Family status (children)

Cancellations

Users were filtered to only include those with more than **7 sessions up**, ensuring an engaged cohort for perk optimization.

🧩 Segments and Corresponding Perks
**1. Inactive Users**
Criteria: num_trips = 0

Sub-segments:

No booking: 🟠 **New Buddies**: 50% off first trip

With cancellations: 🟠 **Last-minute cancelers**: Free Cancellations for 30 days

**2. Active Users**
Divided by age:

A. **Younger Travelers** (Age < 30)
With children:

High spenders: 🟠 **Family High Spenders**: Free stay for child

Others: 🟠 **Family Travelers**: Free child ticket

Without children:

3 Trips: 🟠 **Adventurers**: 10% off each additional seat

≤3 Trips: 🟠 **Occasional Travelers**:Complimentary drinks

B. Senior Travelers (Age > 60)
High spenders: 🟠 **Elder Explorers**: Free Meals

Others: 🟠 **Travel-averse seniors**: Support on Senior Services

C. Middle-Aged Travelers (30 ≤ Age ≤ 60)
3 Trips:

High spenders: 🟠 **Premium Travelers**: 20% off + Free Checked Bag

Others: 🟠 **Standard Travelers**: 15% Discount

≤3 Trips: 🟠 **Unseasoned Travelers**: 50% off Premium Subscription

📊 Key Metrics Extracted from SQL Logic
Demographics
Age and age group

Presence of children

Home location (country, city)

Behavioral Metrics
Number of sessions

Page clicks per session

Cancellations

Transactional Metrics
Number of trips

Average spend per trip

Flight/hotel bookings (standalone or combined)

Spending on flights/hotels

Travel distance (haversine metric)

📁 Data Pipeline Highlights (from SQL)
Filtering Sessions: Post-Jan 4, 2023 only; minimum 7 sessions per user.

User Metrics: Derived trip-level, session-level, and monetary metrics for each user.

Perk Assignment: Final CASE logic uses trip count, spending patterns, age group, and family status to assign perk tiers.

📈 Impact Potential
Based on the perk assignment logic:

High-frequency & high-spend segments (e.g., "Premium Travelers", "Family High Spenders") can drive repeat usage and upsells.

Infrequent and price-sensitive users (e.g., “New Buddies”, “Unseasoned Travelers”) receive discounts to encourage first conversions.

Targeted family and senior perks add personalized value based on lifestyle and likely travel behavior.

📌 # Final Output Table (From SQL)
A curated user-level table was produced with:

Demographics, behavioral and transaction metrics

Final assigned perk label

✅ Next Steps
Deploy perks in-app and via email immediately for better impact.

Monitor perk redemption rate and adjust thresholds quarterly.

Consider dynamic thresholds (like top 25% spenders instead of fixed spend amount).

Add tracking for perk impact on next 30-day engagement or spend.
