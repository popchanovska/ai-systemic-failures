# Research on Systemic Failures in AI Applications

This repository contains research materials and code for analyzing systemic failures in AI applications using news media as a primary data source. ***The study focuses on extracting mitigation actions and organizing them into a structured taxonomy, building on the existing MIT AI Risk Mitigation Taxonomy.***

---

## Introduction

This research explores systemic failures in AI applications as reported by news media, with the goal of identifying recurring risk patterns and mitigation strategies. By analyzing real-world AI incidents, we aim to better understand how failures emerge across technical, organizational, and societal dimensions.

---

## Data and Methodology

The dataset is derived from news articles reporting AI-related incidents. Each article is processed to extract incident descriptions, mitigation actions, and associated risk categories.

GPT-5-mini is used to identify mitigation statements, which are then manually reviewed to ensure consistency and accuracy. The extracted data is organized into structured records containing:

- Incident ID  
- Mitigation action  
- Assigned mitigation subcategory  

When multiple mitigations appear in a single incident, each action is stored as a separate entry.

---
