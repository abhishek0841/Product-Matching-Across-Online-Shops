# 🛒 Product Matching Across Online Shops  
**Machine Learning · Record Linkage · Active Learning · SHAP Explainability**

This project builds an end-to-end **ML-based product matching system** to link consumer electronic items across two online shops.  
The system uses **similarity features**, **CatBoost classification**, **active learning**, and **SHAP analysis** to understand the factors driving product matches.

---

## 🚀 Features

- 🔗 **Record Linkage Pipeline:** Blocking + similarity scoring across product names, codes, prices, and manufacturers  
- 🧠 **ML Classifier:** CatBoost model trained on engineered similarity features  
- 🔁 **Active Learning Loop:** Iteratively improves labels → better precision/recall  
- 📊 **Explainability:** SHAP dependency + feature importance to interpret model behavior  
- 🛠 **Data Preprocessing:**  
  - Regex-based product code extraction  
  - Manufacturer normalization  
  - Name + text cleaning  
  - Price standardization  

---

## 📂 Project Structure
├── data/
│ ├── abt.csv
│ ├── buy.csv
│ └── xref.csv
├── notebook/
│ └── solution.ipynb
├── images/
│ └── shap_dependency_plot.png ← (add your image here)
├── requirements.txt
└── README.md

---

## 📈 SHAP Analysis (Feature Explainability)

Below is an example SHAP dependency plot showing the **non-linear U-shaped effect** of `code_score` and interaction with `manufacturer_score`:

![SHAP Plot](<img width="648" height="459" alt="output3" src="https://github.com/user-attachments/assets/dc352d83-9a83-4092-916e-43dad32b475b" />
)

*(Add your image to `images/` and ensure the filename matches.)*

---

## 🛠 Installation

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
pip install -r requirements.txt
jupyter notebook notebook/solution.ipynb

🧪 How It Works (High-Level)

Load product catalogs (abt, buy) and ground-truth mapping (xref)

Clean and standardize text fields

Extract product codes using regex

Generate similarity features (names, codes, manufacturers, prices)

Block candidate pairs to reduce pair explosion

Train CatBoost classifier

Iteratively refine labels with active learning

Explain model behavior using SHAP

📜 Key Techniques Used

String Similarity (Levenshtein, RapidFuzz)

Blocking for candidate reduction

CatBoost Classification

Active Learning

SHAP Explainability

Feature Engineering & Preprocessing

🏆 Outcome

This system provides a transparent and scalable solution for matching high-variance product listings across e-commerce catalogs—critical for:

Price comparison engines

Duplicate catalog cleanup

Marketplace product consolidation

Retail intelligence & competitor monitoring

🤝 Contributing

Pull requests are welcome!
For major changes, please open an issue first to discuss what you’d like to modify.

📄 License

MIT License
