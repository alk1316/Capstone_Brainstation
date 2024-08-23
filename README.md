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


**Dataset:** BegInvFINAL12312016
<table>
  <thead>
    <tr>
      <th>Column Name</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>InventoryId</strong></td>
      <td>Unique identifier for each item in the inventory. This field distinguishes between different products or variants of the same product.</td>
    </tr>
    <tr>
      <td><strong>Store</strong></td>
      <td>Code of the store where the inventory is located. This field is useful for identifying the physical location of the items in stock.</td>
    </tr>
    <tr>
      <td><strong>City</strong></td>
      <td>City where the corresponding store or warehouse is located. This field allows for geographic analysis and evaluation of how inventory varies by location.</td>
    </tr>
    <tr>
      <td><strong>Brand</strong></td>
      <td>Brand of the product. This field helps segment the inventory by brand, which can be important for sales analysis, customer preferences, and supplier relationship management.</td>
    </tr>
    <tr>
      <td><strong>Description</strong></td>
      <td>Detailed description of the product. This field provides additional information about the item, such as features and specifications, which can be useful for better understanding the inventory.</td>
    </tr>
    <tr>
      <td><strong>Size</strong></td>
      <td>Size or dimensions of the product. This field may refer to the physical size of the item or its capacity, which is relevant for storage space management and customer preferences.</td>
    </tr>
    <tr>
      <td><strong>onHand</strong></td>
      <td>Quantity of units available in the inventory. This field is crucial for tracking stock levels and planning replenishment.</td>
    </tr>
    <tr>
      <td><strong>Price</strong></td>
      <td>Unit price of the product. This field is fundamental for financial analysis and for assessing the value of the inventory.</td>
    </tr>
    <tr>
      <td><strong>startDate</strong></td>
      <td>The start date of inventory or Initian Inventory for 2016.</td>
    </tr>
  </tbody>
</table>


**Dataset:** EndInvFINAL12312016
<table>
  <thead>
    <tr>
      <th>Column Name</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>InventoryId</strong></td>
      <td>Unique identifier for each item in the inventory. This field distinguishes between different products or variants of the same product.</td>
    </tr>
    <tr>
      <td><strong>Store</strong></td>
      <td>Code of the store where the inventory is located. This field is useful for identifying the physical location of the items in stock.</td>
    </tr>
    <tr>
      <td><strong>City</strong></td>
      <td>City where the corresponding store or warehouse is located. This field allows for geographic analysis and evaluation of how inventory varies by location.</td>
    </tr>
    <tr>
      <td><strong>Brand</strong></td>
      <td>Brand of the product. This field helps segment the inventory by brand, which can be important for sales analysis, customer preferences, and supplier relationship management.</td>
    </tr>
    <tr>
      <td><strong>Description</strong></td>
      <td>Detailed description of the product. This field provides additional information about the item, such as features and specifications, which can be useful for better understanding the inventory.</td>
    </tr>
    <tr>
      <td><strong>Size</strong></td>
      <td>Size or dimensions of the product. This field may refer to the physical size of the item or its capacity, which is relevant for storage space management and customer preferences.</td>
    </tr>
    <tr>
      <td><strong>onHand</strong></td>
      <td>Quantity of units available in the inventory. This field is crucial for tracking stock levels and planning replenishment.</td>
    </tr>
    <tr>
      <td><strong>Price</strong></td>
      <td>Unit price of the product. This field is fundamental for financial analysis and for assessing the value of the inventory.</td>
    </tr>
    <tr>
      <td><strong>endDate</strong></td>
      <td>The end date of inventory or Final Inventory for 2016.</td>
    </tr>
  </tbody>
</table>



