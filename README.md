# 📱🌍 Social Media Addiction Analysis

## 🌟 Project Overview
This project focuses on analyzing the impact of 📱 social media usage across 🌎 different countries and regions. The 📊 data-driven study explores trends related to 🌐 internet penetration, social media addiction prevalence, and the corresponding implications on 🧑‍🤝‍🧑 societal and human development. The project uses 🗄️ SQL as the primary tool for data analysis and integrates complementary datasets for comprehensive insights.

## 🎯 Objectives
1. 📈 Analyze social media addiction prevalence globally.
2. 🔗 Understand the relationship between 🌐 internet access and 📱 social media usage.
3. 🛡️ Explore policies and their effects, such as age restrictions on social media usage.
4. 🧠 Provide actionable insights for policymakers and researchers.

## 📂 Data Sources
The datasets used in this project include:

1. **🌐 Internet Usage Statistics**:
   - 📅 Includes year-wise data on 🌐 internet penetration rates by country.
   - 🗂️ Source: Publicly available datasets.

2. **📊 Social Media Addiction Data**:
   - 📉 Contains statistics on the percentage of populations affected by excessive social media use.
   - 📖 Source: Collected from online repositories and research publications.

3. **🌎 Country and Regional Data**:
   - 🗺️ Includes demographic, geographic, and policy details.
   - 📚 Source: World Bank and other open datasets.

## 🛠️ Tools and Technologies
- **🗄️ SQL**: Used for creating the database, querying, and analyzing the datasets.
- **📊 Excel**: For data cleaning and preprocessing before importing into SQL.
- **🐍 Python**: (Optional) For additional data manipulation and visualization.

## 🗂️ Database Structure
The project’s 🗄️ SQL database consists of the following tables:

1. **🌍 Countries**:
   - `🏷️ country_id` (Primary Key)
   - `🌎 country_name`
   - `🌐 region`

2. **📊 InternetUsage**:
   - `🏷️ usage_id` (Primary Key)
   - `🔗 country_id` (Foreign Key)
   - `📅 year`
   - `📈 internet_penetration_rate`

3. **📉 SocialMediaAddiction**:
   - `🏷️ addiction_id` (Primary Key)
   - `🔗 country_id` (Foreign Key)
   - `📅 year`
   - `📉 addiction_rate`

4. **🛡️ Policies**:
   - `🏷️ policy_id` (Primary Key)
   - `🔗 country_id` (Foreign Key)
   - `📝 policy_description`
   - `📅 year`

## 🛠️ Steps to Replicate
1. **🧹 Data Preparation**:
   - 🧽 Clean and preprocess raw datasets using 📊 Excel or 🐍 Python.
   - ✂️ Extract years from formatted columns (e.g., `2000 [YR2000]` to `2000`).

2. **🗄️ Database Creation**:
   - 🏗️ Create an SQL database and define tables based on the structure above.
   - 📤 Load cleaned data into respective tables.

3. **📊 Data Analysis**:
   - ✍️ Write SQL queries to:
     - 📈 Analyze trends over time.
     - 🌍 Compare internet penetration rates and addiction levels by region.
     - 🔗 Identify correlations between policies and addiction rates.

4. **📊 Visualization (Optional)**:
   - 🖼️ Use Python libraries like Matplotlib or Power BI for 📉 charts and graphs.

## 🔑 Key Queries
Example SQL queries include:
- **🏆 Top 10 countries by addiction rate**:
  ```sql
  SELECT 🌎 country_name, MAX(📉 addiction_rate) AS max_rate
  FROM 📉 SocialMediaAddiction
  JOIN 🌍 Countries ON 📉 SocialMediaAddiction.🔗 country_id = 🌍 Countries.🏷️ country_id
  GROUP BY 🌎 country_name
  ORDER BY max_rate DESC
  LIMIT 10;
  ```

- **🔗 Correlation between internet penetration and addiction**:
  ```sql
  SELECT 📅 year, AVG(📈 internet_penetration_rate) AS avg_internet, AVG(📉 addiction_rate) AS avg_addiction
  FROM 📊 InternetUsage
  JOIN 📉 SocialMediaAddiction USING (🔗 country_id, 📅 year)
  GROUP BY 📅 year;
  ```

## ⚠️ Challenges
1. 🔄 Ensuring data consistency across multiple datasets.
2. ❓ Handling missing or incomplete data points.
3. 🧩 Merging datasets with different granularities (e.g., 🌍 country-level vs 🌐 regional-level).

## 🔮 Future Work
1. ➕ Incorporate more datasets for a deeper understanding of the issue.
2. 🤖 Explore machine learning models to predict future trends.
3. 🌐 Publish insights in an interactive dashboard for stakeholders.

## 🤝 How to Contribute
Feel free to 🔀 fork this repository and contribute by:
- 📥 Adding new datasets.
- ✍️ Improving SQL queries or database design.
- 🎨 Creating visualizations or reports.

## 📜 License
This project is licensed under the MIT License. See the LICENSE file for more details.

