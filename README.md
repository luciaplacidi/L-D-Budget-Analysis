# Measuring ROI of Learning and Development

> **Note:** All the data has been generated with a Python script.

## Project Overview & Objectives

This project investigates the impact of Learning and Development (L&D) spending on employee performance, satisfaction, and engagement. The analysis stems from an existing HR general dashboard, which tracked employee performance metrics and usage of L&D budgets across the organisation.

One key observation from the dashboard was that approximately 70% of active employees had used their L&D budget in the past year. However, the dashboard didn’t provide insight into whether this investment was delivering measurable value. This prompted a deeper analysis to investigate the return on L&D investment, specifically, whether employees who engaged in learning and development performed better and reported higher satisfaction.

The goal of this project was to apply analytical techniques to evaluate the return on L&D investment, uncovering actionable insights for HR and leadership teams.

<!--- - [View the HR dashboard here](#) -->
- [View the Python script to generate the data here](#)
- [View the analysis script here](#)

## Data Structure

The analysis is based on four structured datasets created using Python to reflect a realistic employee base of 500 individuals. These datasets are designed to replicate HR systems.

## Executive Summary

The analysis revealed a clear link between L&D investment and improved performance and satisfaction. Employees who used their L&D budget showed higher performance gains from baseline (Q0) to the final quarter (Q4) and reported greater satisfaction by the end of the year.

**Key highlights:**
- 71.2% of active employees used some portion of their L&D budget
- Departments with higher L&D uptake (e.g. Engineering and Sales) also saw stronger average performance improvements
- Junior and Mid-level employees benefited the most from L&D spend
- Moderate spenders ($250–$600) were consistently among the most satisfied, suggesting strategic L&D investment is more effective than maximal spend

![Performance Change by Spend Tier](https://github.com/luciaplacidi/L-D-Budget-Analysis/blob/main/graphs/performance_spend_tier.png)

## Exploratory Overview

### Distribution of Learning & Development Spend
This histogram shows the distribution of L&D spending across the employee population.  
![Histogram](https://github.com/luciaplacidi/L-D-Budget-Analysis/blob/main/graphs/spend_distribution.png)

### Correlation Matrix
We looked at the correlation between L&D spend and outcome variables like performance and satisfaction.  
![Correlation Matrix](https://github.com/luciaplacidi/L-D-Budget-Analysis/blob/main/graphs/correlation_matrix.png)

### Scatterplot
The scatterplot shows the relationship between L&D Spend and Performance Change (Q4 - Q0). The trend line is upward, especially once spending exceeds zero, supporting the relationship between higher investment and performance improvement.  
![Scatterplot](https://github.com/luciaplacidi/L-D-Budget-Analysis/blob/main/graphs/scatterplot.png)

## Insights

### L&D Participation by Department
Engineering and Sales departments had both high participation (over 77%) and performance improvement. HR and Finance departments had lower L&D usage, raising questions about accessibility or perceived relevance of offerings.  
![Department Spend](https://github.com/luciaplacidi/L-D-Budget-Analysis/blob/main/graphs/department_spend.png)

### Performance Change vs Spend Tier
Employees who spent between $600–$1,000 on L&D had the greatest gains in performance, particularly in high-impact roles. Those who did not use their budget generally experienced little to no improvement. A clear performance improvement trend emerges as L&D spend increases. The largest gains are seen in Sales and Engineering departments, especially in the $600–$1000 tier. Departments with lower spend show flatter or more variable results.  
![Performance by Dept and Tier](https://github.com/luciaplacidi/L-D-Budget-Analysis/blob/main/graphs/perf_tier_dep.png)

### L&D Impact by Employee Level
Junior and Mid-level employees showed a strong response to L&D spending. The return was less consistent for Senior and Lead employees, suggesting that different development strategies may be needed at higher levels.  
![Performance by Level and Tier](https://github.com/luciaplacidi/L-D-Budget-Analysis/blob/main/graphs/perf_tier_level.png)

### Satisfaction Trends
Average satisfaction scores increased in line with L&D spend up to the $600 mark, but plateaued or declined at the highest tier. This indicates that while development opportunities are valued, more spending doesn't always equate to better outcomes.  
![Satisfaction Score](https://github.com/luciaplacidi/L-D-Budget-Analysis/blob/main/graphs/satisfaction.png)

## Statistical Testing: Does L&D Spending Actually Improve Performance?

To go beyond visual trends, two statistical tests were used to evaluate whether L&D spending has a meaningful effect on performance:

### 1. Regression Analysis
A linear regression was run to test whether L&D spend predicts performance improvement, controlling for each employee’s starting performance score.

**Result:**  
Employees who spent more on L&D tended to improve slightly more, and this relationship was statistically significant.  
- Coefficient: +0.0019  
- p-value: < 0.0001

**Outcome:**  
For every additional dollar spent on L&D, performance improvement increases by 0.0019 points. While the effect is small, it's statistically meaningful.

### 2. T-Test: Spending Something vs Spending Nothing
We compared two groups:
- Employees who spent $0 of their L&D budget  
- Employees who spent more than $0

**Result:**  
Those who used their L&D budget had a significantly greater increase in performance.  
- t-statistic: 5.87  
- p-value: < 0.0001

**Outcome:**  
This suggests that using the L&D budget — even partially — is associated with better performance outcomes.

## Recommendations

Based on the uncovered insights, the following recommendations have been provided:

- Target underperforming departments (e.g. HR, Finance) by identifying barriers to access or relevance and tailoring communication or training pathways to increase usage.
- Segment L&D programs by employee level: Junior staff benefit most from skill-building, while Senior staff may need more strategic or leadership development to see impact.
- Encourage moderate L&D spending as the most satisfied and high-performing employees were often those in the $250–$600 spend range. Communicate this to employees to encourage optimal investment.

This analysis supports the case for a data-driven L&D strategy that not only promotes participation but aligns spending with meaningful employee outcomes.
