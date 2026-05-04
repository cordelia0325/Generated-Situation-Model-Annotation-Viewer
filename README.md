# Situation Model Annotation Viewer

This tool is designed for annotating the correctness of situation model graphs generated from math word problems.

It allows you to:
- Inspect how the graph is constructed step by step
- Examine the final cumulative graph
- Label whether the final graph is correct
- Identify specific error types when the graph is incorrect

---

## 🔍 What you will do

For each problem:

1. Read the problem and sentence breakdown  
2. Inspect the **final cumulative graph**  
3. Decide:
   - Is the graph structurally correct?
4. If not:
   - Select **all applicable error labels**

---

## ✅ What counts as a “correct” graph

A graph is considered **correct only if it is fully structurally consistent with the problem**, regardless of whether the final numerical answer is correct.

This means:

- All required **nodes (containers)** are present  
- All required **relations (edges)** are present  
- Relation **type, direction, and quantity** are correct  
- The **reference variable (`ref`)** points to the correct target  

---

## 🧭 Annotation workflow

Follow this order when evaluating a graph:

1. **Node existence**
   - Missing node / Extra node

2. **Relation existence**
   - Missing relation / Extra relation

3. **Reference target**
   - Wrong reference target

4. **Relation configuration**
   - Wrong relation type  
   - Wrong direction  

5. **Slot content**
   - Wrong node or relation content  
   - Wrong quantity  

👉 If multiple issues exist, select all that apply  
👉 Prefer identifying the **root cause** rather than downstream effects  

---

## 🏷️ Error labels (quick guide)

- **Missing node**  
  A required entity/container is absent  

- **Extra node**  
  A node is present but not supported by the problem  

- **Missing relation**  
  A required relation is absent  

- **Extra relation**  
  A relation is added but not supported  

- **Wrong reference target**  
  `ref` points to the wrong existing node  

- **Wrong relation type**  
  Relation exists but type is incorrect (e.g., rate vs part-whole)

- **Wrong direction**  
  Relation direction is reversed  

- **Wrong node or relation content**  
  Entity / attribute / unit is incorrect  

- **Wrong quantity**  
  Numeric value or variable is incorrect  

- **Other**  
  Any issue not covered above  

---

## 🖥️ How to use the interface

- Use the **left panel** to select a problem  
- Read the sentence breakdown (top)  
- Focus on the **final cumulative graph**  
- Use the **annotation panel** (bottom) to:
  - Mark correctness
  - Select error labels
  - Add notes if needed  

---

## 💾 Saving your annotations

- Annotations are automatically saved in your browser  
- You can export results as:
  - JSON
  - CSV  

---

## ⚠️ Important notes

- Do **not** judge based on final numerical answer  
- Focus only on **graph structure and semantics**  
- When in doubt:
  - Prefer structural errors (node/relation) over value errors  
- Only use “Wrong reference target” if the correct node already exists  

---

## 📌 Tip

You can refer to the **“Error Reasons” page** in the interface for:
- Detailed definitions  
- Visual examples (correct vs incorrect graphs)  
