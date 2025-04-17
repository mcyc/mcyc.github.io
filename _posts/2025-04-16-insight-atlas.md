---
title: InsightAtlas
author: mcyc
date: 2025-04-16 12:00:00 +0800
categories: [Projects, Python, DataViz, SQL]
tags: [project, geospatial, dashboard, Streamlit, Folium, Python, SQL]
pin: false
comments: false
layout: page
---

**InsightAtlas** – a flexible, mobile-friendly dashboard for exploring and sharing geographic  
insights through data (see [live demo](https://insight-atlas.streamlit.app/)).

- Built to support collaboration with non-partisan NGOs, enabling geographically targeted outreach and engagement strategies.
- Visualizes choropleth maps from custom CSV datasets, supporting both local and cloud-hosted sources.
- Adaptable for community canvassing, education access analysis, public engagement, and planning support.
- Designed with lightweight, shareable tooling (Streamlit + Folium) to support field work and remote collaboration.

### Data Preparation & SQL Workflow

The data powering InsightAtlas was curated through SQL queries involving multiple joined tables, enabling flexible regional comparisons.

- Used `JOIN`, `GROUP BY`, and `CASE WHEN` logic to integrate geospatial identifiers with demographic and engagement metrics.
- Applied filtering logic to tailor datasets for specific outreach goals (e.g., identifying high-impact neighborhoods).
- Ensured consistent formatting and schema compatibility for seamless integration into Streamlit and Folium maps.

This upstream SQL work laid the foundation for meaningful geographic insights surfaced in the [live demo](https://insight-atlas.streamlit.app/).

---
For more, please see:
: <a href="https://github.com/mcyc/InsightAtlas" class="tag text-muted">
    <i class="fab fa-github-square"></i> GitHub
  </a>
