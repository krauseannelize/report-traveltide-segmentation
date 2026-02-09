# TravelTide Segmentation

Customer segmentation analysis of TravelTide travel booking data to design a personalized rewards program, using Python (Pandas, Matplotlib, Seaborn) and SQL.

## Tools & Skills Used

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=flat&logo=matplotlib&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=flat&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![uv](https://img.shields.io/badge/uv-DE5FE9?style=flat&logo=uv&logoColor=white)

## Quick Access

- [Notebook 01 - Sessions EDA](notebooks/01-sessions-eda.ipynb)
- [Notebook 02 - Users Aggregation](notebooks/02-users-aggregation.ipynb)
- [Notebook 03 - Customer Segmentation](notebooks/03-customer-segmentation.ipynb)
- [Database Metadata](data/traveltide-db-metadata.md)
- [Database Schema](data/traveltide-db-schema.png)
- [Executive Summary (PDF)](report/traveltide-report.pdf)
- [Presentation (PDF)](report/traveltide-presentation.pdf)
- [Presentation (Video)](report/presentation-video.mp4)

## Setup & Installation

### Prerequisites

- Python 3.12+
- [uv](https://docs.astral.sh/uv/getting-started/installation/) package manager

### 1. Clone the Repository

```bash
git clone https://github.com/krauseannelize/report-traveltide-segmentation.git
cd report-traveltide-segmentation
```

### 2. Install Dependencies

```bash
uv sync
```

### 3. Run the Project

```bash
uv run jupyter lab
```

> **Note:** `uv run` automatically uses the project's virtual environment—no manual activation needed.

## Project Overview

This project, completed as part of the Masterschool Data Science program, uses the **TravelTide** case study database simulating the operations of an online travel startup. The dataset contains customer, session, flight, and hotel booking information, enabling analysis of travel behavior, discount sensitivity, and booking patterns.  

In this project, I act as a Data Analyst supporting the **Head of Marketing** in her mission to design and execute a personalized rewards program that keeps customers returning to the TravelTide platform. My role is to provide customer insights that guide the personalization of rewards, ensuring they align with traveler preferences and behaviors.

## Objectives

My mission is to support the Head of Marketing in designing a personalized rewards program that drives customer engagement on the TravelTide platform. Specifically, I aim to:

1. **Validate the hypothesis**: Test whether the data supports the existence of distinct customer groups who would be especially interested in the proposed perks.  
2. **Segment the customer base**: Create meaningful groups that reveal differences in demographics, booking behavior, and travel patterns.  
3. **Personalize recommendations**: For each customer, identify and assign a likely favorite perk.  

The business value of segmentation lies in enabling TravelTide to implement targeted strategies, including customized promotions, personalized communications, and differentiated account policies.

## Methodology

This project follows a four‑stage approach. Each stage builds toward the goal of supporting the Head of Marketing in designing a personalized rewards program.

### 1. Exploratory Data Analysis (EDA)

- Clean and filter the data, excluding unsuitable customers.  
- Join tables and prepare a session‑level dataset.  
- Aggregate to the user level and enrich with demographic attributes.  

**Outcome:** A cleaned dataset at both session and user granularity.

### 2. Feature Engineering

- Devise new metrics that capture meaningful customer characteristics.  
- Aggregate session‑level behaviors into user‑level features.  
- Focus on attributes relevant to segmentation (e.g., booking frequency, discount sensitivity, trip length).  

**Outcome:** A feature‑rich dataset ready for clustering.

### 3. Customer Segmentation

- Apply clustering methods to group customers into distinct segments.  
- Interpret the clusters by analyzing demographics and behaviors.  
- Link each segment to a likely preferred perk.  

**Outcome:** Actionable customer segments with clear business relevance and perk associations.

### 4. Presentation & Recommendations

- Summarize findings in an executive‑level report and presentation.  
- Use visualizations (bar plots, scatter plots, radar plots) to illustrate insights.  
- Provide personas or examples to bring clusters to life.  
- Recommend strategies for implementing and measuring the success of the rewards program.  

**Outcome:** A compelling narrative with clear recommendations and defined success metrics.

## Key Findings

- **Seven distinct customer segments identified** based on booking status, family status, and trip duration: Lookers, Sprinters, Voyagers, Trailblazers, Weekenders, Go-Getters, and Adventurers
- **Largest segments:** Sprinters (1,767), Go-Getters (1,762), and Trailblazers (1,557) represent the core customer base
- **Behavioral differences drive segmentation:** Booking frequency, trip volume, and spending patterns vary significantly, while browsing activity and discount uptake remain consistent across groups
- **Tailored rewards mapped to each segment:**
  - Lookers → Exclusive discounts (conversion focus)
  - Sprinters → Free hotel meal (family convenience)
  - Voyagers → One night free hotel with flight (extended family value)
  - Trailblazers → Lounge access (business comfort)
  - Weekenders → Free checked bag (budget leisure)
  - Go-Getters → Weekday stay discounts (price-sensitive)
  - Adventurers → Premium upgrades (experiential rewards)
