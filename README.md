# ✈️ Modeling Passengers’ Airport and Airline Choice Behavior

## 📘 Project Description

This project presents an in-depth analysis and predictive modeling of passengers’ airport and airline choices within the Seoul Metropolitan Area, focusing on Gimpo (GMP) and Incheon (ICN) airports. The primary goal is to uncover key factors influencing traveler decisions and develop models that accurately predict their preferences.

The study leverages a survey dataset of 488 respondents, enriched with both socio-demographic and alternative-specific attributes. Using exploratory data analysis (EDA), correlation mapping, and thoughtful data preprocessing, we prepare a clean dataset suitable for model development.

Ultimately, this project aims to support stakeholders—such as airlines, airports, and policy-makers—by offering insights that can guide more efficient service delivery, targeted marketing, and infrastructure planning.

---

## 📊 Dataset Summary

- **Total Records:** 488
- **Variables:** 27
- **Key Targets:**
  - `Airport Choice` (ICN or GMP)
  - `Airline Choice` (Korean Air, Asiana Air, Korean LCC, Foreign Carriers)

### 🔍 Key Features

- **Demographics:** Age, Gender, Nationality, Income Class, Occupation  
- **Trip Details:** Purpose, Duration, Companions, Flight Time, Destination  
- **Travel Logistics:** Access Time, Access Cost, Mode of Transport, No. of Transport Modes  
- **Flight Details:** Airline, Seat Class, Airfare, Mileage, Frequent Flight Destination  

---

## 📈 Exploratory Data Analysis (EDA)

- **Correlation Highlights:**
  - Positive correlation among `ModeTransport`, `AccessCost`, `AccessTime`, and `Mileage`.
  - `Airfare` is moderately correlated with `SeatClass`, validating fare-tier alignment.
  - Sparse correlation for identifiers (e.g., `Respondent ID`, `Airport`, `Airline`) suggesting independence.

- **Visual Insights:**
  - Heatmaps and distribution plots revealed patterns in departure times and access methods.
  - Airline preference appears linked to demographic segments and trip purpose.

---

## 🧹 Data Cleaning & Preprocessing

### ❗ Missing Value Analysis

| Variable         | Missing Count |
|------------------|----------------|
| Mileage          | ~400           |
| Mileage/Airline  | High           |
| AccessCost       | Moderate       |
| Airfare, FlightNo| ~50% missing   |

### ✅ Imputation Strategies

- **Dropped:** Variables with excessive nulls or non-contributive information
- **Kept & Imputed:**
  - **Access Time**: Group mean imputation by `ProvinceResidence`, `ModeTransport`, and `NoTransport`  
    - Reduced missing from 97 → 15
  - **Departure Hour**: Imputed using mode by `Destination` and `DepartureTime`

These imputation strategies maintained model interpretability and data integrity.

---

## 🚀 Objectives & Outcomes

- Understand drivers behind airport and airline choices
- Create predictive models for transportation policy and marketing decisions
- Provide data-driven support to improve passenger experience

---

## 📎 Tools & Technologies

- Python (pandas, numpy, seaborn, matplotlib)
- Jupyter Notebooks
- Scikit-learn
- Survey & behavioral data modeling
