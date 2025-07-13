Retail Price Optimization ML Model
Role: ML Developer | Tools: Python, Scikit-learn, XGBoost, PuLP, Pandas, NumPy

I developed a machine learning-based retail price optimization model designed to maximize sales volume by recommending optimal pricing strategies for retail products. The model was built using a real-world dataset that included both product metadata and competitive pricing signals.

Dataset Highlights:
676 product-month records across multiple categories

Features used:

Sales metrics: quantity sold, total and unit price, freight cost

Product metadata: name length, description length, photo quantity, weight, rating

Temporal info: month, year, holidays, weekday/weekend flags

Competitive data: prices, scores, and freight prices of 3 competitors

Lag features: previous month's price

Key Components:
Demand Estimation

Built regression models (e.g. XGBoost) to predict qty sold using unit_price, product attributes, time features, and competitor prices.

Evaluated feature importance to understand drivers of customer demand.

Price Elasticity Modeling

Estimated price elasticity at a product level by analyzing changes in sales w.r.t. price fluctuations over time.

Used lagged prices and competitive pricing as key elasticity indicators.

Sales-Driven Optimization Engine

Designed a constrained optimization model using linear programming (PuLP) to suggest price points that maximize unit sales under constraints:

Min/max price range

Margin thresholds

Inventory or freight cost limits

Scenario Simulation

Enabled what-if analysis to visualize the impact of different pricing strategies on expected sales using historical behavior.
