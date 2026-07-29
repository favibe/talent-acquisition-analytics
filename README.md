# 🎯 Talent Acquisition Analytics

&gt; **Data-driven insights to optimize tech talent recruitment pipeline**

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-1.3+-green.svg)](https://pandas.pydata.org)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 📌 Table of Contents

- [Business Problem](#business-problem)
- [Dataset](#dataset)
- [Key Findings](#key-findings)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Analysis](#analysis)
- [Recommendations](#recommendations)
- [Author](#author)

---

## 🎯 Business Problem

**"What factors drive talent approval decisions, and how can we optimize our recruitment pipeline to improve approval rates and quality of hire?"**

A tech talent acquisition platform processed **1,550 candidate profiles** but achieved only a **32.8% approval rate**. This project analyzes the data to identify which candidate segments perform best and provides actionable strategies to improve pipeline efficiency.

---

## 📁 Dataset

| Feature | Description | Type |
|---------|-------------|------|
| `URL` | LinkedIn profile link | String |
| `First_Name` | Candidate first name | String |
| `Last_Name` | Candidate last name | String |
| `Job_Title` | Full job description | String |
| `Status` | Approval decision | Categorical |

**Size:** 1,550 rows × 5 columns

**Engineered Features:**
- `Employer_Name` — Extracted company from job title
- `Job_Category` — Standardized role classification  
- `Seniority_Level` — Experience level classification

---

## 🔑 Key Findings

### 1. Overall Pipeline Health
- **Approval Rate:** 32.8% (509 approved / 1,041 rejected)

### 2. Seniority Level is the Strongest Predictor
| Level | Approval Rate |
|-------|--------------|
| **Junior** | **62.5%** ⭐ |
| Management | 47.5% |
| Senior | 33.8% |
| Mid-Level | 32.7% |
| Lead | 23.1% ⚠️ |
| Intern | 15.8% |

### 3. Job Category Performance
| Category | Approval Rate |
|----------|--------------|
| **DevOps/SRE** | **40.0%** ⭐ |
| Full Stack | 38.6% |
| Software Engineer | 32.5% |
| Frontend | 31.0% |
| Backend | 29.2% |
| Mobile | 27.3% |
| QA | 25.0% |

### 4. Talent Source Risk
- **Andela** = 17.4% of all talent (270 profiles)
- **36.8%** have no identifiable employer

---

## 🛠 Technologies Used

- **Python** — Primary language
- **Pandas** — Data manipulation
- **NumPy** — Numerical computations
- **Matplotlib** — Visualizations
- **Seaborn** — Statistical charts
- **Regex** — Text pattern extraction

---





---

## ⚙️ Installation

```bash
# Clone repo
git clone https://github.com/YOUR_USERNAME/talent-acquisition-analytics.git
cd talent-acquisition-analytics

# Create environment
python -m venv venv
venv\Scripts\activate  # Windows
source venv/bin/activate  # Mac/Linux

# Install packages
pip install -r requirements.txt

# Run notebook
jupyter notebook notebooks/01_talent_analysis.ipynb
