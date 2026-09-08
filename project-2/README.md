# EXPLORATORY DATA ANALYSIS

# Businness Understanding
### Problem Statement

The dataset contained transaction-level records with multiple numerical variables related to customer purchases. The analysis needed to determine how transaction values were distributed, identify unusual observations, and understand the relationships between purchasing variables while distinguishing genuine purchasing patterns from potential data-quality issues.

### Project Objective

The objective was to conduct an exploratory analysis of the transaction data to:

* Understand the distribution and variability of key numerical variables.
* Identify trends, patterns, and potential outliers.
* Examine relationships between purchasing variables and transaction value.
* Assess the consistency between recorded and calculated transaction totals.
* Translate the findings into actionable business insights and recommendations.

# Methodology
The analysis followed a structured Exploratory Data Analysis (EDA) process using the following methods:

**Data Understanding:** Reviewed the dataset structure, dimensions, data types, and numerical variables to establish the scope of the analysis.

**Descriptive Statistics:** Calculated count, mean, median, standard deviation, minimum, maximum, and quartiles to understand the central tendency and variability of each numerical variable.

**Distribution Analysis:** Used histograms and boxplots to examine the distribution of numerical variables, identify skewness, and observe the spread of transaction values.

**Outlier Analysis:** Applied the Interquartile Range (IQR) method to identify observations that fell outside the expected range and assessed whether they represented genuine purchasing behavior or potential data-quality issues.

**Correlation Analysis:** Calculated Pearson correlation coefficients and visualized the correlation matrix to identify the strength and direction of relationships between numerical variables.

**Key Findings:** Synthesized the statistical results into key business insights, distinguishing meaningful purchasing patterns from potential data-quality artifacts.

**Recommendations:** Translated the findings into practical recommendations for interpreting transaction values, investigating high-value purchases, and maintaining transaction validation controls.

# Descriptive Statistics

<img width="828" height="206" alt="image" src="https://github.com/user-attachments/assets/6aeda8d2-4164-45ab-ae36-43895c66db7d" />

**Insight:**
TotalPrice had the greatest variability, with a mean of 1,053.97 compared with a median of 823.62, indicating that higher-value transactions influenced the average. Other variables were more closely centered around their typical values, providing a clearer view of normal purchasing behavior.


# Distribution Analysis

<img width="761" height="421" alt="image" src="https://github.com/user-attachments/assets/9ddd172d-f5d4-4aec-b379-cfea5c13a9fd" />

**Insight:**
Purchases were concentrated around 2–4 units, indicating that most transactions involved relatively small quantities. Inventory and purchasing strategies could prioritize typical purchase volumes while still accounting for higher-quantity transactions.

<img width="762" height="421" alt="image" src="https://github.com/user-attachments/assets/70389e7a-a0ab-416b-95b9-a462ec569b54" />

**Insight:**
Prices distributed broadly across the available range, indicating variation in the prices of products purchased. This suggested that transaction value was influenced by a range of pricing levels, making pricing an important area to examine when understanding customer spending.

<img width="763" height="419" alt="image" src="https://github.com/user-attachments/assets/0e12ba4c-1986-4a13-a043-430eb43c8596" />

**Insight:**
Most transactions contained around 4–7 items, with fewer transactions at the lower and upper ends. This provided a useful indication of typical basket size and supported opportunities to examine what factors were associated with larger carts.

<img width="761" height="421" alt="image" src="https://github.com/user-attachments/assets/759ace61-8b91-4065-9573-528219b121d4" />

**Insight:**
Transactions concentrated at lower values and fewer transactions extending toward much higher values. The average transaction value could be influenced substantially by a smaller number of high-value purchases, so relying on the mean alone could give a misleading picture of typical customer spending.

<img width="761" height="418" alt="image" src="https://github.com/user-attachments/assets/4f8446b5-5e2c-450f-86a1-d3519b59d48d" />

**Insight:**
The histogram followed the same distribution as TotalPrice. This reinforced confidence that the calculated transaction values were consistent with the recorded values.

<img width="771" height="420" alt="image" src="https://github.com/user-attachments/assets/34c056cb-2d8b-44e8-a888-c1d63c113249" />

**Insight:**
Values concentrated effectively at zero. Business impact: This indicated that recorded transaction totals were internally consistent, reducing concerns about calculation discrepancies affecting the analysis.

# Outlier Analysis

