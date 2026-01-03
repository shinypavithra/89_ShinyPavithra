PROBLEM STATEMENT:

Modern marketers rely heavily on historical campaign data such as conversion rates, ROI, clicks, and engagement scores. However, this data is often presented only in dashboards and spreadsheets, leaving marketers to guess how to translate insights into effective marketing copy.

Most existing AI copywriting tools generate generic content without understanding past campaign performance, resulting in inefficient A/B testing, low ROI, and trial-and-error decision making.

There is a clear gap between marketing analytics and actionable content generation.

 PROPOSED SOLUTION:
We built a Data-Aware Marketing Content Generator that:

Analyzes historical marketing campaign performance data.

Generates 3 personalized marketing copy variants per customer segment.

Provides a clear A/B testing hypothesis based on data.

Outputs results in a structured JSON format for easy experimentation.

Instead of generating copy blindly, our system conditions the content generation on campaign KPIs, audience segments, channels, and performance trends.

⚠️ Note: In this hackathon MVP, we used rule-based, deterministic logic for insights. LLM integration is designed to be plug-and-play but was not executed live due to API constraints.


 DATASET USED:

 Marketing Campaign Performance Dataset from Kaggle
🔗 Dataset Link

200,000 campaign records spanning two years.

Covers diverse companies, audience segments, channels, and timeframes.

Key attributes used in MVP:

Campaign_Type, Customer_Segment, Target_Audience

Channels_Used, Conversion_Rate, ROI, Engagement_Score

Clicks & Impressions, Duration, Language

The system analyzes KPIs per segment to produce actionable marketing copy and a simple A/B hypothesis.


SYSTEM ARCHITECTURE & DESGIN:


![WhatsApp Image 2026-01-04 at 12 25 49 AM](https://github.com/user-attachments/assets/c03bf314-9a2b-4111-a8cc-75df40b68d5f)

TECHNIQUES USED:

Rule-based KPI analysis

Feature computation: conversion rate, ROI, engagement score

Copy generation logic based on segment-level insights

Structured JSON output for consistency

⚠️ Note: LLM integration is optional/future — currently, content is generated using rule-based logic.

GUARDRAILS & EVALUATION:

Enforced JSON schema for output.

KPIs validated against historical segment data.

Copy strategies aligned with computed insights.

Output is reproducible and deterministic.

Evaluation is qualitative, focusing on:

Copy diversity across variants

Alignment between KPIs and strategy

Clarity of A/B hypothesis

Professional tone

TECH STACK:

Python

Pandas

JSON

(Optional for future) LLMs: Gemini / Gemma / Local LLM

HOW TO RUN:

Upload the Kaggle dataset (archive.zip) and extract CSV.

Select a customer segment.

Run the script to generate JSON output:

python app.py


ASSUMPTIONS & LIMITATIONS:

Segment-level personalization only (not individual users).

Static historical dataset — no live campaign feedback.

A/B testing hypothesis is heuristic, not statistically validated.

LLM integration is not live in MVP.

IMMEDIATE IMPACT:

Helps marketers translate KPIs into actionable marketing copy.

Reduces guesswork in A/B testing.

Applicable for startups and SMBs.

FUTURE SCOPE:

Integrate live campaign feedback for automated learning.

LLM integration for richer, more creative copy generation.

Multi-language copy support.

Integration with marketing automation platforms.

Channel-specific optimization using historical trends.

CONCLUSION

This project demonstrates how data-aware logic can bridge marketing analytics and action. By making content generation conditioned on KPIs and audience segments, we ensure outputs are actionable, explainable, and immediately useful — even without live LLM calls.
