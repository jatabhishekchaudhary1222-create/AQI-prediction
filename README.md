# AQI-prediction
this is a small ml project created by me on aqi prediction
"Predictive Analytics for Air Quality under Data Constraints"
Public Health Crisis: Air pollution is a major driver of respiratory diseases; however, monitoring systems are often reactive rather than predictive.

The Data Integrity Gap: Real-world environmental data (pollutants, weather, traffic) is "dirty." It contains categorical strings (e.g., City names like 'Amritsar'), complex date formats, and inconsistent values that standard Machine Learning algorithms cannot process directly.

Technical Bottleneck: As seen in initial model iterations, standard regression and classification models fail when encountering non-numerical data, requiring a full ML lifecycle approach to resolve.

To solve the data inconsistencies and provide accurate AQI predictions, the project follows a four-stage technical solution:

1. Automated Preprocessing (The Fix for 'ValueError')
Categorical Encoding: Converting non-numeric city and station data into numerical formats using Label Encoding or One-Hot Encoding.

Temporal Transformation: Converting raw date strings (e.g., '2018-11-04') into seasonal features (Month, Day, Hour) to help the model learn time-based pollution patterns.

2. Feature Engineering
Creating Lag Features (using previous hours' data) to account for the persistence of pollutants in the atmosphere.

Normalizing weather and traffic data to a unified scale for better model convergence.

3. Robust Modeling
Moving from simple Decision Trees to Random Forest Regressors.

Why Random Forest? It handles the non-linear relationship between traffic density and wind speed more effectively, providing more stable predictions.

4. Scalable Deployment
The project is hosted on GitHub to ensure version control and transparency.

The code is structured for reproducibility, allowing other researchers to apply the same cleaning pipeline to different cities.
