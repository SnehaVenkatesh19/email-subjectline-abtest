#  A/B Test on Email Subject Lines for Subscription Uplift

##  Objective  
To evaluate whether a new email subject line (Treatment) improves user engagement and subscription rates compared to the existing subject line (Control).

---

##  Dataset
- 10,000 synthetic email users
- Features:
  - `group` (control / treatment)
  - `opened`, `clicked`, `subscribed`
  - `device`, `age_group`, `source`, `location`

---

## Methodology

### Funnel Breakdown

| Metric           | Control | Treatment |  Uplift |
|------------------|---------|-----------|-----------|
| **Open Rate**    | 30.2%   | 37.1%     |  +6.9%   |
| **Click Rate**   | 6.0%    | 8.8%      |  +2.8%   |
| **Subscribe Rate** | 0.6%  | 1.2%      |  ~2x     |

---

### Statistical Tests (Z-Test Results)

- **Open Rate**: Z = -7.36, p < 0.001  
- **Click Rate**: Z = -5.27, p < 0.001  
- **Subscribe Rate**: Z = -3.17, p = 0.0015  

>  Statistically significant improvements across all stages.

---

### Confidence Intervals (95%)

- Control: **0.4% → 0.8%**  
- Treatment: **0.9% → 1.5%**  
> 📈 Intervals do **not overlap**, confirming a reliable uplift.

---

###  Logistic Regression

- Variables: `group`, `device`, `age_group`, `source`, `opened`, `clicked`
- Strong predictive power, quasi-separation indicates behavior-driven conversion
- Interaction terms added to test treatment effect across user segments

---

### Segmented Funnel Insights

-  **Mobile users** and  **users aged 25–44** responded best
- **Mobile-Treatment group**: 1.35% vs 0.61% in control
- Treatment effect most noticeable in age group **35–44**

---

##  Key Takeaways

- The **treatment subject line significantly outperformed** control across all funnel metrics  
- Treatment is **especially effective on mobile and middle-aged users (35–44)**  
- Strong business case to **roll out Subject Line B platform-wide**, with segmentation-based targeting

---

##  Tableau Dashboard

> Includes:
- KPI Tiles (Open, Click, Subscribe Rates)
- Funnel Comparison by Group
- Segmented Analysis by Device & Age Group

 *https://public.tableau.com/app/profile/sneha.venkatesh3644/viz/Email_AB_Testing/Dashboard1*



