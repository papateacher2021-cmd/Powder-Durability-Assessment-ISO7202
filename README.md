**EMSA - Ship Safety and Security Unit**

# Technical Study: Integrating ISO 7202:2018 Standards with Machine Learning for Dry Chemical Powder Compliance

**Author: Francisco Broissin - EMSA Senior Officer for Marine Equipment**

**Topic: Predictive Quality Control in Fire Suppression Agents**

**Date: 26 March 2026**

## Abstract

This work explores the digital transformation of laboratory compliance testing for fire extinguishing powders under the ISO 7202:2018 standard. By leveraging synthetic datasets based on empirical physical limits—specifically needle penetration, moisture content, and granulometry—we developed a Random Forest Classification model. The study demonstrates how AI can transition from binary Pass/Fail logic to a nuanced "Marginal Pass" warning system, allowing for proactive manufacturing adjustments and enhanced quality assurance in fire safety engineering.

**Licence**. With a view to transparency and free use, the author has licenced the resulting artificial intelligence model under the terms of the MIT Licence.

## Introduction and Methodology

The research focuses on the durability requirements of dry chemical agents (e.g., MAP, sodium Bicarbonate, and Potassium Bicarbonate). The methodology follows a four-stage engineering pipeline:

a) **Data Synthesis**: Generating 2,000+ samples using NumPy to simulate real-world laboratory variances. Physical correlations were hard-coded to reflect that high fine-particle counts (< 40 micro meter) increase moisture absorption and decrease penetration depth (caking).

b) **Feature Engineering**: Three primary features were utilized:
   - Penetration Depth (mm): The primary indicator of powder fluidity.
   - Moisture Content (%): The leading cause of chemical instability.
   - Fines Percentage (%): The granulometric driver of surface area reactivity.

c) **Artificial Intelligence - Model Selection**: A Random Forest Classifier was chosen due to its ability to handle non-linear decision boundaries and provide high interpretability through feature importance rankings.

d) **Classification Logic**: The model was trained to identify three distinct states:
   - Class 0 (Fail): Direct violation of ISO 7202:2018.
   - Class 1 (Marginal): Compliant, but within a 10% "Warning Zone" buffer.
   - Class 2 (Clear Pass): High-stability batches.

## Key Findings and Visualization

Through the use of Seaborn and Matplotlib, the work visualized the "Tipping Point" of powder failure. The Correlation Matrix confirmed a strong negative correlation between fine particles and penetration depth, proving that granulometry is a leading indicator of eventual caking.

The Feature Importance Report identified Penetration Depth as the most significant mathematical "weight" in the decision-making process, followed closely by Moisture Content. This provides engineers with a "Priority Map" for troubleshooting factory production lines.

## Conclusion

The integration of Machine Learning with ISO 7202:2018 standards moves quality control from reactive (testing after failure) to predictive (identifying marginal risks). By prompting the model with "unseen" lab data, engineers can obtain instant compliance verdicts with a calculated confidence percentage. This approach reduces human error in data interpretation and ensures that fire suppression systems are equipped with only the most stable chemical agents.
