Data Cleaning & EDA: OnlineRetail & Netflix Datasets
Author: Richard Obanijesu Fajorin
Program: AnalystLab Africa, Data Analyst Internship (Week 1–2)
Tools: Python, Pandas, Jupyter Notebook, Matplotlib, Seaborn
Overview
End-to-end data cleaning and exploratory data analysis (EDA) on two Kaggle datasets: an e-commerce transaction log (OnlineRetail) and a media catalog (Netflix Titles): covering missing-value handling, outlier treatment, format standardization, statistical summaries, and visualization.
Repository Contents
File
Description
OnlineRetail_CLEANED.csv
Cleaned e-commerce dataset (~405K rows)
Netflix_CLEANED.csv
Cleaned Netflix catalog (8,809 rows)
OnlineRetail_EDA.png
4-panel visualization of retail trends
Netflix_EDA.png
4-panel visualization of content trends
analysis.ipynb
Full Jupyter Notebook with documented analysis
Data Cleaning
OnlineRetail Dataset
Missing CustomerID (135,080 rows): dropped, required for customer-level analysis
Missing Description (1,454 rows): dropped, incomplete product info
Negative unit prices: removed as data quality issues (likely refund artifacts)
Negative quantities: kept, represent legitimate returns
Date format standardized from MM/DD/YYYY HH:MM to datetime
Result: 541,909 rows → ~404,000+ usable rows
Netflix Dataset
Missing director (~29%), cast (~9%), date_added (~10%) — kept, reflect legitimate gaps in older/undocumented titles
Missing country: filled with 'Unknown'
Missing rating: filled with 'Not Rated'
Mixed duration format ("90 min" vs "2 Seasons"): parsed into numeric fields
Result: 8,809 rows fully processed, no rows deleted
Key Findings
OnlineRetail
UK generates 50%+ of total revenue; international markets remain underdeveloped
Top 10 products drive a disproportionate share of revenue (concentration risk)
Consistent month-over-month growth with a Q4 seasonal peak
Bulk orders (80K+ units/transaction) indicate an identifiable B2B segment
Low return rate (~3–5%) suggests solid product quality
Top 10 customers account for ~15% of total revenue
Netflix
TV Shows (60%) outnumber Movies (40%): a retention-oriented content strategy
Content additions peaked in 2021, declining from 2022 onward (likely cost management)
USA leads production (35%); India and South Korea are emerging content hubs
Mature-rated content dominates (TV-MA/R = 50%+); family content is comparatively scarce (~15%)
Dramas, International TV, and Documentaries are the top genres
Clear global sourcing strategy with localized content per major market
Recommendations
OnlineRetail
Expand top-selling products into Netherlands, Sweden, and Germany: proven demand, high potential
Establish a dedicated B2B sales team with tiered pricing for bulk buyers
Plan Q4 inventory surge and run promotional campaigns in Jan–Feb to smooth demand
Netflix
Grow family-friendly content from ~15% to ~25% of the library to capture an underserved segment
Increase investment in international drama production, a proven and differentiated strength
Monitor content acquisition costs and evaluate ROI on new productions given the 2022+ slowdown
Part of the AnalystLab Africa Data Analyst Internship.