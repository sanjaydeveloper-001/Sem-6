

# 14.a) Build Decision Tree using CART Algorithm (DATA WEATHER)

### Given Dataset

| Day | Outlook  | Temperature | Humidity | Play |
| --- | -------- | ----------- | -------- | ---- |
| D1  | Sunny    | Hot         | High     | No   |
| D2  | Sunny    | Hot         | High     | No   |
| D3  | Overcast | Hot         | High     | Yes  |
| D4  | Rain     | Mild        | High     | Yes  |
| D5  | Rain     | Cool        | Normal   | Yes  |

---

## Step 1: CART Algorithm Concept

**CART (Classification and Regression Tree)** is a decision tree algorithm that uses **binary splits** and the **Gini Index** to select the best attribute. 

Gini Index Formula:

[
Gini = 1 - \sum (p_i)^2
]

Where
(p_i) = probability of class i

The attribute with the **minimum Gini value** is chosen as the root node.

---

## Step 2: Choose Root Node

From calculations (similar to PDF method), **Outlook** generally gives the minimum impurity.

Therefore:

**Root Node = Outlook**

---

## Step 3: Split Dataset

### Case 1: Outlook = Overcast

| Day | Play |
| --- | ---- |
| D3  | Yes  |

Pure node → Leaf = **Yes**

---

### Case 2: Outlook = Sunny

| Day | Play |
| --- | ---- |
| D1  | No   |
| D2  | No   |

Leaf = **No**

---

### Case 3: Outlook = Rain

| Day | Play |
| --- | ---- |
| D4  | Yes  |
| D5  | Yes  |

Leaf = **Yes**

---

## Final Decision Tree

```
            Outlook
          /    |     \
       Sunny Overcast Rain
        No      Yes     Yes
```

---

## Decision Rules

1. If Outlook = Sunny → Play = No
2. If Outlook = Overcast → Play = Yes
3. If Outlook = Rain → Play = Yes

---
