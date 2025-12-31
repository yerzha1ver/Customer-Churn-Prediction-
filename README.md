# Customer-Churn-Prediction
Data Science Project to analyze customer churn based on various customer-related features
### Overall Project Progress

This project demonstrates a well-structured and methodical approach to solving a customer churn problem, progressing logically from data understanding to business-oriented modeling conclusions. The workflow covers all critical stages: data cleaning, exploratory data analysis (EDA), feature engineering, model development, hyperparameter tuning, and evaluation. Each step contributes meaningfully to the final outcome, ensuring that model results are not only statistically sound but also interpretable and actionable from a business perspective.

The dataset was handled appropriately, with careful treatment of categorical variables, numerical scaling, and feature selection. The reduction to a set of high-impact features (such as tenure, contract type, monthly charges, service add-ons, and payment method) reflects a strong alignment between statistical relevance and business intuition.

### Key Insights from EDA (Business Perspective)

EDA revealed a clear churn pattern driven by **customer commitment and engagement**. Customers with:

* Short tenure,
* Month-to-month contracts,
* Higher monthly charges,
* Lack of value-added services (Online Security, Tech Support),
* Electronic check payment methods

are significantly more likely to churn.

These findings suggest that churn is less about dissatisfaction alone and more about **low switching costs and weak service integration**. From a business standpoint, this supports strategies focused on early customer lifecycle interventions, bundling services, incentivizing long-term contracts, and improving onboarding for new customers.


### Model Selection and Performance Analysis (Core Focus)

Multiple models were evaluated, including **Logistic Regression, AdaBoost, Random Forest, and CatBoost**, with performance compared using metrics aligned to the churn use case (ROC-AUC, recall, precision, and F1-score).

#### Why Model Selection Matters Here

In churn prediction, **false negatives are costly**—missing a customer who is about to leave means losing revenue and lifetime value. Therefore, the priority is not raw accuracy but **recall and probability ranking**, enabling the business to identify at-risk customers early.

#### CatBoost – Best Model Choice

CatBoost clearly emerges as the **optimal model** for this problem:

* Handles categorical variables natively, avoiding information loss from encoding
* Demonstrates the strongest balance between **recall, ROC-AUC, and stability**
* Shows superior generalization compared to Random Forest
* Produces reliable probability estimates, which are essential for threshold tuning

Importantly, CatBoost aligns well with business needs because its decision threshold can be adjusted to favor recall over precision, allowing the company to proactively target more customers with retention campaigns.

#### Random Forest – Suboptimal for This Use Case

Although Random Forest performs reasonably, it underperforms CatBoost in identifying churners. Its lower recall makes it less suitable when the goal is churn reduction rather than pure classification accuracy. Additionally, it is more sensitive to feature engineering and scaling choices.


### Final Business Conclusion

From both a technical and strategic perspective, **CatBoost is the most appropriate model for deployment**. It not only delivers the best predictive performance but also integrates seamlessly with business decision-making processes by enabling risk-based customer prioritization.

The project successfully translates data science outputs into **clear business actions**:

* Target high-risk customers early
* Incentivize long-term contracts
* Promote bundled services
* Focus retention efforts on the first months of customer tenure

Overall, this project represents a strong, production-ready churn modeling pipeline with a well-justified model selection grounded in both data performance and business impact.