**Dataset:** PurchasesFINAL12312016
<table>
  <thead>
    <tr>
      <th>Column Name</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>InventoryId</strong></td>
      <td>Unique identifier for each item in the inventory. This field distinguishes between different products or variants of the same product.</td>
    </tr>
    <tr>
      <td><strong>Store</strong></td>
      <td>Code of the store where the purchase was made or where the inventory is located. This field helps identify the physical location associated with the purchase.</td>
    </tr>
    <tr>
      <td><strong>Brand</strong></td>
      <td>Brand of the product. This field helps segment the purchase data by brand, which can be important for supplier management and brand analysis.</td>
    </tr>
    <tr>
      <td><strong>Description</strong></td>
      <td>Detailed description of the product. This field provides additional information about the item, such as features and specifications, which can be useful for understanding the nature of the purchase.</td>
    </tr>
    <tr>
      <td><strong>Size</strong></td>
      <td>Size or dimensions of the product. This field may refer to the physical size of the item or its capacity, which is relevant for storage and inventory management.</td>
    </tr>
    <tr>
      <td><strong>VendorNumber</strong></td>
      <td>Unique identifier for the vendor or supplier. This field is used to track purchases by vendor.</td>
    </tr>
    <tr>
      <td><strong>VendorName</strong></td>
      <td>Name of the vendor or supplier. This field helps identify the supplier associated with each purchase.</td>
    </tr>
    <tr>
      <td><strong>PONumber</strong></td>
      <td>Purchase Order (PO) number associated with the purchase. This field is used to track and manage orders with suppliers.</td>
    </tr>
    <tr>
      <td><strong>PODate</strong></td>
      <td>Date when the Purchase Order was issued. This field is crucial for understanding the timing of orders and for inventory planning.</td>
    </tr>
    <tr>
      <td><strong>ReceivingDate</strong></td>
      <td>Date when the goods were received. This field helps track the lead time and manage inventory levels.</td>
    </tr>
    <tr>
      <td><strong>InvoiceDate</strong></td>
      <td>Date when the invoice was issued by the vendor. This field is used for financial tracking and payment processing.</td>
    </tr>
    <tr>
      <td><strong>PayDate</strong></td>
      <td>Date when the payment was made to the vendor. This field helps manage cash flow and supplier relationships.</td>
    </tr>
    <tr>
      <td><strong>PurchasePrice</strong></td>
      <td>Price paid for each unit of the product. This field is essential for cost analysis and financial planning.</td>
    </tr>
    <tr>
      <td><strong>Quantity</strong></td>
      <td>Number of units purchased. This field helps track the volume of purchases and manage inventory levels.</td>
    </tr>
    <tr>
      <td><strong>Dollars</strong></td>
      <td>Total cost of the purchase in dollars. This field is crucial for budgeting and financial reporting.</td>
    </tr>
    <tr>
      <td><strong>Classification</strong></td>
      <td>Category used to classify purchases</td>
    </tr>
  </tbody>
</table>


**Dataset:** InvoicePurchases12312016

<table>
  <thead>
    <tr>
      <th>Column Name</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>VendorNumber</strong></td>
      <td>Unique identifier for the vendor or supplier. This field is used to track purchases by vendor.</td>
    </tr>
    <tr>
      <td><strong>VendorName</strong></td>
      <td>Name of the vendor or supplier. This field helps identify the supplier associated with each purchase.</td>
    </tr>
    <tr>
      <td><strong>InvoiceDate</strong></td>
      <td>Date when the invoice was issued by the vendor. This field is used for financial tracking and payment processing.</td>
    </tr>
    <tr>
      <td><strong>PONumber</strong></td>
      <td>Purchase Order (PO) number associated with the purchase. This field is used to track and manage orders with suppliers.</td>
    </tr>
    <tr>
      <td><strong>PODate</strong></td>
      <td>Date when the Purchase Order was issued. This field is crucial for understanding the timing of orders and for inventory planning.</td>
    </tr>
    <tr>
      <td><strong>PayDate</strong></td>
      <td>Date when the payment was made to the vendor. This field helps manage cash flow and supplier relationships.</td>
    </tr>
    <tr>
      <td><strong>Quantity</strong></td>
      <td>Number of units purchased. This field helps track the volume of purchases and manage inventory levels.</td>
    </tr>
    <tr>
      <td><strong>Dollars</strong></td>
      <td>Total cost of the purchase in dollars. This field is crucial for budgeting and financial reporting.</td>
    </tr>
    <tr>
      <td><strong>Freight</strong></td>
      <td>Cost associated with the transportation of goods. This field is important for calculating the total cost of goods purchased and for financial planning.</td>
    </tr>
    <tr>
      <td><strong>Approval</strong></td>
      <td>Indicates whether the purchase has been approved.</td>
    </tr>
  </tbody>
</table>


**Dataset:** SalesFINAL12312016

