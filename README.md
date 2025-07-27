# 📊 Alternative Tuition Graph – Linked Structure Version

This is an alternative approach to visualizing school tuition data using a **self-referential linked structure** (instead of a list).

---

## 🔄 What’s Different?

Unlike the `ListOfSchool` approach, this solution uses a single self-referential structure:
```racket
(define-struct school (name tuition next))
;; A School is one of:
;; - false
;; - (make-school String Natural School)

---

## 🎯 What It Does
Renders a bar chart of school tuition values using 2htdp/image

Recursively walks through each (make-school ...) node

Uses overlay/align to stack rotated labels and bars

---

## 💡 Concepts Practiced

- Self-referential data structures  
- Recursion over linked data  
- Functional programming with conditionals  
- Modular rendering with `2htdp/image`


---

## 🤔 Comparison
Compared to the first version:

❌ This version requires handling both data and display in one function

✅ It simplifies the data definition into a single struct

➡️ Preference: We prefer the list-based version for clarity and separation of concerns.

