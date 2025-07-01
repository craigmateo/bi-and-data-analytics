# Introduction

To find signals in data, we must learn to reduce the noise — not just the noise that resides in the data, but also the noise that resides in us. It is nearly impossible for noisy minds to perceive anything but noise in data.

> *Stephen Few, Information Technology Author, Innovator, Teacher, and Consultant*

The Fellowship of Data Miners. Hardy souls whose singular purpose is to scour reams of data for the factoids that, layered in the nacre of analysis, will become the pearls of wisdom that will rid the world of the evils of bad decision making.

After you complete this module, the topic of which is data mining, you will be one step closer to joining the ranks of The Fellowship. You also will have newfound respect for the Guild of Semantic Analysts and the job they do, day-after-day, sorting through endless arrays of textual data in search of human understanding.

[“Big Data Analytics Lifecycle” (Erl, Khattak, & Buhler, 2016, p. 54).](images/data_mining.png)

---

## Learning Outcomes

By the end of this module, you should be able to complete the following:

- Interpret the term data mining.
- Outline and explain data mining tasks.
- Identify the purpose of data clustering.
- Distinguish between linear regression and logistic regression.
- Explain the term dichotomous variable.
- Interpret different types of semantic analysis.
- Execute a multiple linear regression task using the Weka data mining tool.
- Implement a data clustering task using the Weka data mining tool.
- Execute a logistic regression task using the Weka data mining tool.
- Execute a document classification task using the Weka data mining tool.

---

## Key Terms and Concepts

**Clustering**  
Identification of data groups whose occupants are in some way similar.

**Data Mining**  
Searching through large amounts of data for unknown patterns, anomalies, or relationships between variables.

**Dichotomous Variables**  
Variables that have two categories (e.g., heads or tails).

**Natural Language Processing (NLP)**  
Machines learning how to understand human speech and text and, in some cases, make decisions based on the information.

**Overfit**  
A statistical model that overstates the accuracy of its predictions.

**Sentiment Analysis**  
Scoring words, as well as voice inflections, to obtain readings on persons’ feelings about a topic of a discussion.

# The Leopard’s Spots

- Linear regression is a fundamental tool in inferential statistics.
- It enables making predictions based on how independent (predictor) variables affect dependent (response) variables.
- Predictions come from simple or multiple regression equations.
- Regression equations can be expressed in different forms.
- Various step-by-step methods exist for solving regression equations to find response variable values.
- Whether or not you have encountered these methods before, this module offers a unique approach to linear regression.
- Activity #1 in this module will have you use the Weka data mining tool to:
  - Perform classification by regression.
  - Obtain information needed to formulate a regression equation.

# Data Mining Overview

- **Data extraction (Module 5)** differs from **data mining** (current topic).
- Data mining is like being in a processing facility, analyzing extracted data.
- It involves searching large datasets for **unknown patterns, anomalies, or relationships**.
- According to Erl et al. (2016), data mining is foundational for **predictive analytics** and **business intelligence**.

## Business Context
- Data mining analyzes historical business data stored in data warehouses.
- Automated software tasks identify groupings or relationships across data.

## Key Data Mining Tasks
- **Anomaly detection:** Find unusual data needing further investigation.
- **Association rule learning:** Discover relationships between variables (e.g., products often bought together).
- **Clustering:** Group data into similar clusters without predefined categories.
- **Classification:** Use training data to categorize new data (e.g., spam detection).
- **Regression:** Identify relationships among datasets.
- **Summarization:** Create compact data representations (e.g., reports, visualizations).

## Machine Learning Relation
- Classification = supervised machine learning (uses labeled training data).
- Clustering = unsupervised machine learning (categories emerge naturally).

## Cluster Analysis in Business
- Used to group data for marketing or advertising strategies.
- Examples of consumer clusters:
  - **Demanders:** Seek high-quality goods and service.
  - **Escapists:** Avoid intense marketing pressure.
  - **Educationalists:** Interested in learning and new experiences.
- Tailored marketing can target each group’s preferences.

## Other Applications of Clustering
- Identifying manufacturing problems.
- Preventing customer attrition.
- Acquiring new customers.
- Cross-selling to existing customers.
- Profiling customers more accurately.

## Important Considerations
- Not all patterns found are valid; beware of **overfitting**.
- Use test datasets to validate patterns found in training data.
- Adjust data mining design if test results do not match targets.
- Confirm and convert validated patterns into actionable insights.

## Exclusive Disjunction

- When two horses race, only one wins — not both.
- This illustrates **exclusive disjunction**: only one of two possible outcomes occurs, never both or neither.
- In data analytics, such outcomes are called **dichotomous variables** (e.g., pass/fail, heads/tails, male/female).
- **Binary dichotomous variables** assign one category a value of 1 and the other a value of 0.
- **Logistic regression** predicts the probability of each dichotomous outcome.
  - It’s a type of machine learning using prior data to classify unknown data.
  - As more data is processed, the model improves.
- Difference between logistic and linear regression:
  - Logistic regression: dependent variable is binary/categorical.
  - Linear regression: establishes a linear relationship between independent and continuous dependent variables.
- Logistic regression can analyze multiple attributes simultaneously to classify outcomes.
- Example: classifying governments as democracies (Y) or dictatorships (N) using multiple attributes.

### Logistic Regression in Business

- Used to improve strategies that increase revenue and reduce expenses or losses.
- Example: credit card issuers predict likelihood of applicant default based on variables like income and payment history.
- Used in online advertising to predict user likelihood to click on ads (yes/no probabilities).
- Cautions:
  - Including irrelevant variables reduces model’s predictive power.
  - Cannot predict continuous outcomes (e.g., exact sales figures).
  - Beware of **overfitting** — model appears more accurate than it is due to sample bias.

## Semantic Analysis and Text Mining

- When you post on social media, your words are scanned by automated data mining engines.
- These engines seek to:
  - Understand the meaning of your comments.
  - Find associations between your words and marketing triggers.
  - Detect emotional intensity to tailor responses.
- Machines analyzing **unstructured data** (human speech and text) are called **semantic analysts** — smiths of words.

### Three Categories of Semantic Analysis (Erl et al., 2016, p.198)

1. **Natural Language Processing (NLP)**
   - Machines learn to understand human speech and text.
   - Applications:
     - Conversational interfaces (smart assistants, in-home devices).
     - Grammar/spell check and auto-complete.
     - Website chatbots.

2. **Sentiment Analysis**
   - Algorithms score words and voice inflections to gauge feelings.
   - Uses include:
     - Brand reputation monitoring.
     - Customer support performance improvement.
     - Political opinion analysis for better messaging.

3. **Text Analytics**
   - Uses data mining, machine learning, and NLP to extract value from unstructured text.
   - Applications across industries:
     - Manufacturers analyze competitor products.
     - Insurers detect fraudulent claims.
     - Legal firms find keywords in documents.
     - Healthcare providers identify patterns in medical reports.

### Objective of Semantic Analysis

- Transform unstructured text into structured data.
- Discover new knowledge through this transformation.