<img width="573" height="419" alt="image" src="https://github.com/user-attachments/assets/3c1d6bf8-44f1-4c09-93a7-4578e3e28fea" />
<img width="576" height="419" alt="image" src="https://github.com/user-attachments/assets/fa3d642f-b7f9-462c-8dbf-34bf96a8530f" />
<img width="575" height="421" alt="image" src="https://github.com/user-attachments/assets/32189eb6-b938-4292-b364-cde419cfc4a2" />
<img width="576" height="422" alt="image" src="https://github.com/user-attachments/assets/b9269b0c-e9a8-457f-9f4a-a7598096dead" />
<img width="578" height="421" alt="image" src="https://github.com/user-attachments/assets/78bf3816-4562-423f-8db2-c4995e7b0f70" />
<img width="578" height="421" alt="image" src="https://github.com/user-attachments/assets/4d9593df-072f-48da-a167-e1ab5a74e6e1" />

**Insight:**
The boxplots showed that TotalPrice had the most significant extreme observations, with 27.9% flagged by the IQR method, highlighting substantial variation in transaction values. The high proportion of ItemsInCart (44.4%) and Quantity (18.1%) flags largely represented higher-volume purchasing behavior rather than clear errors.

# Correlation Analysis

<img width="759" height="488" alt="image" src="https://github.com/user-attachments/assets/a90b0a03-86b2-4a6d-9324-346fa62f7abc" />

**Insight:**
UnitPrice (r = 0.72) and Quantity (r = 0.62) showed the strongest relationships with TotalPrice, indicating that pricing and purchase volume were strongly associated with transaction value. However, correlation does not imply causation; the analysis identified relationships between variables but did not establish that changes in UnitPrice or Quantity directly caused changes in TotalPrice.

# Key Findings
**1. Transaction values showed substantial variation**

TotalPrice recorded a mean of 1,053.97 compared with a median of 823.62, while the standard deviation was 819.86 and the maximum transaction value reached 3,456.40. This indicates that higher-value transactions had a considerable influence on the overall average.

**2. UnitPrice demonstrated the strongest numerical relationship with transaction value**

UnitPrice had a strong positive correlation with TotalPrice (r = 0.72), followed by Quantity (r = 0.62). This indicates that differences in unit pricing and purchase volume were closely associated with variations in transaction value.

**3. Purchase volume and cart size were strongly associated**

The average Quantity was 2.95 units, compared with a median of 3, while ItemsInCart had a mean of 5.49 and a median of 5. The two variables also showed a positive correlation (r = 0.65), indicating that larger carts were generally associated with higher purchase quantities.

**4. A substantial number of TotalPrice observations were identified as potential outliers**

The IQR analysis flagged 335 observations (27.9%), reflecting the considerable spread in transaction values. These observations warranted further investigation to determine whether they represented legitimate high-value purchases or distinct purchasing patterns.

**5. The IQR method flagged a high proportion of larger cart sizes as potential outliers**

533 ItemsInCart observations (44.4%) were classified as outliers. However, because ItemsInCart was a discrete variable ranging from 1 to 10, these observations were more appropriately interpreted as larger cart sizes rather than automatically being considered data-quality errors.

**6. Recorded and calculated transaction totals were internally consistent**

TotalPrice and CalculatedTotal had identical distributions, while PriceDifference remained effectively zero across the dataset. No meaningful discrepancies were identified between the recorded and independently calculated transaction totals.

# Recommendations
**1. Use median alongside mean when reporting transaction value**

TotalPrice has a mean of 1,053.97 versus a median of 823.62, reporting both measures will give a more accurate view of typical customer spending and prevent high-value transactions from distorting performance interpretation.

**2. Investigate the drivers of high-value transactions**

With 27.9% of TotalPrice observations flagged as potential outliers and a maximum transaction value of 3,456.40, segment high-value transactions to determine whether they are driven by higher unit prices, larger quantities, or larger carts.

**3. Focus purchasing analysis on UnitPrice and Quantity**

Since UnitPrice (r = 0.72) and Quantity (r = 0.62) have the strongest relationships with the total price, future analysis should examine how pricing and purchase volume differ across customer or product segments.

**4. Analyze larger carts as a distinct purchasing segment**

44.4% of ItemsInCart are flagged by the IQR rule, but because the variable ranges from 1–10 and is discrete, these should not automatically be removed. Instead, compare customers with larger versus typical carts to understand their purchasing behavior and value.

**5. Preserve legitimate high-volume observations during future analysis**

The relationship between ItemsInCart and quantity (r = 0.65) suggests that larger carts correspond with higher purchase volumes. Outlier treatment should therefore distinguish genuine high-volume behavior from actual data-quality errors.

**6. Maintain automated transaction validation**

Since PriceDifference is effectively zero and TotalPrice matches CalculatedTotal, retain the calculation check as a data-quality control to ensure future transaction records remain internally consistent.
