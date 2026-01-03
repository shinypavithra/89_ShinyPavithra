PROBLEM STATEMENT:

Modern marketers rely heavily on historical campaign data such as conversion rates, ROI, clicks, and engagement scores. However, this data is often presented only in dashboards and spreadsheets, leaving marketers to guess how to translate insights into effective marketing copy.

Most existing AI copywriting tools generate generic content without understanding past campaign performance, resulting in inefficient A/B testing, low ROI, and trial-and-error decision making.

There is a clear gap between marketing analytics and actionable content generation.

 PROPOSED SOLUTION:

We propose a Data-Aware Marketing Content Generator that analyzes historical marketing campaign performance data and uses Generative AI to:

Generate 3 personalized marketing copy variants

Provide a clear A/B testing hypothesis

Explain why a particular copy strategy is recommended

Output results in a structured JSON format for easy experimentation

Instead of generating copy blindly, our system conditions the LLM on campaign KPIs, audience segments, channels, and performance trends.

 DATASET USED:

Dataset Used
Marketing Campaign Performance Dataset

This project uses the Marketing Campaign Performance Dataset sourced from Kaggle, which provides detailed insights into the effectiveness of various marketing campaigns.

The dataset contains 200,000 unique campaign records collected over a two-year period, offering a comprehensive view of campaign performance across diverse companies, audience segments, channels, and timeframes.

It captures both performance metrics and contextual campaign attributes, enabling data-driven analysis of marketing effectiveness and making it well-suited for building a data-aware Generative AI system.

🔗 Dataset Link:
https://www.kaggle.com/datasets/manishabhatt22/marketing-campaign-performance-dataset


For the hackathon MVP, the system selectively uses attributes that directly influence marketing copy personalization and strategy reasoning, including:

Campaign_Type

Target_Audience

Customer_Segment

Channels_Used

Conversion_Rate

ROI

Engagement_Score

Clicks & Impressions

Duration

Language

These features are used to condition the LLM on campaign performance trends, audience context, and channel behavior, enabling more relevant and explainable content generation.

Dataset Scope & Relevance:

By leveraging this dataset, the system can:

Analyze campaign effectiveness across channels and segments

Identify high- and low-performing campaign patterns

Translate KPI insights into actionable marketing copy

Support data-driven A/B testing hypotheses

This dataset provides a strong foundation for bridging marketing analytics with Generative AI-powered content creation.

 Future Extensions:

Attributes such as Company, Location, and Date are not directly used in the MVP but enable future enhancements such as:

Brand-specific tone adaptation

Geo-localized campaign messaging

Time-series and seasonal performance analysis

Key Design Principles

Explainability over black-box generation

Segment-level personalization

Reproducibility and simplicity for hackathon scope

 AI & ML TECHNIQUES USED:
Generative AI

Large Language Models (LLMs)

Prompt Engineering

Context Engineering

Structured JSON output control

Machine Learning Concepts

Feature engineering (CTR, ROI, engagement buckets)

Performance trend interpretation

Rule-based reasoning over KPIs

Agentic Pattern (Conceptual)

KPI Analyzer Agent

Copy Generation Agent

GUARDRAILS & EVALUATION:
Guardrails Implemented

Enforced JSON schema output

KPI value validation

Copy length constraints

Non-offensive language filtering

Evaluation Strategy

Since this is a generative task, evaluation is qualitative and rule-based:

Copy diversity across variants

Alignment between KPI condition and copy strategy

Clarity and relevance of A/B hypothesis

Human readability and tone appropriateness

TECH STACK:

Language: Python

Libraries: Pandas, LangChain

LLM: OpenAI / Gemini / Local LLM (user-provided key)

Optional: FastAPI for API-based execution

Environment: Jupyter Notebook / Python script

HOW TO RUN:

python app.py


ASSUMPTIONS & LIMTATIONS:

Segment-level personalization (not individual users)

Static historical dataset

No live campaign feedback loop

Hypotheses are heuristic, not statistically validated

IMPACT & EXPANDABILITY:
Immediate Impact

Helps marketers convert KPIs into actionable copy

Reduces guesswork in A/B testing

Suitable for startups and SMBs

FUTURE SCOPE:

Real-time campaign feedback learning

Multi-language generation

Channel-specific optimization

Integration with ad platforms

Vector similarity search using embeddings (RAG)

 Conclusion:

This project demonstrates how Generative AI can bridge the gap between analytics and action. By making LLMs aware of campaign performance data, we move from generic content generation to explainable, data-driven marketing decisions.
