# Flight Delay Insights: Analysis and Prediction
### Data and Business Analysis Report


## 1. Executive Summary

### Purpose of the Report
The primary objective of this analysis is to examine flight performance metrics, including delays, cancellations, and diversions, to identify patterns and key contributing factors. The goal is to derive insights that can:
- Improve operational efficiency
- Optimize resource allocation
- Enhance the overall passenger experience

### Recommendations
- **Operational Improvements**: Airlines should focus on reducing carrier-related delays by improving operational factors.
- **Weather Contingency Plans**: Enhanced weather forecasting models and proactive re-routing strategies can help minimize cancellations and diversions.

## 2. Introduction

### Scope of the Analysis
This analysis investigates the following metrics:
1. **Flight Delays**: Examining departure and arrival delays, their frequency, and contributing factors.
2. **Cancellations**: Identifying trends in flight cancellations and primary reasons behind them.
3. **Diversions**: Analyzing the frequency and causes of flight diversions.
4. **Flight Performance**: Evaluating scheduled vs actual elapsed time, taxi time, and air time to assess overall efficiency.
5. **Airline and Airport Comparison**: Assessing differences in performance across airlines and airports.

## 3. Data Preparation and Cleaning

### Data Cleaning Process
#### Data Import and Initial Exploration
- Imported the dataset into **Tableau** for visualization and **Python (Pandas)** for preprocessing.
- Conducted **exploratory data analysis (EDA)** to understand the structure, identify missing values, and detect anomalies.

#### Handling Missing Values
- Identified missing values primarily in **weather-related delay columns**.
- Imputed missing values using **column median** where applicable or categorized them as "Unknown" for categorical fields.

#### Outlier Detection and Treatment
- Removed clear data-entry errors while retaining high-delay records relevant to the analysis.

#### Data Type Conversion
- Converted date columns to appropriate **datetime** format.
- Ensured numeric columns like **passenger count** were recognized correctly as integers or floats.

#### Standardizing and Normalizing Data
- Standardized categorical values for consistency (e.g., "NYC" and "New York" → "New York, NY").
- Applied scaling to columns where necessary for meaningful comparisons.

#### Feature Engineering
- Derived new columns such as **"Flight Delay Category"** based on delay duration thresholds.
- Created **quarter-based time aggregation** to identify seasonal trends.

### Data Quality Assessment
- **Completeness**: Dataset was mostly complete except for some weather delay fields.
- **Consistency**: Standardized city names and ensured uniform time formats.
- **Accuracy**: Addressed anomalies in delay durations.
- **Limitations**:
  - Some assumptions were made while imputing missing weather delays.
  - Lack of granular data on security-related delays.

## 4. Descriptive Analysis

### Summary of Key Metrics

#### **Average Departure Delay (by Airline)**
| Airline | Code | Avg. Delay |
|---------|------|------------|
| JetBlue Airways | B6 | 22 min 0 sec |
| Frontier Airlines | F9 | 19 min 31 sec |
| Spirit Airlines | NK | 15 min 43 sec |
| American Airlines | AA | 15 min 9 sec |
| Southwest Airlines | WN | 13 min 42 sec |
| United Airlines | UA | 12 min 27 sec |
| Delta Air Lines | DL | 9 min 38 sec |
| Hawaiian Airlines | HA | 8 min 5 sec |
| Alaska Airlines | AS | 5 min 49 sec |

#### **Average Departure Delay (by Origin City)**
| Origin City | Code | Avg. Delay |
|------------|------|------------|
| Bakersfield, CA | BFL | 68 min 35 sec |
| South Bend, IN | SBN | 67 min 0 sec |
| San Luis Obispo, CA | SBP | 47 min 55 sec |
| Grand Forks, ND | GFK | 47 min 0 sec |
| Monterey, CA | MRY | 37 min 1 sec |

#### **Average Arrival Delay (by Airline)**
| Airline | Code | Avg. Delay |
|---------|------|------------|
| JetBlue Airways | B6 | 16 min 28 sec |
| Frontier Airlines | F9 | 15 min 29 sec |
| Spirit Airlines | NK | 11 min 32 sec |
| American Airlines | AA | 9 min 12 sec |
| Hawaiian Airlines | HA | 6 min 48 sec |
| Southwest Airlines | WN | 6 min 44 sec |
| United Airlines | UA | 6 min 16 sec |
| Alaska Airlines | AS | 2 min 48 sec |
| Delta Air Lines | DL | 2 min 13 sec |

#### **Cancellation Rate (by Airline)**
| Airline | Cancellation Rate | Canceled Flights | Total Flights |
|---------|------------------|------------------|--------------|
| JetBlue Airways | 2.69% | 1826 | 67837 |
| Spirit Airlines | 2.61% | 1594 | 60960 |
| Southwest Airlines | 2.34% | 7920 | 338577 |
| Frontier Airlines | 2.29% | 945 | 41282 |
| American Airlines | 2.27% | 5172 | 227787 |
| Alaska Airlines | 1.73% | 1025 | 59170 |

## 5. Insights and Recommendations
### [Tableau Dashboard](https://public.tableau.com/views/Airline_17395903157640/AirlineDelay?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

### Key Findings
- **JetBlue Airways and Frontier Airlines** had the highest average departure delays.
- **Bakersfield, CA** had the longest departure delays among origin cities.
- **JetBlue Airways also had the highest cancellation rate (2.69%)**.

### Recommendations
1. **Delay Reduction Strategies**: Airlines should focus on improving turnaround times and operational efficiency.
2. **Weather Resilience Plans**: More robust forecasting models and dynamic scheduling can mitigate weather-related delays.
3. **Customer Communication**: Improved notification systems for passengers affected by cancellations and diversions.

---

This README provides an overview of the data analysis process, key metrics, and insights derived from the study. For a more detailed analysis, refer to the full report or the visualization dashboard in Tableau.
