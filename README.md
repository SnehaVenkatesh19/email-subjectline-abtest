# 📧 A/B Test on Email Subject Lines for Subscription Uplift

## 📌 Objective
To evaluate whether a new email subject line (Treatment) improves user engagement and subscription rates compared to the existing subject line (Control).

---

## 📊 Dataset
- 10,000 synthetic users
- Features:
  - `group` (control/treatment)
  - `opened`, `clicked`, `subscribed`
  - `device`, `age_group`, `source`, `location`

---

## 🔬 Methodology

### Funnel Breakdown
- **Open Rate**:  
  - Control: 30.2%  
  - Treatment: 37.1% ✅  
- **Click-Through Rate**:  
  - Control: 6.0%  
  - Treatment: 8.8% ✅  
- **Subscription Rate**:  
  - Control: 0.6%  
  - Treatment: 1.2% ✅  

### Z-Tests (Statistical Significance)
- Open Rate: **Z = -7.36, p < 0.001** 
- Click Rate: **Z = -5.27, p < 0.001**   
- Subscription Rate: **Z = -3.17, p = 0.0015**   
→ The treatment subject line significantly improved every stage of the funnel.

### Confidence Intervals (95%)
- Control Subscription Rate: 0.4% to 0.8%  
- Treatment Subscription Rate: 0.9% to 1.5%  
→ Intervals do **not** overlap → strong evidence of uplift.

### Logistic Regression
- Used `group`, `device`, `age_group`, `source`, `opened`, and `clicked` to predict `subscribed`
- Model showed good fit, though quasi-separation indicated strong prediction

### Segmented Funnel Insights
- **Mobile users** and **users aged 25–44** responded best to the new subject line
- Subscription rate for mobile-treatment group: **1.35%** vs. **0.61%** in control

### Interaction Effects
- Treatment impact was slightly stronger for mobile and age 35–44 users
- Logistic regression with interaction terms confirmed segment-wise trends

---

## 💡 Key Takeaways
- **Treatment subject line significantly improved** all funnel metrics
- Especially effective for **mobile users** and **age group 35–44**
- Clear business case to roll out Subject B across all segments, with targeting focus on younger mobile users

---
