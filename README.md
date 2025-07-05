## 🗂️ Notes

⚠️ The original QuickSight dashboard was publicly published and fully functional, but is no longer accessible due to the deletion of the associated QuickSight account and S3 bucket. All insights and visuals are preserved via screenshots and documentation in this repository.


# Netflix Data Dashboard with Amazon QuickSight

This project analyzes the Netflix Movies and TV Shows dataset using Amazon QuickSight to build a fully interactive dashboard. The visualizations uncover patterns in content type, release trends, genre distributions, and top contributing countries.

## Overview

- **Time Period**: Titles released from 1925–2021  
- **Content Types**: Movies and TV Shows  
- **Coverage**: Global dataset including top content-producing countries  
- **Objective**: Gain strategic insights into Netflix’s content trends using AWS QuickSight  

## Tools Used

- **Amazon QuickSight**
- **Amazon S3** (for data storage)
- **QuickSight SPICE Engine**
- Dataset: [Netflix Movies and TV Shows (Kaggle)](https://www.kaggle.com/datasets/shivamb/netflix-shows)

## Dashboard Features

| Insight | Description |
|--------|-------------|
| Content by Year | Tracks how Netflix releases evolved over time |
| Genre Breakdown | Shows the most common listed genres |
| Type Distribution | Compares the volume of Movies vs TV Shows |

## Sample Visuals

![Dashboard Overview](Netflix%20Dashboard.png)


# How to Recreate the Netflix QuickSight Dashboard

This guide walks you through the steps to replicate the Netflix data analysis dashboard on your own AWS account.

---

## ✅ Prerequisites

- ✅ AWS Account
- ✅ Amazon QuickSight enabled (Standard or Enterprise edition)
- ✅ S3 Bucket created (you can name it: `netflix-dashboard-bucket`)

---

## Step 1: Upload Dataset to S3

1. Download `netflix_titles.csv` from Kaggle  
   [Dataset Link](https://www.kaggle.com/datasets/shivamb/netflix-shows)

2. Go to AWS Console > S3  
3. Upload `netflix_titles.csv` into your bucket (`netflix-dashboard-bucket`)

---

## Step 2: Prepare QuickSight Dataset

1. Go to Amazon QuickSight  
2. Choose **New Dataset**  
3. Select **S3** as data source  
4. Enter the S3 URL path (or browse to your bucket)  
5. Name your dataset `Netflix_Titles`

6. Let QuickSight load and preview data  
7. Use **Edit/Transform** to:
   - Change `date_added` to Date type  
   - Extract year from `release_year` if needed  
   - Split multiple genres from `listed_in` column (optional)

---

## Step 3: Build Your Dashboard

Create visuals like:
- Bar chart: `release_year` vs `count`
- Pie chart: `type` (Movie vs TV Show)
- Tree map: `country` vs `count`
- Word cloud: `listed_in` (genres)
- Line graph: content over years

Add filters for:
- Type
- Country
- Genre

---

## Step 4: Add Your Dashboard to GitHub

- Take screenshots of 2–3 key visuals (save into `assets/`)
- If available, export the analysis or manifest JSON from QuickSight
- Upload all to your GitHub project directory

---







