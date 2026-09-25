# 🏋️ Fitzone Gym Member Analytics Dashboard — Power BI

An interactive Power BI dashboard built for a gym business to track membership health, retention, and workout performance across 150 members.

---

## 🎯 Project Objective

Give gym owners and fitness business managers a single view to answer questions like:

- How many members do we have, and how much revenue are they generating?
- How many members are at risk of churning, and why?
- Which membership plans retain customers best?
- What exercises and demographics drive the most engagement?
- Who are our individual members, and what's their activity level?

---

## 🗂️ Dashboard Components

The report contains **4 pages**.

| Page | What it shows |
|------|----------------|
| **Overview** | Total members, total revenue, avg visits/month, at-risk members, churn rate, members by plan, total members by month |
| **Retention** | Churn breakdown (yes/no), churn % by membership plan, live table of at-risk members with days since last visit |
| **Performance** | Avg calories burned by exercise, avg visits/month by age group, workout duration vs. weight lifted (by gender) |
| **Members** | Full searchable/sortable member directory with age, gender, membership type, visit frequency, and churn status |

---

## 🎛️ Interactivity

- **Filters:** At Risk Flag, Churn, Gender, Membership Type
- Every visual across all pages responds to the selected filters

---

## 🧮 Calculated Fields (DAX Measures)

| Measure | Definition |
|---------|------------|
| **Churn Rate %** | `DIVIDE(CALCULATE(COUNTROWS(Members), Churn = "Yes"), COUNTROWS(Members))` |
| **At Risk Members** | `CALCULATE(COUNTROWS(Members), AtRiskFlag = "Yes")` |
| **Avg Visits/Month** | `AVERAGE(Members[VisitsPerMonth])` |
| **Total Revenue** | `SUM(Members[MembershipFee])` |

**Data fields used:** Name, Age, Gender, Membership_Type, Visits_Per_Month, Days_Since_Last_Visit, Churn, At_Risk_Flag, Exercise_Type, Calories_Burned, Workout_Duration, Weight_Lifted, Membership_Fee.

---

## 🛠️ Tools & Techniques

- **Power BI** — report pages, slicers, DAX measures, custom dark theme
- **Visualization types** — KPI cards, gauge chart, column charts, area chart, donut chart, horizontal bar charts, scatter plot, data table

---

## 📁 Repository Structure


---

## 🚀 How to Use

1. Download or clone this repository
2. Open `GYM_DASHBOARD.pbix` in **Power BI Desktop**
3. Use the slicers (At Risk Flag, Churn, Gender, Membership Type) to explore the dashboard

---

## 💡 Key Insights

- **Headline numbers:** **150** total members, **Rs1.49M** total revenue, **14** avg visits/month, **105** members flagged at risk, and a **26%** churn rate.
- **Churn breakdown:** 74% (111) of members are retained (No churn) vs. 26% (39) churned.
- **Plan performance:** Monthly members churn the most at **29%**, followed by Quarterly (26%) and Yearly (18%) — longer commitments retain better.
- **Exercise performance:** Pull-Ups burn the most calories on average (**515.33**), followed by Bench Press (512.60).
- **Age group engagement:** The 30–39 age group is the most active, averaging **630** visits/month collectively, ahead of 20–29 (554).
- **Risk concentration:** 70% of members (105 of 150) are currently flagged at risk — a strong signal for a targeted retention campaign.

---

## 👤 Author

**Hammad**

- LinkedIn: [linkedin.com/in/hammad-ali-baig](https://www.linkedin.com/in/hammad-ali-baig)
- GitHub: [github.com/HammadAliBaig-Analytics](https://github.com/HammadAliBaig-Analytics)

Feedback and suggestions are welcome!
