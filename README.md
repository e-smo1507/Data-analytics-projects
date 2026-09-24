Data Analytics Projects
Python Jupyter License Status

A portfolio of end-to-end data analytics and data science projects spanning pandemic epidemiology, real estate economics, global security, sports statistics, and quantitative finance.

📑 Table of Contents
About This Repository
Projects Overview
Technology Stack
Getting Started
Repository Structure
Contributing
License
Author
About This Repository
This repository contains a curated collection of data analytics and data science projects completed as part of an ongoing portfolio. Each project follows a rigorous workflow: problem formulation → data acquisition → cleaning → exploratory analysis → modeling → interpretation.

The work spans multiple domains and tools, demonstrating proficiency in both Python and R, statistical modeling, machine learning, geospatial analysis, and financial time-series analytics.

Projects Overview
#	Project	Domain	Language	Focus
1	🦠 COVID-19 Pandemic Analysis	Public Health	Python	Pandemic visualization & EDA
2	🏠 Cracow Real Estate Pricing	Real Estate	Python	Price prediction with ensemble ML
3	💣 Global Terrorism Database	Security / Policy	R	Geospatial EDA & trend analysis
4	⌚ Polar Watch — Workout Vitals	Sports Analytics	Python	Statistical modeling of fitness data
5	📈 FX Trading Algorithm Analysis	Quantitative Finance	Python	Algorithm performance & risk metrics
Results Snapshot
Project	Key Result
COVID-19	~35M cases analyzed; rural pop vs. cases correlation: -0.46
Cracow Real Estate	VotingRegressor ensemble outperformed MLP, GBR, and baseline
Global Terrorism	11-year EDA; ISIL, Taliban, Al-Qaida among deadliest groups
Polar Watch	Mixed model RMSE 61 vs. 79 (OLS); 283 workouts analyzed
FX Trading	92 trades; 40% win rate; Monte Carlo: 100K simulations
1. COVID-19 Pandemic Analysis
Python Status Matplotlib

A multi-notebook end-to-end exploratory data analysis of the COVID-19 pandemic. Combines JHU CSSE case time series with World Bank socioeconomic indicators to uncover trends across time, geography, and population health metrics.

Key Highlights
Global scale: ~35M confirmed cases analyzed as of October 2020
Multi-level analysis: World, continent, and country-level breakdowns
Socioeconomic integration: Correlates pandemic metrics with GDP, life expectancy, rural population, and healthcare expenditure
Reusable architecture: Custom CovidDataViz class for reproducible plotting
📂 View Project

2. Flats in Cracow
Python Status Scikit-learn

A complete data science workflow for predicting residential flat sale prices in Cracow, Poland — from web-scraped listing data through cleaning, exploratory analysis, feature engineering, and ensemble regression modeling.

Key Highlights
Ensemble modeling: VotingRegressor combining MLP and Gradient Boosting
Rich feature engineering: 8+ derived features including log-transforms and ratio features
Comprehensive preprocessing: KNN imputation, one-hot encoding, min-max scaling
Interpretability: District-level price analysis reveals central vs. outlying area premiums
📂 View Project

3. Global Terrorism Database
R Status Tidyverse

An exploratory data analysis and geospatial visualization of the Global Terrorism Database (GTD), covering 2007–2017. Examines attack patterns, casualty distributions, weapon and target types, and the most active terrorist organizations.

Key Highlights
11-year window: 2007–2017, filtered to confirmed terrorist incidents
Geospatial mapping: Annotation-style maps of group activity
Multidimensional analysis: Time, geography, attack type, weapon, target, and perpetrator
Rich visualizations: Faceted time series, correlation matrices, tile plots, stacked area charts
📂 View Project

4. Polar Watch — Workout Vitals
Python Status Statsmodels

A statistical analysis of workout data exported from a Polar watch. Heart-rate distributions, caloric expenditure, session duration, and sport-type differences are examined, with a focus on comparing strength training against cardiovascular activity.

Key Highlights
283 workouts analyzed over ~1 year
Statistical rigor: OLS regression, linear mixed models, VIF, Goldfeld-Quandt, Shapiro-Wilk, Q-Q plots
Activity comparison: Strength vs. cardio heart-rate profiles
Caloric modeling: RMSE 79 (OLS) → 61 (mixed model), R² up to 0.98 by sport
📂 View Project

5. Trading Results Analysis
Python Status Finance

Walk-forward performance analysis of an algorithmic trading system. Examines 92 trades across multiple instruments to evaluate profitability, risk characteristics, trade duration distributions, and statistical properties of returns.

Key Highlights
92 trades analyzed across multiple FX instruments
Monte Carlo simulation: 100,000 samples to estimate forward performance
Distribution analysis: Profit-per-lot characterized by skew, kurtosis, and fitted distributions
Timing edge: Identified profitable intraday patterns (2pm, 4pm)
📂 View Project

