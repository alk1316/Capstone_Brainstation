<a name="readme-top"></a>
<br />
<div align="center">

  # Inventory Analysis Capstone Project
### Analysis to Predict Demand and Inventory Levels

  </a>


</div>

## Project Overview

The objective of this project is to conduct a comprehensive analysis of the manufacturing company's inventory to identify patterns and areas for improvement. Techniques will be applied to model demand and optimize inventory levels.

The specific solutions include:

 - Demand Modeling: Forecasting demand to avoid stockouts and excess inventory.

 - Inventory Optimization: Implementing optimization strategies such as EOQ (Economic Order Quantity) and ABC analysis to efficiently manage inventory.

## Table of Contents
  <ol>
    <li><a href="#motivation">Project Motivation</a></li>
    <li><a href="#opportunity">The opportunity</a></li>
    <li><a href="#keytakeaway">Key Takeaway</a></li>
    <li><a href="#data">The Data</a></li>
    <li><a href="#dict">Data Dictionary</a></li>
    <li><a href="#roadmap">Project Roadmap</a></li>
    <li><a href="#progression">Project progression</a></li>
    <li><a href="#repo">Repository</a></li>
    <li><a href="#learnings">Learnings</a></li>
    <li><a href="#conclusions">Conclusions</a></li>
    <li><a href="#next">Next Steps</a></li>
  </ol>
  </details>
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2 id="motivation"> Project Motivation </h2>
As a SAP Business One consultant with over a decade of experience, I have observed a recurring challenge in every company where I have implemented this powerful ERP: managing inventory levels. 

During each new implementation, it's common for upper management to ask if the system can automatically calculate optimal stock levels based on existing information. Unfortunately, the answer has always been a resounding "No". And few companies choose to invest in this analysis; many continue to operate intuitively, without using the existing data as a guide for decision-making. 

This challenge has been a constant throughout my career and is what motivates me to tackle this project. I want to explore how, through data analysis, we can obtain accurate demand predictions and, consequently, determine optimal inventory levels. With a robust ERP like SAP Business One, companies already have access to a rich source of data, but implementing the system is only the first step. It's crucial to take an additional step: analyzing that data to transform information into real value for the company's operations.

My goal with this project is to finally answer the question I've heard countless times: "How do I calculate the demand and stock levels for my company?" I hope that the results of this analysis not only provide a clear and practical answer but also become a valuable tool for many small and medium-sized enterprises (SMEs), helping them optimize their operations and reduce costs.


<h2 id="opportunity"> The opportunity </h2>
Technological advancements have revolutionized the way companies access, analyze, and apply data. Today, data analysis and the implementation of machine learning models not only enable more informed decision-making but also provide a crucial competitive advantage.

In today’s business environment, where data is stored across multiple systems like ERP, WMS, and CRM, its analysis is not just desirable but essential for successful management. This is where a significant opportunity arises: leveraging the vast amount of data stored in business systems to apply models that provide a deeper understanding of the market and greater capacity to meet its demands.

By thoroughly analyzing business data and applying machine learning models, companies can improve demand forecasting, identify hidden sales patterns, and optimize their operations. This not only leads to more efficient inventory management, ensuring product availability when needed, but also contributes to the reduction of operational costs by minimizing excess stock and preventing stockouts. In summary, integrating advanced analytics and machine learning into business management opens the door to greater efficiency, agility, and profitability.
<p align="right">(<a href="#readme-top">back to top</a>)</p>
<h2 id="keytakeaway"> Key takeaways </h2>
Data Analysis: Analysis of supply and demand, best-selling products, inventory turnover, among others.

Demand Modeling: Predicting product demand to better plan inventory needs.

By applying inventory analysis, organizations can respond quickly to shifts in demand, enabling more agile and effective interventions.
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2 id="data"> The Data</h2>

The dataset used for this analysis was taken from Kaggle. It consists of six CSV files containing detailed information on inventory, purchases, and sales throughout an entire year of operation.

https://www.kaggle.com/datasets/bhanupratapbiswas/inventory-analysis-case-study/data

Details of each dataset:

