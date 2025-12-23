# cnpj-data-processing
Process and enrich Brazilian Federal Revenue (CNPJ) public data with filters by UF and CNAE, partner age classification, and municipality mapping.
# 📊 Brazilian Federal Revenue (CNPJ) Data Processing

This project aims to **download, process, filter, and enrich public CNPJ data provided by the Brazilian Federal Revenue Service (Receita Federal)**, generating a **final CSV file** based on user-defined filters such as **State (UF)** and **CNAE**.

In addition to basic filtering, the script also:
- **Cross-references company and partner (shareholder) data**
- **Classifies partners by age range**
- **Identifies and classifies municipalities**, even though this information is not explicitly available in the original Receita Federal datasets

---

## 🚀 Features

- 📥 Reads official Receita Federal public CNPJ datasets
- 🔍 Filters companies by:
  - State (UF)
  - CNAE
- 🔗 Data merging:
  - Companies × Establishments
  - Companies × Partners
- 👥 Partner (shareholder) processing:
  - Age calculation
  - Age range classification
- 🏙️ Municipality classification based on available codes
- 📄 Exports consolidated results to **CSV**
- ⏱️ Progress tracking with `tqdm`

---

## 🗂️ Expected Data Structure

The script expects the Receita Federal files to be organized according to the official distribution structure:

dados_receita/
│
├── empresas/
│ └── *.csv
│
├── estabelecimentos/
│ └── *.csv
│
└── socios/


> ⚠️ The original files are usually provided as `.zip`. Make sure to extract them before running the script.

---

## 🧰 Requirements

- Python **3.8+**
- Python libraries:
  - `pandas`
  - `tqdm`

Install dependencies using:

```bash
pip install pandas tqdm

└── *.csv

▶️ How to Use

Download the public CNPJ datasets from the official Receita Federal website

Extract and organize the files following the structure above

Adjust the script:

Path to the dataset folder

Desired UF and CNAE filters

Run the script or Jupyter Notebook

After processing, a filtered and enriched CSV file will be generated.

👥 Partner Age Range Classification

The script calculates partner age (when available) and classifies it into predefined age ranges, for example:

Up to 18 years

19 to 30 years

31 to 45 years

46 to 60 years

Over 60 years

Classification depends on the availability and consistency of birth date information.

🏙️ Municipality Classification

The Receita Federal datasets do not provide municipality names directly.
This project derives and classifies municipalities by processing and mapping the available municipality codes.

📄 Output

Final CSV file

Consolidated data including:

Company information

Establishment details

Partner data

Partner age range

Municipality

State (UF)

CNAE

⚠️ Important Notes

All data used in this project is publicly available

This project does not perform official or legal company validation

Data usage is the user's responsibility and must comply with LGPD and applicable regulations
