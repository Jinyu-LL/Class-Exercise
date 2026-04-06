# Streamlit Sales Dashboard

This project is a Streamlit Community Cloud–ready interactive dashboard built from:

- `orders.csv`
- `returns.csv`
- `customers.csv`

It merges the datasets, applies light cleaning, and exposes interactive Plotly charts with sidebar filters for:

- Region
- Category
- Order date range

## Files

- `app.py` — main Streamlit application
- `requirements.txt` — Python dependencies
- `orders.csv`, `returns.csv`, `customers.csv` — source data files

## Features

- KPI cards:
  - Total Sales
  - Total Profit
  - Returned Orders
  - Profit Margin
- Plotly charts:
  - Monthly Sales and Profit trend
  - Top 10 Sub-Categories by Sales
  - Sales vs Profit by Region
  - Sales and Profit by Customer Segment
  - Discount vs Profit scatter plot
- Filtered table view
- Download filtered data as CSV

## Run locally

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Deploy to Streamlit Community Cloud

1. Create a new GitHub repository.
2. Upload these files to the repository root:
   - `app.py`
   - `requirements.txt`
   - `orders.csv`
   - `returns.csv`
   - `customers.csv`
3. Sign in to Streamlit Community Cloud.
4. Click **Create app**.
5. Select your GitHub repository and branch.
6. Set the main file path to:

```text
app.py
```

7. Click **Deploy**.

After deployment, Streamlit will generate a public `*.streamlit.app` URL.

## Notes

- File paths are relative, so the app works on both local machines and Streamlit Community Cloud.
- `st.cache_data` is used to speed up reloads.
- The dashboard is designed for small to medium-sized CSV datasets.