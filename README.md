# 📋 Project Portfolio & Tracker Dashboard

<table>
  <tr>
    <td>
      <img src=https://github.com/didarul-rashed/Project-Portfolio-Tracker-Dashboard/blob/c0cdbef31ac7de3403e785bb1002a73b15b86366/Screenshot%202026-11-13%20105436.png/>
    </td>
    <td>
      <img src=https://github.com/didarul-rashed/Project-Portfolio-Tracker-Dashboard/blob/c0cdbef31ac7de3403e785bb1002a73b15b86366/Screenshot%202026-11-13%20105528.png/>
    </td>
  </tr>
</table>
<table>
  <tr>
    <td>
      <img src=https://github.com/didarul-rashed/Project-Portfolio-Tracker-Dashboard/blob/c0cdbef31ac7de3403e785bb1002a73b15b86366/Screenshot%202026-11-13%20105611.png/>
    </td>
    <td>
      <img src=https://github.com/didarul-rashed/Project-Portfolio-Tracker-Dashboard/blob/c0cdbef31ac7de3403e785bb1002a73b15b86366/Screenshot%202026-11-13%20105650.png/>
    </td>
  </tr>
</table>

[![View Dashboard](https://img.shields.io/badge/PowerBI-Dashboard-blue?logo=powerbi)](https://app.powerbi.com/view?r=eyJrIjoiODk2ZTU1MmYtY2E4NC00Yzg1LWI3YWItMDFlYmFhNGFiMGE1IiwidCI6Ijg2NDU3OWM1LWVjMjctNDAzYi1hMjAwLWFhNjViYmEwMTIyMyIsImMiOjEwfQ%3D%3D)


## 🔎 Project Overview

An end-to-end project tracking solution built in Power BI on a SharePoint list, designed to monitor:

- Portfolio status (pipeline, in progress, on hold, completed)
- Projects needing attention (amber and red health)
- Delivery timeline against schedule
- Lifecycle stage of every project
- Owners, next steps and blockers
- Ongoing support, maintenance and training work

> ⚠️ All project names, owners and figures are fictional (dummy data) for portfolio presentation.

---

# 🎯 Business Problem

Management and the team needed:

- One consolidated view of every project
- Clear identification of delayed or blocked work
- Visibility of blockers in plain language, not buried in emails
- Effort tracking without manual hour entry
- A way to track ongoing support and training alongside projects
- No extra tools, hosting costs or licences beyond Power BI Pro

The challenge:
Mixed work types (projects, support, R&D, training) + a simple data entry experience + an executive-friendly view.

---

# 🧩 Dashboard Structure

## 1️⃣ Portfolio Page

### Covers:
- KPI cards: Total, Pipeline, In Progress, On Hold, Completed, Needs Attention, Training
- Gantt timeline of every project
- Lifecycle stage chart (Planned → Requirement → Development → Testing → UAT → Live → On Going)
- Project register with a blocker line under delayed or held projects

### Business Value:
- Shows the whole portfolio in seconds
- Highlights where management attention is needed
- Replaces manual status decks

---

## 2️⃣ Project Page

### Covers:
- Project selector
- Stage tracker
- Five KPI cards (progress, started, due, effort, last updated)
- Timeline with time used versus work done
- Details, owners, next step and blocker
- Bottom ticker with key updates

### Business Value:
- Gives a one-page answer to "where are we on this project?"
- Surfaces blockers early
- Makes owner and next-step accountability visible

---

## 3️⃣ Ongoing Work and Training

### Covers:
- Support and maintenance projects shown as "Ongoing" with no fake due date
- Training plan versus delivered hours
- On-hold projects that are built but waiting on a stakeholder

### Business Value:
- Keeps the portfolio honest about maintenance load
- Separates "waiting on others" from "delayed by us"

---

## 4️⃣ Navigation and Experience

### Covers:
- Bookmark-driven menu panel
- Page navigation between Portfolio and Project views
- Tap-to-ask panel with preset questions (in progress)

### Business Value:
- Lets managers use the report without training

---

# ⚙️ Technical Architecture

- Tool: Power BI (Pro), HTML Content custom visual
- Source: SharePoint list (Tasks), refreshed from Power BI Service
- Data prep: Power Query (M) for stage order, status order, owner badges and text cleaning
- Measures: DAX in a dedicated measures table
- Hours logic: derived from start and due dates (8 hours per working day, Saturday off) in a SharePoint calculated column; manual hours for support and training
- Visuals: native Gantt, cards and slicers, plus measure-driven HTML for the stage tracker, timeline, register and ticker

---

# 📊 Key KPIs Delivered

| KPI | Purpose |
|------|---------|
| Total Projects | Portfolio size |
| In Progress / On Hold / Completed | Delivery status |
| Needs Attention | Risk visibility (amber or red health) |
| Progress % | Work done per project |
| Time Used vs Work Done | Schedule health |
| Estimated Effort (hours) | Capacity planning |
| Training Hours (plan vs delivered) | Learning delivery |

---

# 🧠 Technical Complexity

- DAX measures that generate HTML for custom layouts
- Handling numbers that arrive as text from SharePoint calculated columns
- Sort-order columns built in Power Query to avoid circular dependencies
- Per-page bookmarks for a clean open and close menu
- Working-day hours logic that excludes weekends
- Dynamic verdict colours (on track, behind, overdue)
- Dummy-data version built in Power Query with dates relative to today

This is a complete project tracking system, not just a report.

---

# 🚀 Business Outcomes

✔ One live view of every project  
✔ Blockers visible early  
✔ No manual hour entry for project work  
✔ Support and training tracked properly  
✔ Faster, simpler management reviews  
✔ No extra hosting cost  

---

# 🗂️ Repository Structure

```
project-portfolio-tracker/
├── README.md
├── screenshots/
├── dax/            # measures (KPI cards, HTML visuals)
├── power-query/    # Tasks query and dummy-data query
└── docs/           # SharePoint column setup, build guide
```

---

## 📌 Note

This project is built for portfolio demonstration purposes.
All sensitive information has been replaced with dummy data.
