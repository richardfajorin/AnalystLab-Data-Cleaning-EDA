# Data Cleaning & EDA: OnlineRetail & Netflix Datasets

**Author:** Richard Obanijesu Fajorin  
**Program:** AnalystLab Africa, Data Analyst Internship (Week 1–2)  
**Tools:** Python, Pandas, Jupyter Notebook, Matplotlib, Seaborn

---

##  Overview

End-to-end data cleaning and exploratory data analysis (EDA) on two Kaggle datasets:
- **OnlineRetail** — E-commerce transaction log with 541,909 transactions
- **Netflix Titles** — Media catalog with 8,809 titles

This project demonstrates proficiency in missing-value handling, outlier treatment, format standardization, statistical analysis, and data visualization for business insights.

---

##  Repository Contents

| File | Description |
|------|-------------|
| `OnlineRetail_CLEANED.csv` | Cleaned e-commerce dataset (~405K rows) |
| `Netflix_CLEANED.csv` | Cleaned Netflix catalog (8,809 rows) |
| `OnlineRetail_EDA.png` | 4-panel visualization of retail trends |
| `Netflix_EDA.png` | 4-panel visualization of content trends |
| `analysis.ipynb` | Full Jupyter Notebook with documented analysis |
| `README.md` | This file |

---

##  Data Cleaning Process

### OnlineRetail Dataset
- **Missing CustomerID** (135,080 rows): Dropped — required for customer-level analysis
- **Missing Description** (1,454 rows): Dropped — incomplete product information
- **Negative Unit Prices**: Removed as data quality issues (likely refund artifacts)
- **Negative Quantities**: Retained — represent legitimate returns
- **Date Format**: Standardized from MM/DD/YYYY HH:MM to datetime

**Result:** 541,909 rows → ~404,000+ usable rows (25% reduction, quality-focused)

### Netflix Dataset
- **Missing Director** (~29%): Kept — reflects legitimate gaps in older/undocumented titles
- **Missing Cast** (~9%): Kept
- **Missing Date Added** (~10%): Kept
- **Missing Country**: Filled with 'Unknown'
- **Missing Rating**: Filled with 'Not Rated'
- **Mixed Duration Format** ("90 min" vs "2 Seasons"): Parsed into numeric fields

**Result:** 8,809 rows fully processed with no rows deleted

---

##  Key Findings

### OnlineRetail Analysis
✓ **Geographic Concentration:** UK generates 50%+ of total revenue; international markets remain underdeveloped  
✓ **Revenue Concentration:** Top 10 products drive a disproportionate share of revenue (concentration risk)  
✓ **Seasonal Trends:** Consistent month-over-month growth with a Q4 seasonal peak  
✓ **Customer Segments:** Bulk orders (80K+ units/transaction) indicate an identifiable B2B segment  
✓ **Quality Metrics:** Low return rate (~3–5%) suggests solid product quality  
✓ **Customer Value:** Top 10 customers account for ~15% of total revenue

### Netflix Analysis
✓ **Content Mix:** TV Shows (60%) outnumber Movies (40%) — retention-oriented strategy  
✓ **Production Trends:** Content additions peaked in 2021, declining from 2022 onward (likely cost management)  
✓ **Geographic Dominance:** USA leads production (35%); India and South Korea are emerging content hubs  
✓ **Content Maturity:** Mature-rated content dominates (TV-MA/R = 50%+); family content is comparatively scarce (~15%)  
✓ **Genre Leaders:** Dramas, International TV, and Documentaries are the top genres  
✓ **Global Strategy:** Clear global sourcing strategy with localized content per major market

---

##  Actionable Recommendations

### For OnlineRetail
1. **Expand High-Potential Markets:** Launch targeted campaigns in Netherlands, Sweden, and Germany — proven demand, high potential for growth
2. **B2B Revenue Opportunity:** Establish a dedicated B2B sales team with tiered pricing for bulk buyers (80K+ unit/transaction segment)
3. **Seasonal Planning:** Plan Q4 inventory surge and run promotional campaigns in Jan–Feb to smooth demand variability

### For Netflix
1. **Family Content Gap:** Grow family-friendly content from ~15% to ~25% of the library to capture an underserved segment
2. **International Production:** Increase investment in international drama production — proven differentiated strength
3. **Cost Management:** Monitor content acquisition costs and evaluate ROI on new productions given the 2022+ slowdown

---

##  Installation & Usage

### Prerequisites
```bash
Python 3.7+
Jupyter Notebook
pip install pandas matplotlib seaborn
```

### Running the Analysis
1. Clone this repository:
   ```bash
   git clone https://github.com/richardfajorine/AnalystLab-Data-Cleaning-EDA.git
   cd AnalystLab-Data-Cleaning-EDA
   ```

2. Open the Jupyter Notebook:
   ```bash
   jupyter notebook analysis.ipynb
   ```

3. Run all cells to regenerate cleaned datasets and visualizations

### Viewing Cleaned Data
```python
import pandas as pd

# Load cleaned datasets
retail_df = pd.read_csv('OnlineRetail_CLEANED.csv')
netflix_df = pd.read_csv('Netflix_CLEANED.csv')

# View summary statistics
print(retail_df.describe())
print(netflix_df.info())
```

---

## 📈 Visualizations

Both datasets include comprehensive EDA visualizations:
- **Distribution plots** — understand data spread and outliers
- **Time series analysis** — identify trends and seasonality
- **Category breakdowns** — segment performance analysis
- **Heatmaps** — correlation and relationship insights

---

##  Learning Outcomes

Through this project, I demonstrated:
-  Practical data cleaning at scale (541K+ rows)
-  Strategic handling of missing values (domain-specific decisions)
-  Exploratory data analysis and statistical insight generation
-  Professional data visualization for business communication
-  End-to-end pipeline development (raw data → cleaned data → insights)
-  Documentation and code reproducibility

---

##  Related Projects

- [Adidas Sales Dashboard](https://github.com/your-username/adidas-sales-dashboard) — Power BI visualization project
- [Data Validation & ETL Framework](https://github.com/your-username/data-validation-etl) — Reusable data pipeline (in development)

---

##  About

**Richard Obanijesu Fajorin**  
Biomedical Engineering Student | Data Analyst | HealthTech Enthusiast  
Federal University of Technology, Akure (FUTA) | BME/25/8072

-  Email: richardfajorin@gmail.com
-  Phone: +234 8144792457
-  [GitHub](https://github.com/richardfajorin)


---

**Last Updated:** July 2026  
**Status:** ✅ Complete (Weeks 1–2 Deliverable)
