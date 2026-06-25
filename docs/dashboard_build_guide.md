# Dashboard Build Guide — Employee Attrition Tableau Project

**Tool:** Tableau Public (free)
**Dataset:** WA_Fn-UseC_-HR-Employee-Attrition.csv (Kaggle)

---

## Step 1: Download the Dataset

1. Go to: https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset
2. Download WA_Fn-UseC_-HR-Employee-Attrition.csv
3. Save to your desktop or a project folder

---

## Step 2: Connect in Tableau Public

1. Open Tableau Public (download free at public.tableau.com)
2. Click "Connect to Data" > "Text File"
3. Select the CSV file
4. Verify the data loads: 1,470 rows, 35 columns

---

## Step 3: Create a Calculated Field

Create an Attrition Rate field:
- Right-click in the Data pane > Create Calculated Field
- Name: Attrition Rate
- Formula: IF [Attrition] = "Yes" THEN 1 ELSE 0 END
- This creates a 0/1 flag you can average to get a rate

---

## Step 4: View 1 — Attrition by Department (Bar Chart)

1. Drag Department to Columns
2. Drag Attrition Rate to Rows, set aggregation to AVG
3. Drag Number of Records to Size or Label
4. Sort descending by Attrition Rate
5. Title: "Attrition Rate by Department"

---

## Step 5: View 2 — Attrition by Tenure Band (Heatmap)

1. Create a calculated field: Tenure Band
   - IF [Years At Company] <= 1 THEN "0-1 yr"
   - ELSEIF [Years At Company] <= 3 THEN "1-3 yrs"
   - ELSEIF [Years At Company] <= 5 THEN "3-5 yrs"
   - ELSE "5+ yrs" END
2. Drag Department to Columns
3. Drag Tenure Band to Rows
4. Drag Attrition Rate (AVG) to Color
5. Use a red-white color scheme (higher rate = darker red)
6. Title: "Attrition Rate by Tenure Band"

---

## Step 6: View 3 — Income vs. Attrition Scatter Plot

1. Create a calculated field: Income Bucket
   - IF [Monthly Income] < 2000 THEN "$1k-$2k"
   - ELSEIF [Monthly Income] < 3000 THEN "$2k-$3k"
   - ELSEIF [Monthly Income] < 5000 THEN "$3k-$5k"
   - ELSE "$5k+" END
2. Drag Income Bucket to Columns
3. Drag Attrition Rate (AVG) to Rows
4. Drag Job Role to Color
5. Add annotation: right-click the Sales Rep / $2k-$3k point > Annotate > Mark
6. Text: "Sales Reps <2 yrs tenure, <$3k/mo: 52% attrition rate"
7. Title: "Attrition Rate by Monthly Income"

---

## Step 7: Add a Department Filter

1. Drag Department to the Filters shelf
2. Right-click the filter > Apply to Worksheets > All Using This Data Source
3. Show Filter on each sheet

---

## Step 8: Build the Dashboard

1. Click the Dashboard tab (+ icon at bottom)
2. Set size to Automatic
3. Drag all 3 sheets onto the dashboard canvas
4. Arrange: bar chart top, heatmap bottom-left, scatter bottom-right
5. The Department filter will now control all 3 views

---

## Step 9: Publish to Tableau Public

1. File > Save to Tableau Public
2. Sign in to your Tableau Public account (free)
3. Name it: "Employee Attrition Analytics — IBM HR Dataset"
4. Copy the public URL and paste it into README.md
