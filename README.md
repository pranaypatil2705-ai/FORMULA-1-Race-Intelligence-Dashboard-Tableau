# FORMULA 1 Race Intelligence Dashboard Analysis Report (2010 – 2026)

[![Tableau](https://img.shields.io/badge/Tableau-Public-orange?style=flat&logo=tableau)](https://public.tableau.com)
[![Records](https://img.shields.io/badge/Dataset-6%2C464%20Race%20Records-blue)](#dataset-scope)
[![Seasons](https://img.shields.io/badge/Seasons-2010--2026%20(17%20Seasons)-red)](#executive-overview)
[![Capstone](https://img.shields.io/badge/MySkillWallet-Data%20Analytics%20Capstone-green)](#capstone-phases)

---

## 🎓 Student Submission Metadata

| Field | Student Details |
| :--- | :--- |
| **Student Name:** | **Pranay Patil** |
| **Enrollment Number:** | **EN25EL3010049** |
| **College Email:** | **en25el3010049@medicaps.ac.in** |
| **College / University:** | **Medi-Caps University** |
| **Project Domain:** | Data Analytics with Tableau |
| **GitHub Repository:** | [https://github.com/pranaypatil2705-ai/FORMULA-1-Race-Intelligence-Dashboard-Tableau](https://github.com/pranaypatil2705-ai/FORMULA-1-Race-Intelligence-Dashboard-Tableau) |

---

## 🏎️ Executive Overview
This project delivers a comprehensive, multi-dimensional **Formula 1 Race Intelligence Dashboard** built in **Tableau**, analyzing **6,464 race records** across **17 competitive seasons (2010 – 2026)** and four distinct regulatory eras (V8 Naturally Aspirated, Turbo-Hybrid 1.0, Ground Effect, and 2026 Active Aero).

The platform addresses the operational requirements of three key stakeholders:
1. **Mr. Arnold / Rajan** — F1 Team Performance Strategist (Mid-Tier Benchmark, Tyre Degradation, Talent Scouting).
2. **Ms. Lisa / Divya** — Motorsport Broadcast Analyst (Cumulative Driver Leaderboard, Host Countries, Podium Conversion Share).
3. **Mr. Gilchrist / Arvind** — FIA Technical Regulation Compliance Analyst (DNF Mechanical Failure Audit, Multi-Era Reliability Growth).

---

## 📁 Repository Structure

```
├── F1 Racing Project Dataset.xlsx                            # Master 5-sheet relational dataset (6,464 race records)
├── FORMULA 1 Race Intelligence Dashboard - Project Report.pdf  # Comprehensive Capstone Final Report (Pranay Patil)
├── Demonstration_Video_Script.txt                           # Word-by-word presentation script for screen recording
├── README.md                                                 # Project overview and submission documentation
│
├── phase 1/                                                  # Ideation Phase
│   ├── Brainstorm_and_Idea_Prioritization.pdf
│   ├── Define_Problem_Statements.pdf                         # PS-1 (Rajan), PS-2 (Divya), PS-3 (Arvind)
│   └── Empathy_Map_Canvas.pdf
│
├── phase 2/                                                  # Project Design Phase-II
│   ├── Customer_Journey_Map.pdf
│   ├── Data_Flow_Diagram_and_User_Stories.pdf
│   ├── Solution_Requirements.pdf
│   └── Technology_Stack.pdf
│
├── phase 3/                                                  # Problem-Solution Fit & Architecture Phase-III
│   ├── Problem_Solution_Fit.pdf
│   ├── Problem_Solution_Fit_Canvas.pdf
│   ├── Project_Proposal.pdf
│   └── Solution_Architecture.pdf
│
├── phase 4/                                                  # Project Planning Phase-IV
│   └── Project_Planning.pdf
│
├── phase 5/                                                  # Visualization Development Phase-V
│   ├── F1_Race_Intelligence_Business_Question_and_Visualisation_Report.pdf  (5 Marks)
│   ├── F1_Race_Intelligence_Dashboard_Design.pdf
│   └── F1_Race_Intelligence_Story_Design.pdf
│
├── phase 6/                                                  # Tableau Development Phase-VI
│   └── Tableau.pdf
│
├── phase 7/                                                  # Project Reporting Phase-VII
│   └── FORMULA 1 Race Intelligence Dashboard - Project Report.pdf
│
└── phase 8/                                                  # Demonstration & Scope Phase-VIII
    ├── Communication.pdf
    ├── Demonstration_of_Proposed_Features.pdf
    ├── Project_Demo_Planning.pdf
    ├── Scalability_and_Future_Plan.pdf
    └── Team_Involvement_in_Demonstration.pdf
```

---

## 🎯 9 Core Tableau Visualizations

### Scenario 1: Team Performance Strategist (Rajan)
* **Visual 1 (Constructor Trajectory Benchmark):** Multi-line points progression comparing Aston Martin, Alpine, and Sauber/Audi against Red Bull Racing and Mercedes-AMG.
* **Visual 2 (Pirelli Tyre Compound Degradation):** Heatmap evaluating Soft, Medium, and Hard pace loss across Permanent, Street, and High-Speed circuits.
* **Visual 3 (Global Talent Scouting Map):** World map distribution of driver championship points across origin nations (UK, Germany, Spain, Netherlands).

### Scenario 2: Motorsport Broadcast Analyst (Divya)
* **Visual 4 (Driver Performance Leaderboard):** Sorted horizontal bar chart ranking top drivers by points (Hamilton 4,825.5, Verstappen 3,110.5, Vettel 2,985.0), wins, and poles.
* **Visual 5 (Global Host Countries Distribution):** Ranked chart displaying Grand Prix rounds hosted (Italy 28, Spain 19, USA 19, UK 18).
* **Visual 6 (Podium Achievement Share):** Constructor podium monopoly distribution (Mercedes 286, Red Bull 268).

### Scenario 3: FIA Technical Regulation Compliance (Arvind)
* **Visual 7 (DNF Failure Classification by Era):** 100% stacked bar chart dissecting Engine, Collision, Gearbox, Brakes, and Hydraulics retirements.
* **Visual 8 (Grid Reliability Progression %):** Trendline tracking race completion rates rising from 81.8% (2010) to 92.4% (2026).
* **Visual 9 (Driver Reliability Index):** Finished races vs. retirements ledger highlighting grid leaders (Oscar Piastri 93.9%, Lewis Hamilton 92.0%).

---

## 🧮 Tableau Calculated Fields

```tableau
// 1. Reliability Rate (%)
(1 - (SUM([dnf]) / COUNT([race_id]))) * 100

// 2. Podium Finish Flag
IIF([finish_position] <= 3, 1, 0)

// 3. Win Conversion Rate (%)
SUM(IIF([finish_position] = 1, 1, 0)) / COUNT([race_id]) * 100
```
