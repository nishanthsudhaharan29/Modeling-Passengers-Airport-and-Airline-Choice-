# Modeling Passengers’ Airport and Airline Choice Behavior using ML

## Project Description

This project presents an in-depth analysis and predictive modeling of passengers’ airport and airline choices within the Seoul Metropolitan Area, with a focus on the two major airports: Gimpo (GMP) and Incheon (ICN). The primary objective is to identify key factors influencing traveler decisions and develop models that accurately predict their preferences.

The study is based on a structured survey dataset of 488 respondents, capturing both socio-demographic and alternative-specific attributes. Through exploratory data analysis (EDA), correlation assessments, and targeted data preprocessing, the dataset is prepared for effective model development.

The findings aim to support stakeholders—such as airlines, airport authorities, and transportation policymakers—by offering insights to enhance service efficiency, tailor marketing strategies, and inform infrastructure planning.

---

## Dataset Summary

- **Total Records:** 488
- **Variables:** 27
- **Target Variables:**
  - `Airport Choice` (ICN or GMP)
  - `Airline Choice` (Korean Air, Asiana Air, Korean LCC, Foreign Carriers)

### Key Features

- **Demographics:** Age, Gender, Nationality, Occupation, Income Class  
- **Trip Details:** Purpose of trip, Trip duration, Number of flying companions, Destination  
- **Travel Logistics:** Mode of transport to airport, Number of transport modes used, Access time, Access cost  
- **Flight Details:** Airline, Seat class, Airfare, Departure hour and minute, Mileage, Frequent flyer program

---

## Exploratory Data Analysis (EDA)

### Correlation Analysis

- Positive correlations observed among `ModeTransport`, `AccessCost`, `AccessTime`, and `Mileage`, reflecting expected travel dynamics.
- Moderate positive correlation between `Airfare` and `SeatClass`, confirming typical fare-tier patterns.
- Minimal correlation between identifier-like variables (`ID`, `Airport`, `Airline`) and other features, indicating independence.

### Visual Insights

- Distribution plots and heatmaps were used to reveal patterns in departure timing, airline choice by demographic segment, and access methods.
- Demographic and trip-specific variables appear to influence both airport and airline choices.

---

## Data Cleaning and Preprocessing

### Missing Value Analysis

| Variable           | Approx. Missing Count |
|--------------------|------------------------|
| Mileage            | ~400                   |
| Mileage/Airline    | High                   |
| AccessCost         | Moderate               |
| Airfare, FlightNo  | ~50% missing           |

### Imputation and Treatment

- **Dropped Variables:** High-null columns with limited modeling utility.
- **Retained and Treated Variables:**
  - **Access Time:** Imputed using group mean based on `ProvinceResidence`, `ModeTransport`, and `NoTransport`, reducing missing values from 97 to 15.
  - **Departure Hour:** Imputed using the mode based on `Destination` and `DepartureTime`, ensuring consistency with temporal travel trends.

These preprocessing steps preserved data integrity while enhancing feature usability for modeling.

---

## Project Objectives and Outcomes

- Identify key factors driving passengers’ choice of airport and airline.
- Build predictive models to support transportation planning and strategic marketing.
- Generate actionable insights to enhance the passenger experience and optimize service design.

---

## Tools and Technologies

- Python (pandas, numpy, matplotlib, seaborn)
- Jupyter Notebooks
- Scikit-learn
- Behavioral modeling and survey data analysis techniques
