## **Building a Decision Tree using the CART algorithm for DATA WEATHER**

The **CART (Classification and Regression Trees)** algorithm builds a **binary decision tree** using the **Gini Index** to find the best split. The goal is to divide the dataset into groups that are as pure as possible.

---

# **1. Given Dataset**

| Day | Outlook  | Temperature | Humidity | Play |
| --- | -------- | ----------- | -------- | ---- |
| D1  | Sunny    | Hot         | High     | No   |
| D2  | Sunny    | Hot         | High     | No   |
| D3  | Overcast | Hot         | High     | Yes  |
| D4  | Rain     | Mild        | High     | Yes  |
| D5  | Rain     | Cool        | Normal   | Yes  |

Target variable: **Play (Yes / No)**

Total records = **5**

* Yes = **3**
* No = **2**

---

# **2. Calculate Initial Gini Index**

[
Gini = 1 - (P_{Yes}^2 + P_{No}^2)
]

[
P_{Yes} = 3/5
]

[
P_{No} = 2/5
]

[
Gini = 1 - ( (3/5)^2 + (2/5)^2 )
]

[
Gini = 1 - (9/25 + 4/25)
]

[
Gini = 1 - 13/25 = 12/25 = 0.48
]

---

# **3. Choose Best Attribute for Root Node**

We evaluate splits using **Gini Impurity**.

### **Split on Outlook**

Groups:

**Sunny**

D1, D2 → No, No
Gini = 0 (pure)

**Overcast + Rain**

D3, D4, D5 → Yes, Yes, Yes
Gini = 0 (pure)

Since both groups are **pure**, this is the **best split**.

---

# **4. Construct Decision Tree**

Using the **CART algorithm**, we create a **binary split**.

```
            Outlook
           /       \
       Sunny     Overcast/Rain
        |             |
       Play=No      Play=Yes
```

---

# **5. Final Decision Rules**

From the tree we get:

**Rule 1**

If Outlook = Sunny
→ Play = No

**Rule 2**

If Outlook = Overcast or Rain
→ Play = Yes

---

# **6. Final CART Decision Tree**

```
             [Outlook]
            /         \
        Sunny      Overcast/Rain
         (No)          (Yes)
```

---

# **7. Conclusion**

Using the **CART algorithm**, the dataset is split based on the **Outlook attribute**, producing a simple binary decision tree. The algorithm uses the **Gini Index** to select the best split and continues until pure leaf nodes are obtained.

---

✅ **Tip for exams:**
After drawing the tree, **always write the decision rules**. This helps secure **full marks in a 20-mark Big Data Analytics question.**

---

If you want, I can also show **the full step-by-step Gini calculations for Temperature and Humidity splits** (teachers sometimes expect that for 20-mark answers).
