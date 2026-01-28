# Research on Systemic Failures in AI Applications

This repository contains research materials and code for analyzing systemic failures in AI applications using news media as a primary data source. **The study focuses on extracting mitigation actions and organizing them into a structured taxonomy, building on the existing [MIT AI Risk Mitigation Taxonomy](https://airisk.mit.edu/blog/mapping-ai-risk-mitigations).**

<img width="1988" height="440" alt="image" src="https://github.com/user-attachments/assets/57b58cdb-7e53-43e2-9135-38648748d985" />

---

## Introduction

This research explores systemic failures in AI applications as reported by news media, with the goal of identifying recurring risk patterns and mitigation strategies. By analyzing real-world AI incidents, we aim to better understand how failures emerge across technical, organizational, and societal dimensions.

---

## Datasets

We use data from three sources — [AI Incident Database (AIID)](https://incidentdatabase.ai/), [AIAAIC](https://docs.google.com/spreadsheets/d/1Bn55B4xz21-_Rgdr8BBb2lt0n_4rzLGxFADMlVW0PYI/edit?gid=888071280#gid=888071280) and [AI Incidents Monitor](https://oecd.ai/en/incidents) (developed by OECD), with over 9,000 rows in total. Each row represents one AI-related incident. All three datasets follow a similar methodology in which each AI incident reported in the news media is recorded as a distinct entry and linked to its original source.

---

## Mitigation Extraction
In this phase, each incident text is transformed into an individual task and submitted to the OpenAI Batch API, where GPT-5-mini extracts the corresponding mitigation actions. The resulting JSONL file contains standardized mitigation statements that will be used for taxonomy development and classification.

---

## Taxonomy
In this phase, AI incident mitigation statements are submitted to the OpenAI Batch API using GPT-5-mini to generate a hierarchical taxonomy of mitigation actions. After obtaining the derived taxonomies from the model, we manually reviewed each category and subcategory against MIT's taxonomy, stored unmatched subcategories separately, clustered them to define new categories where appropriate, and identified completely four new categories and two new subcategories within existing categories. With this, we have 32 subcategories in total.

_The newly added subcategories and categories are in blue._
<img width="1005" height="348" alt="image" src="https://github.com/user-attachments/assets/1dd80dd6-1d1a-4171-bd8e-47cdb4dbe461" />


---

## Classification
In this phase, we classify AI incident mitigation actions using GPT-5-mini, assigning each up to five of 32 predefined subcategories. At first, we manually reviewed 300 randomly selected classified texts to assess accuracy, iteratively testing and refining multiple prompt formulations with outputs checked at each step, and in each iteration, a random 5% sample of the final dataset was examined, defining accuracy based on our mutual agreement on label assignment.

---

## Results
Results
A total of 6,893 rows containing mitigation texts were labeled, resulting in 23,994 assigned labels. Of these, 9,629 correspond to newly identified subcategories, while 14,365 match existing subcategories. This shows that although 14,365 mitigation actions align with known categories, approximately **67%** more labels reflect previously unseen mitigation patterns, highlighting the emergence of new categories of mitigation in AI incidents.