<table>
  <thead>
    <tr>
      <th>Column Name</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>InventoryId</strong></td>
      <td>Unique identifier for each item in the inventory. This field distinguishes between different products or variants of the same product.</td>
    </tr>
    <tr>
      <td><strong>Store</strong></td>
      <td>Code of the store where the sale took place. This field helps identify the physical location associated with the sale.</td>
    </tr>
    <tr>
      <td><strong>Brand</strong></td>
      <td>Brand of the product. This field helps segment the sales data by brand, which can be important for market analysis and supplier management.</td>
    </tr>
    <tr>
      <td><strong>Description</strong></td>
      <td>Detailed description of the product. This field provides additional information about the item sold, such as features and specifications.</td>
    </tr>
    <tr>
      <td><strong>Size</strong></td>
      <td>Size or dimensions of the product. This field may refer to the physical size of the item or its capacity, which is relevant for inventory and sales analysis.</td>
    </tr>
    <tr>
      <td><strong>SalesQuantity</strong></td>
      <td>Number of units sold. This field is crucial for tracking the volume of sales and analyzing product performance.</td>
    </tr>
    <tr>
      <td><strong>SalesDollars</strong></td>
      <td>Total revenue generated from the sale in dollars. This field is important for financial analysis and performance tracking.</td>
    </tr>
    <tr>
      <td><strong>SalesPrice</strong></td>
      <td>Price at which each unit was sold. This field helps in understanding pricing strategies and profitability.</td>
    </tr>
    <tr>
      <td><strong>SalesDate</strong></td>
      <td>Date when the sale occurred. This field is essential for time-series analysis and understanding sales trends.</td>
    </tr>
    <tr>
      <td><strong>Volume</strong></td>
      <td>Total volume of the product sold, which could be measured in units such as liters or kilograms, depending on the product type.</td>
    </tr>
    <tr>
      <td><strong>Classification</strong></td>
      <td>Category or type of product, used to classify sales for analysis and reporting purposes.</td>
    </tr>
    <tr>
      <td><strong>ExciseTax</strong></td>
      <td>Tax levied on the sale of specific goods. This field is used for financial reporting and compliance.</td>
    </tr>
    <tr>
      <td><strong>VendorNo</strong></td>
      <td>Unique identifier for the vendor or supplier associated with the product. This field helps track sales by vendor.</td>
    </tr>
    <tr>
      <td><strong>VendorName</strong></td>
      <td>Name of the vendor or supplier associated with the product. This field helps in supplier management and relationship tracking.</td>
    </tr>
  </tbody>
</table>


**Dataset:** 2017PurchasePricesDec

<table>
  <thead>
    <tr>
      <th>Column Name</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Brand</strong></td>
      <td>Brand of the product. This field helps segment the purchase data by brand, which can be important for supplier management and market analysis.</td>
    </tr>
    <tr>
      <td><strong>Description</strong></td>
      <td>Detailed description of the product. This field provides additional information about the item purchased, such as features and specifications.</td>
    </tr>
    <tr>
      <td><strong>Price</strong></td>
      <td>Sales price of the product at the time of purchase. This field is important for pricing analysis and cost management.</td>
    </tr>
    <tr>
      <td><strong>Size</strong></td>
      <td>Size or dimensions of the product. This field may refer to the physical size of the item or its capacity, relevant for storage and inventory management.</td>
    </tr>
    <tr>
      <td><strong>Volume</strong></td>
      <td>Total volume of the product, which could be measured in units such as liters or kilograms, depending on the product type.</td>
    </tr>
    <tr>
      <td><strong>Classification</strong></td>
      <td>Category or type of product, used to classify purchases for analysis and reporting purposes.</td>
    </tr>
    <tr>
      <td><strong>PurchasePrice</strong></td>
      <td>Price paid for each unit of the product. This field is crucial for cost analysis and financial planning.</td>
    </tr>
    <tr>
      <td><strong>VendorNumber</strong></td>
      <td>Unique identifier for the vendor or supplier. This field is used to track purchases by vendor.</td>
    </tr>
    <tr>
      <td><strong>VendorName</strong></td>
      <td>Name of the vendor or supplier. This field helps identify the supplier associated with each purchase.</td>
    </tr>
  </tbody>
</table>












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
