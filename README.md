# Research on Systemic Failures in AI Applications

This repository contains research materials and code for analyzing systemic failures in AI applications using news media as a primary data source. ***The study focuses on extracting mitigation actions and organizing them into a structured taxonomy, building on the existing MIT AI Risk Mitigation Taxonomy.***

---

## Introduction

This research explores systemic failures in AI applications as reported by news media, with the goal of identifying recurring risk patterns and mitigation strategies. By analyzing real-world AI incidents, we aim to better understand how failures emerge across technical, organizational, and societal dimensions.

---

## Data

We use data from three sources — AI Incident Databas (AIID), AIAAIC and AI Incidents Monitor (developed by OECD), with over 9,000 rows in total. Each row represents one AI-related incident. All three datasets follow a similar methodology in which each AI incident reported in the news media is recorded as a distinct entry and linked to its original source.

---

# Mitigation
GPT-5-mini is used to identify mitigation statements, which are then manually reviewed to ensure accuracy. The extracted data is organized into structured records containing:

- Incident ID  
- Mitigation action  
- Assigned mitigation subcategory  

When multiple mitigations appear in a single incident, each action is stored as a separate entry.

---

