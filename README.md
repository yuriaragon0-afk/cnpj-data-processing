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

