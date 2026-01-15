# Singapore Public Transport: Fare and Ridership Analysis (2019-2024)

## Project Overview

This project provides a comprehensive analysis of Singapore's public transport system, examining the relationship between fare adjustments and ridership patterns from 2019 to 2024. The analysis includes data exploration, visualization, COVID-19 impact assessment, and predictive modeling using machine learning techniques.

## Objectives

- **Analyze monthly ridership trends** across Bus, MRT, and LRT from 2019-2024
- **Create standardized fare indices** to track fare evolution over time
- **Examine the relationship** between fare changes and ridership patterns
- **Assess the impact** of COVID-19 pandemic on public transport usage
- **Build predictive models** to forecast ridership based on fare and other factors
- **Provide data-driven insights** for future fare policy decisions

## Dataset

The project uses four main data sources:

1. **Ridership Data** (`ridership monthly(2019-2024).xlsx`)
   - Monthly ridership counts for Bus, MRT, and LRT
   - Period: January 2019 - December 2024 (72 months)

2. **Bus Fare Data** (`fare_review(bus)(2019-2024).xlsx`)
   - Bus fare structure across different distance bands
   - Annual fare data for 2019-2024

3. **Train Fare Data** (`fare_review(mrt&lrt)(2019-2024).xlsx`)
   - MRT & LRT fare structure across different distance bands
   - Annual fare data for 2019-2024

4. **Monthly Pass Data** (`Adult (Monthly Travel Pass2019-2024).xlsx`)
   - Adult Monthly Travel Pass prices
   - Annual pricing data for 2019-2024

All data files are located in the `data/` folder.

## Project Structure

```
CA6002-Project/
├── data/                                    # Data files folder
│   ├── ridership monthly(2019-2024).xlsx
│   ├── fare_review(bus)(2019-2024).xlsx
│   ├── fare_review(mrt&lrt)(2019-2024).xlsx
│   └── Adult (Monthly Travel Pass2019-2024).xlsx
├── SMRT_DATA_work.ipynb                     # Main analysis notebook
├── master_dataset.csv                        # Generated master dataset
├── *.png                                     # Generated visualization files
└── README.md                                 # This file
```

## Notebook Structure

The main notebook (`SMRT_DATA_work.ipynb`) is organized into the following sections:

1. **Introduction & Objectives** - Project background and goals
2. **Setup & Library Imports** - Import necessary libraries
3. **Data Loading** - Load all data files
4. **Data Exploration** - Explore each dataset's structure
5. **Feature Engineering** - Create fare indices and features
6. **Data Preprocessing** - Clean and transform data
7. **Exploratory Data Analysis** - Visualize trends and patterns
8. **COVID-19 Impact Analysis** - Quantify pandemic effects
9. **Model Training & Evaluation** - Build and compare ML models
10. **Summary & Conclusions** - Key findings and recommendations

## Key Features

### Data Analysis
- Comprehensive ridership trend analysis
- Fare evolution tracking
- COVID-19 impact quantification
- Seasonal pattern identification
- Mode-specific analysis (Bus, MRT, LRT)
- Fare-ridership relationship analysis

### Visualizations
- Time series plots of ridership trends
- Fare evolution charts
- COVID-19 impact comparisons
- Seasonal pattern visualizations
- Mode share analysis
- Correlation heatmaps
- Model performance comparisons

### Machine Learning Models
- **Linear Regression** - Baseline interpretable model
- **Random Forest Regressor** - Advanced ensemble model
- Model comparison and evaluation metrics
- Prediction visualizations
- Residual analysis

## Requirements

### Python Libraries
- `pandas` - Data manipulation
- `numpy` - Numerical operations
- `matplotlib` - Data visualization
- `seaborn` - Statistical visualizations
- `scikit-learn` - Machine learning models
- `openpyxl` - Excel file reading

### Installation

Install required packages using pip:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl
```

## Usage

1. **Clone or download** this repository
2. **Ensure all data files** are in the `data/` folder
3. **Open** `SMRT_DATA_work.ipynb` in Jupyter Notebook or Google Colab
4. **Run all cells** sequentially to reproduce the analysis

### Running the Notebook

The notebook is designed to be run from top to bottom. Each section builds upon the previous one:

- **Cells 1-3**: Setup and data loading
- **Cells 4-7**: Data exploration
- **Cells 8-10**: Feature engineering
- **Cells 11-12**: Data preprocessing
- **Cells 13-16**: Exploratory data analysis
- **Cells 17-20**: Additional analysis
- **Cells 21-25**: Model training and evaluation
- **Cell 26**: Summary and conclusions

## Key Findings

### Ridership Trends
- Average monthly ridership varies significantly across the study period
- COVID-19 caused a substantial decrease in ridership
- Recovery patterns differ by transport mode

### Fare Evolution
- Gradual fare increases across both bus and train systems
- Approximately 16-17% increase from 2019 to 2024
- Monthly pass prices remained stable after initial increase

### COVID-19 Impact
- Significant negative impact on ridership during pandemic period
- Recovery ongoing as of 2024
- Mode-specific recovery patterns observed

### Model Performance
- Both Linear Regression and Random Forest models show good predictive capability
- Random Forest generally performs better in capturing non-linear relationships
- Models can effectively forecast ridership patterns

## Output Files

The notebook generates several output files:

- `master_dataset.csv` - Combined and processed dataset
- `covid_impact_ridership.png` - COVID-19 impact visualization
- `seasonal_patterns.png` - Seasonal analysis charts
- `fare_evolution.png` - Fare trend visualizations
- `mode_specific_analysis.png` - Mode-specific analysis
- `fare_ridership_relationship.png` - Fare-ridership correlation analysis
- `model_comparison.png` - Model performance comparison
- `model_predictions_timeseries.png` - Time series predictions

## Methodology

### Fare Index Creation
- Average fares across all distance bands for each year
- Convert from cents to dollars
- Create standardized indices for comparison

### Feature Engineering
- COVID-19 dummy variable (Mar 2020 - Dec 2021)
- 12-month lagged ridership variable
- Quarterly indicators
- Temporal features (month, year)

### Model Training
- Train-test split: 80-20 (temporal split)
- Feature selection based on domain knowledge
- Model evaluation using RMSE, MAE, and R² metrics
- Cross-validation considerations

## Limitations

- Limited to adult card-based fares (excludes student/senior/cash fares)
- Monthly aggregation may miss daily/weekly patterns
- External factors (economic conditions, weather) not fully captured
- Small dataset size (72 months) limits model complexity

## Future Enhancements

- Include additional external factors (economic indicators, weather data)
- Expand to include other fare types (student, senior)
- Implement more advanced time series models
- Add real-time prediction capabilities
- Include route-specific analysis

## Author

CA6002 Project - Singapore Public Transport Analysis

## License

This project is for educational purposes as part of the CA6002 course.

## Acknowledgments

- Data sources: Singapore public transport authorities
- Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn communities

## Contact

For questions or issues, please refer to the project documentation or contact the project maintainer.

---

**Last Updated:** 2024
**Project Status:** Complete
