
# 🫀 Heart Disease Risk Assistant

A powerful AI-powered web application that predicts heart disease risk from **natural language patient descriptions**.  
It leverages machine learning and LLMs (via Groq) to extract features, assess risk, provide personalized advice, and generate downloadable DOCX/Excel reports.

---

##  Demo

![GIF](https://github.com/user-attachments/assets/4e1f365f-f29f-4a10-ba65-8d91cab072b2)


---

## Block Diagram

 ![User input patient details](https://github.com/user-attachments/assets/e18fdd2c-d3ce-4adc-9b68-728eb9b32d7b)

> The following steps explain the system flow:

1. **Natural Language Input**  
   User enters a plain English description of the patient's symptoms (e.g., age, chest pain, BP).

2. **LLM Feature Extraction**  
   Groq-hosted LLaMA3 model parses and extracts structured features (age, sex, cp, etc.) from the input.

3. **Heart Disease Prediction**  
   The structured features are scaled and passed to a trained Random Forest model to compute the risk percentage.

4. **LLM Explanation**  
   The LLM generates a formal explanation of the risk score in medical terms.

5. **Lifestyle Advice**  
   Static heart-health tips are provided (diet, sleep, exercise, etc.).

6. **Reference Links**  
   DuckDuckGo search fetches up to 3 links from trusted sources (e.g., Mayo Clinic, Wikipedia).

7. **Report Generation**  
   Generates a downloadable **DOCX** or **Excel** file with all results.

8. **Gradio Web Interface**  
   A user-friendly UI wraps all functionality in one place.

---

##  Features

- ✅ Accepts natural language input (no forms!)
- ✅ Uses Groq + LangChain LLM for structured feature extraction
- ✅ Predicts heart disease risk using trained ML model
- ✅ Provides formal LLM-based risk explanation
- ✅ Returns lifestyle health advice
- ✅ Fetches reference links from trusted medical sites
- ✅ Generates downloadable reports in DOCX or Excel
- ✅ Clean, modern Gradio-based UI

---

##  Tech Stack

- Python 3.10+
- [Gradio](https://www.gradio.app/) — Web UI  
- [Scikit-learn](https://scikit-learn.org/) — ML model  
- [LangChain](https://www.langchain.com/) + [Groq](https://groq.com/) — LLM processing  
- [DuckDuckGo Search](https://pypi.org/project/duckduckgo-search/) — external medical links  
- [python-docx](https://pypi.org/project/python-docx/), [openpyxl](https://pypi.org/project/openpyxl/) — report generation  
- [joblib](https://joblib.readthedocs.io/) — model persistence  

---

##  Getting Started

### 1.  Install Requirements

```bash
pip install -r requirements.txt
```

> If `requirements.txt` is missing, create it manually with:

```
gradio
pandas
scikit-learn
joblib
requests
python-docx
openpyxl
duckduckgo-search
langchain
langchain-core
langchain-community
langchain-groq
```

---

### 2.  Add Dataset

- Download the heart disease dataset from [Kaggle](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset)
- Save it as:  
  ```
  heart.csv
  ```
- Place it in the **root directory** of your project.

---

### 3.  Set Groq API Key

Replace the placeholder in your code with your Groq API key:

```python
groq_api = "YOUR_GROQ_API_KEY"
```

>  Get your free API key here: [https://console.groq.com](https://console.groq.com)

---

### 4.  Run the App

To launch the app locally:

```bash
python app.py
```

Or in Jupyter Notebook / Google Colab:

```python
demo.launch()
```

---

##  Example Input

Paste this into the Gradio app input box:

```
A 60-year-old male with chest pain type 3, BP 150, cholesterol 270, fasting sugar 1, ECG 0, heart rate 140, no angina, oldpeak 1.8, slope 1, ca 0, thal 2
```

---

##  Output Includes

-  Risk prediction score (e.g., **78.45%**)
-  Formal medical explanation from LLM
-  Heart-healthy lifestyle recommendations
-  Reference links (Wikipedia, Mayo Clinic, etc.)
-  Downloadable report (in DOCX or Excel format)

---

##  Screenshots

INPUT IMAGE

<img width="1890" height="784" alt="S1" src="https://github.com/user-attachments/assets/ab36bdae-8086-4905-b06e-fe4caf8ba960" />
OUTPUT IMAGE

<img width="1881" height="787" alt="S2" src="https://github.com/user-attachments/assets/9a90b5b1-f613-4166-9479-b4bdd2a4b3af" />
DOCUMENT IMAGE

<img width="954" height="973" alt="S3" src="https://github.com/user-attachments/assets/ec759644-2293-4f27-9367-6b2a3293e52c" />
<img width="869" height="888" alt="S4" src="https://github.com/user-attachments/assets/bf3bd716-83e2-4c9f-b5ee-0087461ddead" />




                 




## 📜 License

This project is licensed under the **MIT License**.  
You're free to use, modify, and distribute with credit.

---

## 🙋‍♂️ Author

**Sumukha**  
For questions, suggestions, or collaboration — feel free to open an issue or pull request on GitHub.
