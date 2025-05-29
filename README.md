# 🚀 Executive Summary: Travelproject – Personalization and Engagement Strategy (Post Jan 2023)
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
Filter relevant sessions (post-Jan 4, 2023, >7 sessions)
Compute user-level behavioral, booking, and financial metrics
Assign personalized perks via conditional logic

Produce a final user-perk dataset for downstream use

# 📈 Strategic Value
High-value segments (e.g., Premium Travelers, Family High Spenders) were identified for loyalty and upselling initiatives.
Price-sensitive or new users receive targeted incentives to drive conversions.
Lifestyle-based perks for families and seniors improve personalization and relevance.

# Recommendations:
Deploy perks in-app and via email immediately for better impact.
Monitor perk redemption rate and adjust thresholds quarterly.
Track performance via CTR and conversions.
Run A/B tests to validate impact.
