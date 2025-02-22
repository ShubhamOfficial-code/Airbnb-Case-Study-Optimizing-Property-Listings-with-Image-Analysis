# Airbnb Case Study: Optimizing Property Listings with Image Analysis

## Overview

Airbnb is an online marketplace that connects people who want to rent out their homes with people looking for accommodations in specific locales. Over the last five years, Airbnb has observed a correlation between the number of property images associated with a listing and the number of bookings it attracts. Additionally, a significant number of listings remain redundant (i.e., they attract no bookings) due to the lack of associated images.

This case study aims to:
1. Determine the **minimum number of images** that should be made mandatory for a listing to ensure bookings.
2. Identify the **optimal number of images** that hosts should post to maximize bookings and ensure success.

---

## Business Problem

### Key Challenges:
1. **Redundant Listings**: Many listings fail to attract bookings due to insufficient or no images.
2. **Resource Wastage**: Hosts and Airbnb invest time and resources in listings that do not convert into bookings.
3. **User Experience**: Guests rely on images to make booking decisions, and poor-quality or insufficient images can deter bookings.

### Objectives:
- Analyze the relationship between the number of property images and booking rates.
- Provide actionable recommendations for hosts to optimize their listings.
- Improve overall booking rates and reduce redundant listings.

---

## Datasets

The analysis is based on three datasets:

### 1. **Listing Dataset**
- Contains a random sample of 500 listings posted by hosts (including Superhosts) over the last five years.
- Variables:
  - `Listing_Id`: Unique ID for the property listing.
  - `Posting_Date`: Date the listing was posted.
  - `Posting_Time`: UTC time the listing was posted.
  - `Location`: Property location.
  - `Images`: Number of property images associated with the listing.
  - `Bookings`: Number of bookings attracted by the listing.
  - `Host_Type`: Type of host (Regular or Superhost).

### 2. **Open Listing Dataset**
- Provides data on open listings (listings available but not booked) for each date between August 1, 2018, and August 31, 2019.
- Variables:
  - `Date`: Date of observation.
  - `Open_Listings_0_2`: Listings with 0–2 images.
  - `Open_Listings_3_5`: Listings with 3–5 images.
  - `Open_Listings_6_10`: Listings with 6–10 images.
  - `Open_Listings_11_15`: Listings with 11–15 images.
  - `Open_Listings_16`: Listings with more than 16 images.

### 3. **Redundant Listing Dataset**
- Provides data on redundant listings (listings with no bookings in the last year) as of August 31, 2019.
- Variables:
  - `Property_Images`: Range of associated images.
  - `Total_Listings`: Total active listings in the range.
  - `Redundant_Listings`: Listings with no bookings in the last year.

---

## Solution Approach

### Step 1: Exploratory Data Analysis (EDA)
- Analyze the relationship between the number of images and booking rates.
- Identify trends in open and redundant listings.

### Step 2: Insights from Open Listings
- Listings with **11–15 images** had the lowest number of open listings.
- Listings with **6–10 images** had the second-lowest number of open listings.
- Listings with **0–5 images** had the highest number of open listings.

### Step 3: Insights from Redundant Listings
- Listings with **11–15 images** had the lowest percentage of redundant listings.
- Listings with **6–15 images** were preferred by hosts and had the highest number of active listings.

### Step 4: Insights from Listing Dataset
- **Regular Hosts**: Listings with **12–13 images** had the highest median bookings.
- **Superhosts**: Listings with **11 images** had the highest median bookings (balancing practicality and performance).

### Step 5: Monthly Bookings Analysis
- To ensure at least **one booking per month**, hosts should post a **minimum of 6 images**.

---

## Key Findings

1. **Optimal Number of Images**:
   - **Regular Hosts**: 11–15 images.
   - **Superhosts**: 11 images.

2. **Minimum Number of Images**:
   - **All Hosts**: 6 images (to ensure at least one booking per month).

3. **Impact of Property Age**:
   - Listings with **4–5 years of age** and **11–15 images** had the highest bookings for regular hosts.

---

## Conclusion

Based on the analysis, we recommend:
1. **Mandatory Minimum**: Hosts should post at least **6 images** to ensure bookings.
2. **Optimal Range**: Hosts should aim for **11–15 images** to maximize bookings.
3. **Host-Specific Recommendations**:
   - Regular hosts should focus on **12–13 images**.
   - Superhosts should focus on **11 images**.

These recommendations are supported by data-driven insights and aim to improve booking rates while reducing redundant listings.
