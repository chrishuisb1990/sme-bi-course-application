# Virtual Machine (VM) Exercises

## :information_source: Read this before getting started
- The two exercises should not replicate the exact actions shown in your screencast. The goal of exercises is for learners to apply what was learned in the screencasts to new problems or situations. This is best pedagogical practice for retaining and building skills. For example, this can be done by using another dataset between screencasts and exercises or focusing on a different portion of the dataset.
- We can only run free versions of BI software in our virtual machine exercises. In the case of Power BI, make sure the exercises can run on [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) without any additional paid products. 
- Unsure what the scope of an exercise should be? Here's an [example](https://campus.datacamp.com/courses/introduction-to-power-bi/getting-started-with-power-bi?ex=14) from Introduction to Power BI. The first chapter of most DataCamp courses are free, so take a look at our [BI courses](https://learn.datacamp.com/courses?technologies=Tableau&technologies=Power%20BI) to get a feel for how we assess and guide learners.

## 1st VM Exercise

#### Dataset

- [x] Add datasets used to the `datasets/` folder

#### Files

- [x] **Initial**: Add file to the `exercises/`  folder with the name `ex-1-intial.twbx` or `ex-1-intial.pbix`, depending if you are auditioning for a Tableau or Power BI course.
- [x] **Solution**: Add file to the `exercises/`  folder with the name `ex-1-sol.twbx` or `ex-1-sol.pbix`

#### Learning Objective

*Demonstrate how to utilize the PERCENTILE function to identify and remove anomalous values *

#### Context

As an Analytics Professional, timeseries data is one of the most common data types you’ll be interacting with. Standard performance reporting will have you contrast different business products against each other and occasionally, remove anomalous data points, to improve reporting accuracy for Management. In this exercise, you’ll be seeking to analyse Water Pricing Data  for two water products, Soft and Hard Water, where you’ll be using the PERCENTILE() functions you’ve learned, to remove anomalous values and provide a true reflection of the average monthly pricing for both Soft and Hard water products!  

#### Steps to be executed by the student (max 6)

*Each bulleted instruction is a complete sentence that describes a specific task.*

- Step 1
-	Open the workbook titled ex-1-intial.twbx. Note that the Columns (Month (Trading Interval) and Rows (Water Type) have been pre-populated for you. 
- Step 2
-	Drag the Water Price into the Text field in the Marks Pane. Convert this from a Summed Aggregation to an Average Aggregation. 
- Step 3
-	Click on Analysis, Totals and then check both the Show Row Grand Totals and Show Column Grand Totals. This will reflect the Year to Date Average (for each Water Type, as well as the Monthly Average. 
- Step 4
-	Create a new calculated field called Anomalous Classification that segments the top 5% of Water Pricing data as anomalous (e.g. 95th Percentile), and all other values as non-anomalous. 
- Step 5
-	Drag in the Anomalous Classification field into the Filter and exclude all Anomalous Values. 


#### Exercise question:
*Having excluded all Anomalous Values – what is the new Average Water Price for the Year-to-Date? (This includes both Hard & Soft Water Products).*

#### End goal:

![image](https://user-images.githubusercontent.com/72181097/221604470-4d241283-d8cd-4fec-88c9-4e2754c59a90.png)

## 2nd VM Exercise

#### Dataset

- [x ] Add datasets used to the `datasets/` folder

#### Files

- [x ] **Initial**: Add file to the `exercises/`  folder with the name `ex-2-intial.twbx` or `ex-2-intial.pbix`, depending if you are auditioning for a Tableau or Power BI course.
- [x ] **Solution**: Add file to the `exercises/`  folder with the name `ex-2-sol.twbx` or `ex-2-sol.pbix`

#### Learning Objective

*Upon completion of the Percentile Video, Student should be able to demonstrate how to utilize the PERCENTILE function to identify and or/remove anomalous values. *

#### Context

Previously we identified that the months of January, February and March had the highest average prices for our water products. In other words, we have peak months, which includes the first quarter of the year, and non-peak months, which makes up the rest. Now prices should be a  function of demand – so we might expect to see the majority of anomalous data points centred around the Water Product with higher pricing. However, as data professionals, we believe in testing our hypotheses, so let’s examine this below!

#### Steps to be executed by the student (max 6)

*Each bulleted instruction is a complete sentence that describes a specific task.*

- Step 1
-	Open the workbook titled ex-2-intial.twbx. Note that the Anomalous Classification Field you previously created has already been dragged into the Color Field under the Marks Pane.
- Step 2
-	Create a new calculated field called ‘Market Classification’ which classifies a month as ‘Peak’ if the month is January, February or March. Otherwise, it’s ‘Non-Peak’. 
- Step 3
-	For the Columns, drag the Water Type and Market Water Demand Fields, whereas for the rows, drag in the Peak_Classification and Water Price Fields. Ensure you uncheck Aggregate Measures for your Scatter Plot.

#### Exercise question:
•	Analyzing the Scatter Plot you’ve created, which Water Product and Market Classification, has the majority of Anomalous Values? 

#### End goal:

![image](https://user-images.githubusercontent.com/72181097/221604910-bec8dac6-2044-4925-aae6-c8baf6337e07.png)


