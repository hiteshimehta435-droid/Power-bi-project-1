<img width="1536" height="179" alt="power bi" src="https://github.com/user-attachments/assets/e75260ae-8d2f-4e43-acc2-b304ccb2b2e6" />



# Power BI Project: Bar Charts and KPI Cards

## 📌 Project Overview

This project demonstrates how to create **Bar Charts** and **KPI Cards** using Microsoft Power BI Desktop. These visuals help users understand data, compare values, and display important business information in a simple dashboard.

## 🎯 Project Objectives

- Create a Bar Chart to compare categories.
- Create KPI Cards to display important numerical values.
- Customize visuals for a professional dashboard.
- Learn basic data visualization in Power BI.

## 🛠️ Tools Used

- Microsoft Power BI Desktop
- Sample Sales Dataset (Excel or CSV)

---

## 📊 1. How to Create a Bar Chart in Power BI
<img width="983" height="505" alt="image" src="https://github.com/user-attachments/assets/1b722bd2-4a7c-4259-ba15-61d1e8b040ec" />



A Bar Chart is used to compare values across different categories, such as product sales, regional sales, or customer counts.

### Step 1: Import the Dataset

1. Open Power BI Desktop.
2. Click **Home → Get Data**.
3. Select Excel Workbook or Text/CSV.
4. Choose your dataset.
5. Click **Load**.

### Step 2: Insert a Bar Chart

1. Open the **Report** view.
2. Select the **Clustered Bar Chart** visual from the Visualizations pane.
3. A blank chart will appear on the report canvas.

### Step 3: Add Data Fields

For example, use a sales dataset containing `Product`, `Category`, and `Sales`.

- **Y-axis:** Product or Category
- **X-axis:** Sales

Drag the appropriate fields into the chart's field wells. In newer Power BI versions, the field wells may be labeled **Y-axis** and **X-axis**, or **Category** and **Values**.

### Step 4: Customize the Chart

1. Select the chart.
2. Open the **Format visual** pane.
3. Turn on the chart title and enter *Sales by Product*.
4. Customize bar colors.
5. Enable data labels to display sales values.
6. Adjust axis titles and text sizes.

### Expected Result

The Bar Chart displays sales values for each product, making it easy to identify which products have higher or lower sales.

---

## 🎯 2. How to Create KPI Cards in Power BI
<img width="1002" height="505" alt="image" src="https://github.com/user-attachments/assets/6dfe4036-f91f-4deb-8f3a-cdc184217df5" />



KPI Cards display important business metrics, such as Total Sales, Total Profit, and Total Orders.

### Step 1: Create a Total Sales Measure

1. Select your sales table in the Data or Model pane.
2. Click **Modeling → New measure**.
3. Enter the following DAX formula:

```DAX
Total Sales = SUM(Sales[Sales])
```

Replace `Sales` with your actual table name and column name if they are different.

### Step 2: Create a Total Profit Measure

Click **Modeling → New measure** and enter:

```DAX
Total Profit = SUM(Sales[Profit])
```

Make sure the dataset contains a numeric `Profit` column.

### Step 3: Create a Total Orders Measure

If each row represents one order, use:

```DAX
Total Orders = COUNTROWS(Sales)
```

If one order can contain multiple rows, use a distinct order count instead:

```DAX
Total Orders = DISTINCTCOUNT(Sales[Order ID])
```

Replace `Order ID` with your actual order identifier column.

### Step 4: Insert a Card Visual

1. Select an empty area on the report canvas.
2. Choose the **Card** visual from the Visualizations pane.
3. Drag the `Total Sales` measure into the card's data field.
4. Repeat the process for `Total Profit` and `Total Orders`.

Create three separate cards to display the three metrics.

### Step 5: Format the KPI Cards

1. Select a card.
2. Open **Format visual**.
3. Set the title to *Total Sales*, *Total Profit*, or *Total Orders*.
4. Adjust the callout value size.
5. Set currency formatting for sales and profit if appropriate.
6. Customize the background, text, and borders.
7. Align the cards neatly at the top of the dashboard.

### Expected Result

The report displays three KPI Cards showing:

- **Total Sales:** Sum of sales values.
- **Total Profit:** Sum of profit values.
- **Total Orders:** Number of orders or order records, depending on the measure.

---

## 🖥️ 3. Final Dashboard Layout

Arrange the visuals like this:

| Dashboard Section | Visual |
|---|---|
| Top Left | Total Sales Card |
| Top Center | Total Profit Card |
| Top Right | Total Orders Card |
| Bottom Section | Sales by Product Bar Chart |

This layout makes the main business metrics easy to understand at a glance.

## 📈 Project Outcomes

After completing this project, you will be able to:

- Import a dataset into Power BI.
- Create and format Bar Charts.
- Write basic DAX measures.
- Create KPI Cards for business metrics.
- Arrange visuals into a simple dashboard.

## 🚀 How to Run the Project

1. Install Microsoft Power BI Desktop.
2. Download or prepare a sales dataset in Excel or CSV format.
3. Import the dataset into Power BI.
4. Follow the steps in this README.
5. Save the report as a `.pbix` file.
6. Upload the README, dataset (if permitted), and report screenshots to GitHub.

## 👨‍💻 Author

**Power BI Beginner Project**

*Learning data visualization through practical examples.*

---

⭐ If you find this project helpful, consider giving the repository a star!
