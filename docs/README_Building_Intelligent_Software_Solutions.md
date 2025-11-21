# 💻🤖 Building Intelligent Software Solutions

## 🎯 Objective
This project demonstrates understanding of **AI applications in software engineering** through:
- Theoretical analysis
- Practical implementation
- Ethical reflection

It shows how AI can **automate tasks**, **enhance decision-making**, and **address challenges** in software development.

---

## 🧠 Part 1: Theoretical Analysis
### Q1. AI-Driven Code Generation
AI tools like **GitHub Copilot** reduce development time by suggesting intelligent code completions.  
**Limitations:** potential for inaccurate code, data bias, and overreliance.

### Q2. Supervised vs Unsupervised Learning in Bug Detection
| Aspect | Supervised Learning | Unsupervised Learning |
|--------|---------------------|------------------------|
| Definition | Uses labeled data | Uses unlabeled data |
| Example | Bug classification | Anomaly detection |
| Advantage | High accuracy | No need for labels |
| Limitation | Requires large labeled dataset | Possible false positives |

### Q3. Bias Mitigation in Personalization
Bias mitigation ensures fairness, avoiding exclusion or stereotyping in user experiences.

### Case Study: AIOps in DevOps
AIOps improves deployment by:
1. Predicting rollbacks before failures.
2. Dynamically scaling resources based on predicted workloads.

---

## ⚙️ Part 2: Practical Implementation

### Task 1: AI-Powered Code Completion
**Manual Implementation**
```python
def sort_dicts_by_key(data, key):
    return sorted(data, key=lambda x: x[key])
```
**AI (Copilot) Implementation**
```python
def sort_dicts_by_key(data, key):
    return sorted(data, key=lambda item: item.get(key, None))
```
**Analysis:**  
Copilot’s version adds robustness with missing-key handling while maintaining efficiency (**O(n log n)**).

---

### Task 2: Automated Testing with AI
**Tool:** Selenium IDE / Testim.io  
**Goal:** Automate login validation.

```python
from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()
driver.get("http://example.com/login")
driver.find_element(By.ID, "username").send_keys("testuser")
driver.find_element(By.ID, "password").send_keys("correctpass")
driver.find_element(By.ID, "login").click()
assert "Dashboard" in driver.title
driver.quit()
```

**Summary:**  
AI improves test coverage by learning UI changes and self-healing broken locators.

---

### Task 3: Predictive Analytics for Resource Allocation
**Dataset:** Breast Cancer (Kaggle / sklearn)  
**Model:** Random Forest  
**Goal:** Predict task priority.

```python
from sklearn.datasets import load_breast_cancer
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, f1_score

data = load_breast_cancer()
X_train, X_test, y_train, y_test = train_test_split(data.data, data.target, test_size=0.2)
model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(X_train, y_train)
y_pred = model.predict(X_test)

print("Accuracy:", accuracy_score(y_test, y_pred))
print("F1 Score:", f1_score(y_test, y_pred))
```

**Results:**  
Accuracy = 0.96, F1 = 0.95  
AI can efficiently predict priorities, optimizing resource use.

---

## ⚖️ Part 3: Ethical Reflection
Bias in datasets (e.g., underrepresented teams) can lead to unfair predictions.  
**Solution:** Tools like **IBM AI Fairness 360** detect and mitigate bias using reweighing or adversarial debiasing methods.

---

## 🚀 Bonus Task: Innovation Challenge — DocuMind
**Idea:** An AI tool that auto-generates documentation from code comments and commit history using NLP.

**Workflow:**
1. Collect code + Git logs  
2. Summarize with NLP  
3. Generate markdown/HTML documentation  
4. Auto-update via GitHub Actions

**Impact:** Saves time, maintains consistent, up-to-date documentation, and improves team collaboration.

---

## 📁 Submission Summary
| Component | Deliverable | Platform |
|------------|--------------|-----------|
| Code | Python Scripts + Jupyter Notebook | GitHub |
| Report | PDF with answers, screenshots & reflections | Community |
| Presentation | 3-min demo video | Groups |

---

## 🧩 Tools & Libraries
- **AI Tools:** GitHub Copilot, Testim.io, Google Colab  
- **Libraries:** Scikit-learn, Pandas, Selenium  
- **Dataset:** Kaggle (Breast Cancer)

---

## 🧠 Author
**Name:** Leon Kabugi  
**Course:** Software Engineering & AI  
**Theme:** *Building Intelligent Software Solutions*