Technology Stack
Languages & Core Tools
Tool	Purpose
Python 3.8+	Primary language for 4 of 5 projects
R 4.0+	Global Terrorism analysis
Jupyter Notebooks	All analysis and modeling
Git	Version control
Python Libraries
Library	Domain	Projects
Pandas	Data manipulation	All Python projects
NumPy	Numerical computing	All Python projects
Matplotlib	Visualization	All projects
Scikit-learn	ML preprocessing & modeling	Flats in Cracow
Statsmodels	Statistical modeling	Polar
Scipy	Statistics & distributions	Polar, Trading
wbdata	World Bank API access	COVID-19
tabulate	Table formatting	Polar
R Libraries
Library	Purpose
tidyverse (dplyr, ggplot2, tidyr)	Data manipulation & viz
GGally	Matrix & pair plots
rworldmap / mapproj	Geospatial visualization
ggrepel	Non-overlapping text labels
lubridate	Date handling
scales	Axis formatting
Requirements by Project
Each project includes a requirements.txt (or requirements.R equivalent) for reproducible setup:

Project	Install Command
COVID-19	pip install -r covid19-pandemic-analysis/requirements.txt
Cracow Real Estate	pip install -r cracow-real-estate-pricing/requirements.txt
Global Terrorism (R)	See global-terrorism-eda/requirements.txt
Polar Watch	pip install -r polar-watch-fitness-analysis/requirements.txt
FX Trading	pip install -r fx-trading-analysis/requirements.txt
Getting Started
Prerequisites
Python 3.8+
R 4.0+ (for Global Terrorism project only)
Jupyter Notebook or JupyterLab
Installation
# Clone the repository
git clone https://github.com/shsarv/Data-Analytics-Projects-in-python.git
cd Data-Analytics-Projects-in-python

# Install Python dependencies (example for Flats in Cracow)
pip install pandas numpy matplotlib scikit-learn joblib

# Install R dependencies (for Global Terrorism)
install.packages(c("tidyverse", "GGally", "rworldmap", "ggrepel", "mapproj", "lubridate", "scales"))
Each project folder contains a dedicated README.md with specific setup instructions.

Repository Structure
Data-Analytics-Projects-in-python/
├── README.md                           # This file
├── LICENSE
├── covid19-pandemic-analysis/         # 🦠 Pandemic visualization
│   ├── data/
│   │   └── download_data.py
│   ├── features/
│   │   ├── make_all.py
│   │   ├── make_cases.py
│   │   ├── make_cases_daily_change.py
│   │   ├── make_cases_since_t0.py
│   │   ├── make_continents.py
│   │   ├── make_coordinates.py
│   │   ├── make_country_stats.py
│   │   ├── make_country_to_continent.py
│   │   ├── make_mortality.py
│   │   ├── make_world_bank.py
│   │   └── utils.py
│   ├── visualizations/
│   │   └── covid_data_viz.py
│   ├── notebooks/
│   │   ├── Data-wrangling.ipynb
│   │   ├── Exploratory-analysis-globally.ipynb
│   │   ├── Exploratory_analysis_fancy_plot.ipynb
│   │   ├── Exploratory-analysis-mortality.ipynb
│   │   └── Exploratory_analysis_socioeconomic.ipynb
│   └── tests/
├── cracow-real-estate-pricing/        # 🏠 Real estate ML
│   ├── 00_Data_Wrangling.ipynb
│   ├── 00_Data_Wrangling.pdf
│   ├── 01_Exploratory_Analysis.ipynb
│   ├── 01_Exploratory_Analysis.pdf
│   ├── 02_Model.ipynb
│   ├── 02_Model.pdf
│   └── img/
├── global-terrorism-eda/              # 💣 Terrorism EDA
│   ├── Global Terrorism.ipynb
│   └── img/
├── polar-watch-fitness-analysis/      # ⌚ Sports statistics
│   ├── Polar.ipynb
│   ├── Polar.pdf
│   ├── mdl_results.txt
│   └── img/
└── fx-trading-analysis/               # 📈 Algorithmic trading
    ├── Trading Results Analysis.ipynb
    ├── Trading Results Analysis.pdf
    └── img/
Contributing
Contributions, issues, and feature requests are welcome. Please feel free to open an issue or submit a pull request.

Fork the project
Create your feature branch (git checkout -b feature/AmazingFeature)
Commit your changes (git commit -m 'Add some AmazingFeature')
Push to the branch (git push origin feature/AmazingFeature)
Open a Pull Request
License
Distributed under the MIT License. See LICENSE for more information.


Built with ❤️ and a lot of ☕
