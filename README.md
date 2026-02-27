# House Sales Prediction in King County, USA

[![IBM Data Science Professional Certificate](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/assets/logos/SN_web_lightmode.png)](https://www.coursera.org/professional-certificates/ibm-data-science)

This project analyzes and predicts house prices in King County, USA (including Seattle), using a dataset of residential properties sold between May 2014 and May 2015. Developed as part of the **IBM Data Science Professional Certification** on Coursera.

## Project Overview
As a Data Analyst at a Real Estate Investment Trust, I determine market prices based on features like square footage, bedrooms, bathrooms, floors, waterfront views, condition, grade, and location (latitude/longitude). The analysis follows a standard data science pipeline: data import, wrangling, exploratory analysis (EDA), model development, and evaluation.[file:1]

Key steps include:
- Handling missing values in `bedrooms` and `bathrooms` by replacing with column means.
- EDA: Floor value counts, boxplots for outliers (e.g., waterfront impact), regplots for correlations (e.g., `sqftabove` vs. price).
- Model development: Linear regression on features like `sqftliving`, multi-feature models, pipelines with scaling/polynomials, Ridge regression.
- Highest R² achieved via Ridge with polynomial features (~0.85-0.90 range typical).[file:1]

## Dataset
- **Source**: King County house sales data (slightly modified for course).[file:1]
- **Features** (21 total): `id`, `date`, `price` (target), `bedrooms`, `bathrooms`, `sqft_living`, `sqft_lot`, `floors`, `waterfront`, `view`, `condition`, `grade`, `sqft_above`, `sqft_basement`, `yr_built`, `yr_renovated`, `zipcode`, `lat`, `long`, `sqft_living15`, `sqft_lot15`.
- Download: [[kc_house_data.csv](data/kc_house_data.csv](https://www.kaggle.com/datasets/sumaya23abdul/house-sales-in-king-county-usa)) (21613 samples).[file:1]

## Notebook Structure
1. **Module 1**: Import data and libraries (pandas, sklearn, seaborn).
2. **Module 2**: Data wrangling (drop IDs, handle NaNs).
3. **Module 3**: EDA (stats, correlations, visualizations).
4. **Module 4**: Linear regression models and pipelines.
5. **Module 5**: Train-test split, Ridge regression, cross-validation.[file:1]

Run the notebook in Jupyter for interactive outputs, charts, and R² scores.

## Results Summary
| Model | Key Features | R² Score (Test) |
|-------|--------------|-----------------|
| Linear (sqft_living) | Single feature | ~0.49[file:1] |
| Multi-feature Linear | 10 features (floors, lat, etc.) | ~0.65[file:1] |
| Pipeline (Scale + Poly + Linear) | Same features | ~0.70[file:1] |
| Ridge (Polynomial degree 2) | Training data | ~0.87[file:1] |

`sqft_living` shows strongest correlation with price.[file:1]

## How to Run
1. Clone repo: `git clone <your-repo-url>`
2. Install deps: `pip install -r requirements.txt`
3. Launch Jupyter: `jupyter notebook`
4. Open `notebooks/House_Sales_in_King_Count_USA.ipynb`

## Author
**Tabassum Unnisa**  
Kochi, Kerala, India  


## Acknowledgments
- IBM Developer Skills Network (original template).[file:1]
- Coursera: IBM Data Science Professional Certificate.

---
*This project demonstrates end-to-end data science skills: from EDA to model refinement.*
