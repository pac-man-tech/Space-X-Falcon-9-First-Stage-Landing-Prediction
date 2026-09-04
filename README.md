SpaceX Falcon 9 Launch Analysis & Predictive Modeling
An end-to-end data science capstone project analyzing SpaceX Falcon 9 launch data. This project covers data collection, exploratory data analysis (EDA), interactive dashboard visualization, spatial mapping, and machine learning model evaluation to predict the success of first-stage booster landings.

Project Overview
SpaceX advertises Falcon 9 rocket launches on its website with a cost of 62 million dollars; other providers cost upward of 165 million dollars each, much of the savings is due to SpaceX being able to reuse the first stage. Determining if the first stage will land allows us to determine the cost of a launch. This project aims to predict if the SpaceX Falcon 9 first stage will land successfully using public launch data and supervised machine learning techniques.

Key Features & Deliverables
Data Collection & Wrangle:

SpaceX API: Pulled detailed launch records, unpacked JSON payloads, and filtered records specifically for Falcon 9 boosters.

Web Scraping: Extracted historical launch records from Wikipedia using BeautifulSoup.

Exploratory Data Analysis (EDA):

SQL Analytics: Queried launch metrics, payload mass distributions, and success rates across launch sites.

Data Visualization: Built visual relationship maps using Pandas, Matplotlib, and Seaborn to analyze relationships between payload mass, flight number, orbit types, and landing outcomes.

Interactive Maps & Dashboards:

Folium Interactive Maps: Plotted launch site locations, outcome markers, proximity measurements (to coastlines, railways, and highways), and cluster maps.

Plotly Dash Application: Developed a real-time web dashboard featuring dynamic site selection dropdowns, payload sliders, pie charts, and scatter plots.

Machine Learning & Prediction:

Formulated binary classification pipelines using Logistic Regression, Support Vector Machines (SVM), Decision Trees, and K-Nearest Neighbors (KNN).

Hyperparameter tuning via GridSearchCV to determine the best-performing model for predicting landing outcomes.

Repository Structure
Plaintext
├── 1_Data_Collection_API.ipynb         # API data extraction script
├── 2_Data_Collection_Scraping.ipynb    # Web scraping launch records
├── 3_Data_Wrangling.ipynb              # Data cleaning and binary target generation
├── 4_EDA_SQL.ipynb                     # SQL queries and database analytics
├── 5_EDA_Visualization.ipynb           # Visualization scripts (Seaborn/Matplotlib)
├── 6_Interactive_Map_Folium.ipynb      # Folium maps and spatial analysis
├── spacex_dash_app.py                  # Interactive Plotly Dash dashboard app
├── 7_Machine_Learning_Prediction.ipynb # ML models, grid search, and evaluation
├── dataset_part_1.csv                  # Processed API dataset
├── dataset_part_2.csv                  # Dataset with landing outcome classes
├── dataset_part_3.csv                  # One-hot encoded feature dataset
└── README.md                           # Project documentation
Installation & Setup
Prerequisites
Python 3.8+

Jupyter Notebook / JupyterLab

Environment Setup
Clone the repository:

Bash
git clone https://github.com/your-username/spacex-capstone.git
cd spacex-capstone
Install required dependencies:

Bash
pip install pandas numpy matplotlib seaborn folium plotly dash scikit-learn requests beautifulsoup4
How to Run
1. Jupyter Notebooks
Run the notebooks sequentially (1_Data_Collection_API.ipynb through 7_Machine_Learning_Prediction.ipynb) to view the data pipeline, spatial analysis, and model training.

2. Plotly Dash Dashboard
Launch the interactive web application locally:

Bash
python spacex_dash_app.py
Navigate to [http://127.0.0.1:8050/](http://127.0.0.1:8050/) in your web browser.
