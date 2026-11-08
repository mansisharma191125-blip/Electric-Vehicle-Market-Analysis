# ⚡ Electric Vehicle Market Analysis \| Power BI Dashboard

An interactive **Power BI dashboard** exploring the electric vehicle
(EV) population in the United States. The project examines EV adoption
patterns, geographic distribution, manufacturers, vehicle models,
electric range, and CAFV eligibility.

## 📌 Project Overview

The objective is to turn vehicle-level data into useful insights about
the U.S. EV population and answer questions such as:

1.  How many electric vehicles are represented in the dataset?
2.  Which states have the highest EV counts?
3.  Which manufacturers and models are most represented?
4.  How are vehicles distributed across model years?
5.  What is the split between Battery Electric Vehicles (BEVs) and
    Plug-in Hybrid Electric Vehicles (PHEVs)?
6.  What does the dataset show about CAFV eligibility?
7.  What is the average electric range in the dataset?

## 📊 Dashboard Highlights

The values below are taken from the dashboard screenshot and represent
that report snapshot. They may change when the dataset is refreshed.

  KPI                        Dashboard Snapshot
  ------------------------ --------------------
  Total Vehicles                    **150.38K**
  Average Electric Range        **67.83 miles**
  BEVs                           **117K (78%)**
  PHEVs                           **34K (22%)**

### Visual Analysis

-   **State-wise distribution:** U.S. map showing the geographic spread
    of EVs.
-   **Model-year trend:** Line chart showing vehicle counts by model
    year.
-   **Top manufacturers:** Ranked comparison of the leading vehicle
    makes.
-   **CAFV eligibility:** Breakdown of eligibility categories.
-   **Top models:** Treemap comparing the most represented vehicle
    models.
-   **Vehicle type mix:** Donut charts showing BEV and PHEV counts and
    shares.
-   **Interactive filters:** City, Electric Utility, and Electric
    Vehicle Type.

## 🖼️ Dashboard Preview

![Electric Vehicle Market Analysis
Dashboard](assets/PowerBI_Dashboard.png)

> Upload your dashboard screenshot to the repository at
> `assets/PowerBI_Dashboard.png` for this preview to display. Create an
> `assets` folder if needed.

## 📂 Dataset

**Source:** [Electric Vehicle Population --
Kaggle](https://www.kaggle.com/datasets/willianoliveiragibin/electric-vehicle-population)

The dataset contains vehicle-level information about electric vehicles
registered in the United States. Fields used in the analysis include:

-   Make and Model
-   Model Year
-   State and City
-   Electric Vehicle Type
-   Electric Range
-   CAFV Eligibility
-   Electric Utility

The exact record count and KPI values may vary depending on the version
of the source dataset used.

## 🛠️ Tools & Technologies

-   **Microsoft Power BI Desktop** -- Dashboard development and
    visualization
-   **Power Query** -- Data cleaning and transformation
-   **DAX** -- Measures and KPI calculations
-   **Kaggle** -- Dataset source

## ⚙️ Data Preparation & Analysis

Project workflow:

1.  Import the EV population dataset into Power BI.
2.  Review columns, data types, and data quality.
3.  Clean and transform the data using Power Query.
4.  Create measures for vehicle counts, average electric range, and
    vehicle-type distribution.
5.  Build visuals for geography, model-year trends, manufacturers,
    models, and CAFV eligibility.
6.  Add slicers to make the report interactive.

### Example DAX Measures

These are example measures for recreating the headline KPIs. Adjust
table and column names to match your Power BI model.

**Total Vehicles**

``` dax
Total Vehicles =
COUNTROWS('Electric Vehicle Data')
```

**Average Electric Range**

``` dax
Average Electric Range =
AVERAGE('Electric Vehicle Data'[Electric Range])
```

**BEV Vehicles**

``` dax
BEV Vehicles =
CALCULATE(
    [Total Vehicles],
    'Electric Vehicle Data'[Electric Vehicle Type] = "Battery Electric Vehicle (BEV)"
)
```

**PHEV Vehicles**

``` dax
PHEV Vehicles =
CALCULATE(
    [Total Vehicles],
    'Electric Vehicle Data'[Electric Vehicle Type] = "Plug-in Hybrid Electric Vehicle (PHEV)"
)
```

**BEV Percentage**

``` dax
BEV Percentage =
DIVIDE([BEV Vehicles], [Total Vehicles], 0)
```

Format the percentage measure as **Percentage** in Power BI.

## 🚀 How to Run

1.  Download or clone this repository.
2.  Open the `.pbix` file in [Microsoft Power BI
    Desktop](https://powerbi.microsoft.com/desktop/).
3.  If prompted, update the dataset source path.
4.  Refresh the data if you want to use a newer version of the Kaggle
    dataset.
5.  Use the slicers to explore the report by city, electric utility, and
    vehicle type.

## 📁 Suggested Repository Structure

``` text
Electric-Vehicle-Market-Analysis/
├── EV_Market_Analysis.pbix
├── README.md
├── Problem_Statement.docx
├── assets/
│   └── PowerBI_Dashboard.png
└── data/
    └── README.md
```

The dataset can be downloaded from Kaggle using the source link above.
If you do not commit the CSV to GitHub, keep it locally and update the
file path in Power BI when refreshing.

## 💡 Skills Demonstrated

-   Data preparation and transformation using Power Query
-   KPI creation and DAX measures
-   Interactive dashboard design in Power BI
-   Data visualization and storytelling
-   Geographic and time-based analysis
-   Translating business questions into analytical visuals

## 📝 Notes & Limitations

-   This project analyzes a dataset; it is **not** a live EV
    registration feed or real-time vehicle tracking system.
-   The dashboard figures represent the data available in the report
    snapshot.
-   Average electric range is calculated from the source dataset's
    `Electric Range` field. It should not be interpreted as the
    real-world range of every vehicle.
-   CAFV eligibility is shown as recorded in the source dataset; the
    dashboard does not independently determine incentive eligibility.
-   Results may change when a newer dataset is loaded.

## 👩‍💻 Author

**Mansi Sharma**

-   GitHub:
    [mansisharma191125-blip](https://github.com/mansisharma191125-blip)

------------------------------------------------------------------------

If you find this project useful, feel free to ⭐ the repository.
Feedback and suggestions are welcome!