**<li>BegInvFINAL12312016:** Initial Inventory as of 2016-01-01</li>
**<li>EndInvFINAL12312016:** Final Inventory as of 2016-12-31</li>
**<li>PurchasesFINAL12312016:** Detailed Purchase Information</li>
**<li>InvoicePurchases12312016:** Purchase Information Document Total and Freight Amount</li>
**<li>SalesFINAL12312016:** Detailed Sales Information</li>
**<li>2017PurchasePricesDec:** Summary of Purchase and Sale Price by Brand</li>


<h2 id="dict"> Data Dictionary</h2>

Write here .....
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2 id="roadmap"> Project Roadmap </h2>
<div style="display: flex; align-items: center;">

  <div style="margin-right: 20px;">
    <h2>1. Data Collection</h2>
    <ul>
      <li><strong>Task:</strong> Gather company data with related to inventory, purchase and sales information.</li>
    </ul>
  </div>
  
  <div style="margin-right: 20px;">
    <h2>2. Data Cleaning</h2>
    <ul>
      <li><strong>Task:</strong> Handle missing data, remove irrelevant or noisy data.</li>
      <li><strong>Objective:</strong> Ensure the dataset is clean, consistent, and ready for analysis.</li>
    </ul>
  </div>

  <div style="margin-right: 20px;">
    <h2>3. Exploratory Data Analysis (EDA)</h2>
    <ul>
      <li><strong>Task:</strong> Explore the cleaned dataset to understand purchase and sales information, correlation between variables and identify patterns or trends.</li>
      <li><strong>Objective:</strong> Gain insights that will guide feature engineering and model development, and formulate hypotheses for further analysis.</li>
    </ul>
  </div>

</div>

<div style="display: flex; align-items: center;">

  <div style="margin-right: 20px;">
    <h2>4. Data Splitting/Model Selection</h2>
    <ul>
      <li><strong>Task:</strong> Split the dataset into training, validation, and test sets. Select appropriate machine learning models, such as Linear or Logistic Regression, Time series.</li>
    </ul>
  </div>
  
  <div style="margin-right: 20px;">
    <h2>5. Model Evaluation</h2>
    <ul>
      <li><strong>Task:</strong> Assess the performance of the trained models using validation data. Evaluate models based on accuracy, precision, recall, and F1-score.</li>
      <li><strong>Objective:</strong> Identify the most effective model and understand its strengths and limitations, making adjustments as necessary.</li>
    </ul>
  </div>
  
  <div style="margin-right: 20px;">
    <h2>6. Model Deployment</h2>
    <ul>
      <li><strong>Task:</strong> Deploy the final model to make predictions on unseen test data.</li>
      <li><strong>Objective:</strong> Provide actionable insights to stakeholders and continue monitoring model performance in real-world scenarios, making updates as needed.</li>
    </ul>
  </div>

</div>
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2 id="progression"> Project Progression </h2>

Write here .....
<p align="right">(<a href="#readme-top">back to top</a>)</p>


<h2 id="repo"> Repository </h2>

* `data` 
    - contains link to copy of the dataset (stored in a publicly accessible cloud storage)
    - saved copy of aggregated / processed data as long as those are not too large (> 10 MB)

* `model`
    - `joblib` dump of final model(s)

* `notebooks`
    - contains all final notebooks involved in the project

* `docs`
    - contains final report, presentations which summarize the project

* `references`
    - contains papers / tutorials used in the project

* `src`
    - Contains the project source code (refactored from the notebooks)

* `.gitignore`
    - Part of Git, includes files and folders to be ignored by Git version control

* `conda.yml`
    - Conda environment specification

* `README.md`
    - Project landing page (this page)

* `LICENSE`
    - Project license
<p align="right">(<a href="#readme-top">back to top</a>)</p>
<h2 id="learnings"> Learnings </h2>

Write here ...

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2 id="conclusions"> Conclusions </h2>

Write here...
<p align="right">(<a href="#readme-top">back to top</a>)</p>
<h2 id="next"> Next Steps </h2>

Write here ...
<p align="right">(<a href="#readme-top">back to top</a>)</p>
