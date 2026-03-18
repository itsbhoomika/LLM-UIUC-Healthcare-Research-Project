Overview

Clinical trial datasets contain large volumes of unstructured text describing study design, interventions, eligibility criteria, and outcomes. Many critical factors influencing trial success are embedded in these narratives and are not directly usable in traditional predictive models.

In this project, we developed an LLM-augmented supervised learning pipeline that extracts structured attributes from clinical trial descriptions and converts them into predictive features.

Data

We used publicly available cancer clinical trial data from ClinicalTrials.gov.

1. 115,480 trials
2. 33 structured + unstructured columns

Approach

We built an end-to-end pipeline that converts trial descriptions into structured predictors using an iterative LLM–model feedback loop.
<img width="1536" height="1024" alt="image_llm" src="https://github.com/user-attachments/assets/1137698e-c588-451e-a1c3-c672558651de" />

🔁 Pipeline Overview

Iteration
Repeat the process to improve feature quality and predictive signal.

Key Insight

LLM-extracted structured features capture high-value predictive signals from narrative text and can be effectively integrated with traditional machine learning models.

Conclusion

This project demonstrates an end-to-end pipeline for transforming unstructured clinical trial descriptions into structured features using a large language model. The extracted features can be integrated with traditional machine learning models to support predictive analysis.

The workflow highlights:

The ability of LLMs to extract meaningful structured signals from text

The effectiveness of combining LLM outputs with interpretable models

The value of a model-driven feedback loop for iterative feature refinement

👉 More broadly, this approach can be applied to text-heavy datasets in domains such as fraud detection, risk modeling, and compliance analytics, where critical signals are embedded in unstructured data.
