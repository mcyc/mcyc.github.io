---
title: Voter Behaviour - Clustering
author: mcyc
date: 2025-05-19 12:00:00 +0800
categories: [Projects, Python, DataViz, SQL, Voter Behaviour, Clustering]
tags: [project]
pin: false
comments: false
layout: page
---

Clustering can be a powerful tool for grouping individuals based on their political perceptions—and by extension, 
their likelihood to shift how they vote.  
Using **HDBSCAN** clustering on individual Canadians’ ratings of federal political parties, 
I identified voter segments with varying levels of loyalty and potential to be persuaded.
These insights can inform **targeted outreach strategies** by focusing on demographics most responsive to engagement.

<img src="https://res.cloudinary.com/dmx24zdav/image/upload/v1747688676/CAN_Political_Alignments_2021_CornerPlot_q7jjbl.png" alt="Corner plot showing selected clusters" style="max-width: 600px; width: 100%; height: auto;" />

### Main Findings

Younger, left-leaning demographics with higher satisfaction in Canada's democracy are more likely to view
**multiple parties favorably**, suggesting **vote fluidity** and **lower partisanship**.  
These voters are prime candidates for outreach due to their openness to persuasion.

The youngest demographic segments, while potentially persuadable, tend to lack strong political opinions.
Their general indifference toward all parties **suggests a higher barrier to engagement.** A more nuanced and cautious
approach is recommended when targeting these individuals, possibly by focusing on issues that resonate with their values.

<img src="https://res.cloudinary.com/dmx24zdav/image/upload/v1747688696/CAN_Political_Alignments_2021_ViolinPlots_zlnwb9.png" alt="Violin plot of party ratings by cluster" style="max-width: 500px; width: 100%; height: auto;" />

---

### Technical Overview

- **Objective**: Segment voters based on their favorability ratings of Canadian federal political parties to understand behavioral drivers of voter alignment.

- **Data**: 2021 Canadian Election Study ([CES](https://odesi.ca/en/details?id=/odesi/doi__10-5683_SP3_MMXTFC.xml); n=20,968).

- **Challenge**: A voter’s final ballot choice may not fully reflect their political alignment. Given that many Canadians are not strongly partisan, election-day decisions can be influenced by a range of contextual factors.

- **Approach**: Party ratings provide a more nuanced proxy for political preference. Given Canada’s multi-party system, unsupervised clustering is well-suited to uncover hidden voter segments.

- **Method**: I applied **HDBSCAN** to individual-level ratings for:
  - Conservatives (CON)
  - Liberals (LIB)
  - New Democratic Party (NDP)
  - Green (GRN)
  - Bloc Québécois (BLQ)
  - People's Party of Canada (PPC)

  HDBSCAN was chosen for:
  - Automatically determining the number of clusters
  - Distinguishing “noise” (unclustered individuals) from valid groups
  - Requiring minimal hyperparameter tuning
  - Robustness across varying density scales

---

### Results & Interpretation

The model revealed **9 distinct clusters**, referred to as "groups."
The top plot shows their relative positions based on party favorability ratings.
Some groups exhibit **deep partisanship**, while others appear **politically mobile**—more
likely to switch affiliations across elections.

Each group was named based on its favorability pattern, and grouped under strategic voter categories:

#### **Party-loyalists** – Primarily favor one party

- **CON-only**: Rate only the Conservative Party favorably  
- **LIB-only**: Rate only the Liberal Party favorably  
- **PPC-only**: Rate only the People's Party favorably  
- **PPC-main**: Favor PPC most, but not exclusively  
- **BLQ-main**: Favor Bloc Québécois most, but not exclusively

#### **Non-partisans** – Favor multiple parties

- **N-L-only**: Favor both NDP and Liberals, but no others  
- **G-N-L**: Favor NDP, Greens, and Liberals over remaining parties

#### **Unengaged** – Indifferent or unfavorable to all

- **Indifferent**: Rate all parties similarly and moderately  
- **Dislike-all**: Rate all parties negatively

These groups offer actionable insights for **data-informed political engagement strategies**—especially in identifying persuadable segments and crafting tailored outreach efforts.


