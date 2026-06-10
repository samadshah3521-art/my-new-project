# my-new-project
Building AI Course Project
# PureStream: AI-Powered Local Water Quality Predictor

Final project for the Building AI course

## Summary
PureStream is a machine learning-based tool designed to predict whether local freshwater sources are safe for consumption or agricultural use. By analyzing easily measurable parameters like pH, turbidity, and temperature, the system provides a real-time safety indicator (Safe/Unsafe) for communities lacking immediate access to advanced laboratory testing.

## Background
* **The Problem:** Access to clean drinking water is a critical issue globally. Many rural or developing communities rely on local wells or rivers, but laboratory water testing is expensive and slow.
* **Frequency:** Water contamination spikes unpredictably after heavy rains, industrial runoffs, or seasonal changes.
* **Motivation:** Providing a low-cost, accessible digital alternative to traditional testing can help prevent waterborne diseases before they spread. 
* **Importance:** It empowers local citizens and small-scale farmers to make data-driven decisions about their water safety using affordable, hand-held sensor tools.

## How is it used?
1. **Data Collection:** A user measures basic water metrics using cheap, off-the-shelf digital pens (measuring pH, Total Dissolved Solids, and temperature).
2. **Input:** The user enters these values into the PureStream mobile or web interface.
3. **Prediction:** The AI model processes the inputs and instantly displays a safety assessment alongside a confidence score.

### Example Scenario
> A community health worker in a rural village tests a local well after a major storm. They plug the values into the app, which flags the water as "High Risk - Suspected Bacterial/Runoff Contamination," prompting the village to boil the water before use.

## Data sources and AI methods
* **Data Sources:** The model can be initially trained on open-source water quality datasets, such as the [Water Quality Dataset on Kaggle](https://www.kaggle.com/datasets/adityakadiwal/water-potability).
* **AI Techniques:** * **Binary Classification:** Since the output is a simple "Safe" or "Unsafe", algorithms like **Logistic Regression**, **Random Forests**, or **Support Vector Machines (SVM)** are ideal for this tabular sensor data.

| Sensor Input | Ideal Range | AI Impact |
| :--- | :--- | :--- |
| **pH Level** | 6.5 - 8.5 | Detects chemical/acidic changes |
| **Turbidity** | < 5.0 NTU | Measures cloudiness/particles |
| **TDS (Dissolved Solids)** | < 500 ppm | Flags heavy mineral concentration |

## Challenges
* **Limitations:** This AI project *cannot* detect specific pathogens, heavy metals (like arsenic or lead), or microplastics without specialized chemical sensors. 
* **Ethical Considerations:** False negatives (marking contaminated water as "Safe") could lead to severe health risks. The tool must always clearly state that it is a *screening tool*, not a definitive biological test.

## What next?
* **Hardware Integration:** The project could scale by building a physical IoT device equipped with cheap sensors that automatically uploads data to the cloud.
* **Crowdsourcing:** Creating a public map where users pin their water quality scores to track contamination trends across entire regions.
* **Assistance Needed:** Collaboration with environmental scientists to fine-tune predictive weights and software developers to build a robust offline mobile app.

## Acknowledgments
* Inspired by the global open-data initiatives for clean water.
* Dataset structures adapted from public WHO (World Health Organization) water safety guidelines.
