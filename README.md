# 📈 Sales Forecasting Dashboard

This project uses **Time Series Forecasting** with Facebook’s `Prophet` model in Python to predict future sales and visualizes the results using **Power BI**.

It is designed as a beginner-friendly walkthrough from raw data → forecasting → dashboarding → sharing, combining data science and business intelligence tools.

---

## 📦 Project Structure

| File/Folder            | Description |
|------------------------|-------------|
| `sales_data.csv`       | Raw historical sales data (Date, Article_ID, Country_Code, Sold_Units) |
| `forecast_model.ipynb` | Jupyter notebook with full Python code for cleaning, forecasting, and exporting results |
| `forecast_output.xlsx` | Prophet forecast output with confidence intervals |
| `SalesForecast.pbix`   | Power BI dashboard showing interactive forecast visualizations |
| `README.md`            | Project overview and instructions |

---

## 📊 Tools & Technologies

- 🐍 **Python** (Pandas, Prophet)
- 📊 **Power BI Desktop**
- 📁 **Excel / CSV** for intermediate data storage
- 🖥️ **Jupyter Notebook**
- ☁️ **GitHub** for version control

---

## 🔧 How It Works

### Step 1: Load and Prepare Data
- Load historical sales data from `sales_data.csv`
- Filter for one `Article_ID` and `Country_Code`
- Convert date to `datetime`, group by day

### Step 2: Forecast with Prophet
- Train Prophet model on daily sales data
- Predict sales for the next 30 days
- Export forecast results (`ds`, `yhat`, `yhat_lower`, `yhat_upper`) to Excel

### Step 3: Visualize in Power BI
- Import forecast into Power BI
- Create:
  - Line chart for actual vs forecasted sales
  - Clustered bar chart for accuracy comparison
  - Optional filters (date, article, country)
- Format the dashboard for business users

---

## 📌 Key Columns in Forecast Output

| Column        | Description |
|---------------|-------------|
| `ds`          | Date of forecast |
| `y`           | Actual sales (if available) |
| `yhat`        | Forecasted sales |
| `yhat_lower`  | Lower confidence bound |
| `yhat_upper`  | Upper confidence bound |

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/sales-forecast-dashboard.git
cd sales-forecast-dashboard
