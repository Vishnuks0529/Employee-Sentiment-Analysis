# Employee-Sentiment-Analysis

#Project Overview

This project analyzes employee email messages to evaluate sentiment trends, engagement levels, and flight risks. Using natural language processing (NLP) and statistical analysis, we derive insights from raw text data.

##Steps and Methodology

#Step 1: Load Dataset

We load the raw dataset from a CSV file and verify its structure by checking the initial rows.

#Step 2: Sentiment Labeling

We define positive and negative keywords and apply a function to label each message as Positive, Negative, or Neutral.

#Step 3: Exploratory Data Analysis (EDA)

We analyze the dataset by calculating basic statistics, checking for missing values, and visualizing sentiment distribution and trends over time.

#Step 4: Employee Score Calculation

Each employee’s monthly sentiment score is computed by summing +1 (Positive), -1 (Negative), and 0 (Neutral) messages.

#Step 5: Employee Ranking

We rank employees by sentiment scores, identifying top three positive and top three negative employees each month.

#Step 6: Flight Risk Identification

We apply a rolling 30-day window to count negative messages per employee. Employees with 4 or more negatives in 30 days are flagged as flight risks.

#Step 7: Predictive Modeling

We build a linear regression model to predict sentiment scores using features like message frequency and length.



##Key Results

Sentiment Distribution

Positive: 36 messages

Neutral: 2154 messages

Negative: 1 message


Top 3 Positive Employees (Sample)
Rank	Employee	Month	Score
1	don.baughman@enron.com
	2010-01	1
2	sally.beck@enron.com
	2010-01	1
3	bobette.riner@ipgdirect.com
	2010-01	0

Top 3 Negative Employees (Sample)
Rank	Employee	Month	Score
1	bobette.riner@ipgdirect.com
	2010-01	0
2	eric.bass@enron.com
	2010-01	0
3	john.arnold@enron.com
	2010-01	0


##Flight Risk Employees

Employees who sent 4 or more negative emails in 30 days:

[No flight risks identified in this dataset]



##Predictive Model Performance

Mean Squared Error (MSE): 0.0268375764710145

R-squared Score (R²): -0.009399799974703749



##Project Structure

The project folder is organized as follows:

Employee-Sentiment-Analysis/
│
├── esa.ipynb
├── esa.py
├── test.csv
├── README.md
├── Final_Report.docx
├── requirements.txt
│
└── visualizations/
    ├── sentiment_distribution.png
    ├── monthly_scores.png
    ├── employee_ranking.png
    ├── flight_risk.png
    ├── regression_results.png



##How to Run

Install required libraries by running:

pip install -r requirements.txt

Launch Jupyter in the project folder with:

jupyter notebook

Run all cells in esa1.ipynb.

Review visualizations in the visualizations/ folder.

##Conclusion

This project automated sentiment labeling, employee scoring, ranking, flight risk identification, and developed a predictive model to analyze trends. The codebase, visualizations, and insights offer a practical approach to measuring employee engagement and predicting sentiment trends.
