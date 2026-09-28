# Workforce, Service Quality & Margin Analysis Workflow

## Business Question

> **Why are turnover, agency usage, service quality and margin deteriorating, and where should Operations intervene first?**

---

## 1. Data Sources

The analysis integrates data from multiple operational and financial systems.

| Data Source | Key Data |
|---|---|
| **HR System** | Employees, joiners, leavers, tenure |
| **Recruitment Tracking** | Vacancies, hires, time-to-fill |
| **Rostering System** | Planned shifts, staffing, hours |
| **Call Monitoring** | Actual visits, lateness, missed visits |
| **Payroll** | Pay, overtime, employee costs |
| **Finance Billing Ledger** | Revenue, contract billing |

---

## 2. Data Quality & Reconciliation

Before analysis, data is validated and reconciled across systems.

### Data Quality Checks

- Match employee IDs
- Match branch IDs
- Match service-user / contract IDs
- Reconcile planned vs delivered hours
- Reconcile payroll vs roster hours
- Reconcile billing vs operational activity
- Identify missing records
- Identify duplicate records
- Document conflicting definitions

---

## 3. Data Model

### Dimensions

- **Branch**
- **Employee**
- **Service User**
- **Contract**
- **Date**
- **Agency**

### Fact Tables

- **Employee Events**
- **Roster**
- **Visits**
- **Payroll**
- **Recruitment**
- **Billing**
- **Complaints / Quality**

---

## 4. Standardised Definitions

Consistent definitions are established before calculating KPIs.

| Metric | Definition |
|---|---|
| **Turnover** | Agreed leaver / average headcount methodology |
| **Agency Hours** | Hours delivered by agency carers |
| **On-Time Visit** | Agreed commissioner definition |
| **Missed Visit** | Agreed operational definition |
| **Continuity** | Agreed carer/service-user continuity metric |
| **Complaint** | Agreed quality definition |
| **Leaver Cost** | Recruitment + onboarding + vacancy + agency/overtime + other attributable costs |
| **Contract Margin** | Revenue − attributable costs |

---

# 5. Workforce Analysis

The workforce analysis examines the scale and characteristics of employee turnover and staffing pressure.

### Key Areas

- Turnover
- Leaver volume
- Employee tenure
- Voluntary vs involuntary leavers
- Recruitment activity
- Vacancy levels
- Time-to-fill
- Workforce availability

---

# 6. Service Delivery Analysis

Service delivery performance is analysed alongside workforce conditions.

### Key Areas

- Late visit rate
- Missed visit rate
- Continuity
- Complaints
- Delivered hours
- Agency delivery
- Planned vs delivered hours

---

# 7. Linkage Analysis

The analysis moves beyond individual KPIs to investigate relationships between workforce, service delivery and financial outcomes.

### Relationships Investigated

```text
Turnover
   │
   ├──► Agency Usage
   │
   ├──► Late Visits
   │
   ├──► Missed Visits
   │
   └──► Complaints

Agency Usage
   │
   ├──► Service Quality
   │
   └──► Contract Margin

Continuity
   │
   └──► Service Quality
