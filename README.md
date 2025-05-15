# 🧠 AutoML-Driven AChE Inhibitor Screening

This project accelerates the discovery of Acetylcholinesterase (AChE) inhibitors—crucial for Alzheimer’s treatment—using machine learning. We built a complete end-to-end pipeline to predict compound bioactivity (pIC₅₀) based on molecular descriptors and deployed it through an interactive Streamlit app.

## 📌 Problem Statement

Discovering effective AChE inhibitors is time-consuming and expensive. Our solution applies AutoML techniques to predict which molecules are likely to be bioactive, helping researchers and startups prioritize compounds more efficiently.

## 👥 Team

* Vivek Chatla
* Jahnavi Pragada
* Dheeraj Arumulla

## 🔬 Dataset

* Source: [ChEMBL Database](https://www.ebi.ac.uk/chembl/)
* Total Molecules: 4,695
* Data Includes:

  * `molecule_chembl_id`
  * `canonical_smiles`
  * `standard_value` (IC₅₀)
  * Transformed `pIC₅₀` values
  * \~1400+ descriptors generated using PaDEL

## 🧪 Pipeline

```
1. Bioactivity Data Retrieval (ChEMBL)
2. Data Cleaning (Remove nulls, standardize IC₅₀)
3. Descriptor Computation (PaDEL)
4. Exploratory Data Analysis (MW, LogP, H-bond trends)
5. Model Training (Decision Tree, Random Forest, etc.)
6. Model Interpretation (SHAP)
7. Deployment via Streamlit Web App
```

## 📈 Sample Results

| pIC50 | prediction\_label |
| ----- | ----------------- |
| 5.27  | 5.70              |
| 6.42  | 6.51              |
| 3.60  | 4.96              |
| 5.66  | 6.31              |
| 4.00  | 4.31              |

## 📊 SHAP Explainability

Used SHAP (SHapley Additive exPlanations) to interpret predictions. Key features influencing activity include:

* Aromatic rings
* Hydroxyl groups
* Primary amines

## 💻 Streamlit Web App

* Upload `.mol2` files or descriptor `.csv`
* Visualize molecules interactively using py3Dmol
* Predict pIC₅₀
* View SHAP plots for interpretation
* Download results

## 🚀 Future Work

* Enable batch upload and batch prediction
* Add docking score integration
* Expand training data with external sources
* Improve UI/UX of the web interface

## 📎 How to Run

1. Clone the repo
2. Install requirements:

   ```bash
   pip install -r requirements.txt
   ```
3. Launch the app:

   ```bash
   streamlit run app.py
   ```

## 📄 License

This project is for educational and non-commercial use.

---

🧬 Bridging chemistry and machine learning for real-world drug discovery.
