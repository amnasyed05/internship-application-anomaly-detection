# Internship Application Anomaly Detection

## Objective
Identify anomalies in internship applications to prevent fake entries.

## Project Summary
Analyzed 40 internship applications to detect duplicate entries, rapid/bot-like 
submissions, and inconsistent data using machine learning (Isolation Forest, 
K-Means Clustering) combined with rule-based duplicate checking.

## Key Insights
- Isolation Forest flagged 6 applications (15%) as anomalies based on unusual 
  age, experience, or submission-timing patterns
- Duplicate-entry detection separately identified 2 applications submitted 
  under the same name and email — a case Isolation Forest alone could not catch
- K-Means clustering grouped applicants into 3 behavioral segments, with one 
  cluster showing a notably faster average submission gap (~5,100 seconds) 
  compared to others (~27,000 and ~48,000 seconds)
- An automated alert system was implemented to flag suspicious applications 
  by ID and name for manual review

## Recommendation
Combining statistical outlier detection (Isolation Forest), behavioral 
clustering (K-Means), and rule-based identity checks (duplicates) provides 
more reliable fraud detection than any single method alone. Flagged 
applications should be routed for human review rather than automatically 
rejected, to avoid penalizing legitimate edge cases.

## Tools Used
Excel (data prep), Google Colab, Python, pandas, scikit-learn

## Files
-`APPLICATION_DATA.CSV` — dataset
- `application_data.ipynb` — notebook with code and analysis
