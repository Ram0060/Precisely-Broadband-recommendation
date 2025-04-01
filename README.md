## Broadband Plan Recommendation System(This is a project we worked for precosely)


This project is a Python-based recommendation system that suggests the best internet service provider plans based on user input such as age, number of devices, occupation, and county of residence. It uses Gaussian Naive Bayes classification on synthetic data to predict the most suitable provider and recommends top plans considering budget and speed.

📌 Features
Predicts the most suitable internet provider based on user demographics.

Recommends top 3 plans based on:

County-level clusters and budget ranges

Plan speed and affordability

Model-predicted probabilities for each provider

Uses Gaussian Naive Bayes for provider prediction.

Includes input validation and categorization for smoother UX.

📊 Dataset
The dataset is synthetically generated using:

Age brackets: 18-24, 25-44, 45-64, 65+

Occupations: student, it_employee, home, other

Counties: Grouped into 7 clusters for regional budget stratification

Number of connected devices: 1-4, 5-10, 11-16

Internet providers: Verizon, AT&T, Xfinity, Viasat, HughesNet

Each provider has 4 plans with associated budget and speed.

🧠 Model & Methodology
Data Encoding: All categorical features are encoded using LabelEncoder.

Feature Scaling: Features are scaled using StandardScaler.

Model Training: A GaussianNB model is trained on the encoded data.

Prediction & Recommendation:

Predicts provider probabilities from user input.

Filters and ranks plans within budget limits based on user’s county cluster.

Recommends the top 3 fastest plans from the most likely providers.

🛠️ Requirements
Python 3.11+

Libraries:

numpy

pandas

scikit-learn

Install dependencies via pip:

bash
Copy
Edit
pip install numpy pandas scikit-learn
🚀 How to Use
Run the notebook or script. The system will prompt:

bash
Copy
Edit
Enter your age: 
Enter number of devices: 
Enter your occupation: 
Enter your county:
You’ll then receive a list of the top 3 recommended plans like:

yaml
Copy
Edit
Provider: Xfinity, Plan name: Xfinity_basic2, Plan budget: $40, Plan speed: 250 Mbps, Probability: 26.73%
Provider: AT&T, Plan name: AT&T_basic1, Plan budget: $40, Plan speed: 150 Mbps, Probability: 22.84%
...
🗺️ County Clusters
County clusters are used to define a user’s expected budget range. For example:

Cluster 2 (Los Angeles) → High Budget: $80–$90

Clusters 3 & 4 → Medium Budget: $50–$60

Clusters 5 & 6 → Low Budget: $30–$40

✅ Future Improvements
Replace synthetic data with real ISP user datasets.

Integrate a GUI or web interface for user-friendly access.

Add support for more providers and plan features (e.g., data caps, upload speed).

Enhance model using advanced classifiers (e.g., Random Forest, XGBoost).

