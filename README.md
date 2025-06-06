# 🚀 Executive Summary: Travelproject – Customer Segmentation & Rewards Program
Travelproject aims to increase user engagement and conversion rates through personalized perks tailored to user demographics, behavior, and spending patterns. By analyzing post-January 4th, 2023 user activity, a decision-tree-based segmentation framework was designed to strategically assign perks that resonate with user needs and travel habits.

# 🎯 Objective
To enhance engagement and boost booking conversions by targeting active and inactive users with contextual perks based on behavioral and transactional insights.

# 🔍 Segmentation Strategy
Users with more than 7 sessions were considered for analysis. Key segmentation dimensions included:

Trip Frequency
Age Group
Spending Behavior
Family Status (Children)
Cancellations

A rule-based decision tree was used to define personalized segments and perks.

# 🧩 Segment-Based Perks
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

# 📊 Key Metrics Computed
Demographics: Age, children, home city/country
Behavioral: Sessions, page clicks, cancellations
Transactional: Spend on hotels/flights, number of trips, avg. trip spend, travel distance (haversine metric)

# 🧮 SQL Logic Summary
A robust SQL pipeline was built to:
1. Filter relevant sessions (post-Jan 4, 2023, >7 sessions)
2. Compute user-level behavioral, booking, and financial metrics
3. Assign personalized perks via conditional logic

Produce a final user-perk dataset for downstream use

# 📈 Strategic Value
1. High-value segments (e.g., Premium Travelers, Family High Spenders) were identified for loyalty and upselling initiatives.
2. Price-sensitive or new users receive targeted incentives to drive conversions.
3. Lifestyle-based perks for families and seniors improve personalization and relevance.

# Recommendations:
1. Deploy perks in-app and via email immediately for better impact.
2. Monitor perk redemption rate and adjust thresholds quarterly.
3. Track performance via CTR and conversions.
4. Run A/B tests to validate impact.

# References:
[Tableau Reports](https://public.tableau.com/app/profile/vishnu.padmini.lanka/viz/Traveltide_17486436137030/FamilyHighSpenders)

[Presentation pdf](https://github.com/vishnupadminilanka/TravelTide_v2/blob/main/documents/Traveltide%20Customer%20Segmentaion%20%26%20Req_compressed.pdf)

[Decision Tree Framework](https://github.com/vishnupadminilanka/TravelTide_v2/blob/main/documents/Traveltide_Decision%20Tree%20with%20perks.drawio.png)

[Presentation](https://www.canva.com/design/DAGo3SRIcCw/EorHKac4nIgWVLNT8Kg9Tg/view?utm_content=DAGo3SRIcCw&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h25ad5bba90)

