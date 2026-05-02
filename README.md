# ClimateAI
This project investigates how CO₂ prediction models behave under realistic data issues; and whether we can detect unsafe outputs before they cause harm.
Motivation
AI models are increasingly used in climate and policy decision-making. But what happens when these systems are confidently wrong?

Research Questions:
Can AI models produce high-confidence but incorrect predictions?
Do explanations make these errors more or less trustworthy?
Can simple signals help us detect and control unsafe predictions?

Dataset
We use the Our World in Data CO2 and Greenhouse Gas Emissions Dataset, a widely used source in climate research and policy.

Methodology
1. Baseline Model:
Random Forest Regression predicting CO₂ emissions

2. Failure Simulation:
We simulate real-world data issues introducing:
Missing data, Noisy inputs, Distribution shift (cross-region / temporal)

3. Misleading Behavior Detection: 
We define misleading predictions as High-confidence predictions with large error

4. Explainability Audit:
We test whether SHAP explanations reveal failure Or reinforce false trust

5. Control System
We implement a simple risk scoring mechanism to flag unsafe predictions based on:
Prediction instability and Input deviation

Key Results
Models can remain highly confident even when wrong
Explanations often appear reasonable despite incorrect predictions
Simple control signals can detect a portion of unsafe outputs

Implications
Climate AI systems may silently fail in deployment
Overconfidence can mislead policymakers
Safety auditing should be standardized before deployment

Future Work
Improve detection systems
Extend to deep learning models

Human-in-the-loop evaluation
