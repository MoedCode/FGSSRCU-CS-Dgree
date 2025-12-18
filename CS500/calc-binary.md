Perfect — let’s turn this into **one clean, correct, exam-ready note** you can keep and rely on.
I’ll **correct the mistakes**, keep your style, and present it **as a single reference**.

---

## **Binary Addition – Complete Carry Rules (Final Note)**

### **Without carry**

```
0 + 0 = 0
1 + 0 = 1
0 + 1 = 1
1 + 1 = 0   carry 1        (2 = 10₂)
```

---

### **With carry = 1 (carry-in from previous column)**

> Always calculate:
> **bit1 + bit2 + carry**

```
0 + 0 + 1 = 1   → 1 = 01₂   → result = 1 , carry = 0
```

```
0 + 1 + 1 = 2   → 2 = 10₂   → result = 0 , carry = 1
```

```
1 + 0 + 1 = 2   → 2 = 10₂   → result = 0 , carry = 1
```

```
1 + 1 + 1 = 3   → 3 = 11₂   → result = 1 , carry = 1
```

---

## **Corrected summary table (most important part)**

| bit A | bit B | carry-in | sum (decimal) | result | carry-out |
| ----- | ----- | -------- | ------------- | ------ | --------- |
| 0     | 0     | 0        | 0             | 0      | 0         |
| 1     | 0     | 0        | 1             | 1      | 0         |
| 0     | 1     | 0        | 1             | 1      | 0         |
| 1     | 1     | 0        | 2             | 0      | 1         |
| 0     | 0     | 1        | 1             | 1      | 0         |
| 0     | 1     | 1        | 2             | 0      | 1         |
| 1     | 0     | 1        | 2             | 0      | 1         |
| 1     | 1     | 1        | 3             | 1      | 1         |

---

## **Golden rule (write this on top of your notes)**

> **If the sum in a column is 0 or 1 → no carry**
> **If the sum is 2 or 3 → carry = 1**

---

## **Key clarifications (fixing your doubts)**

❌ `0 + 0 carried 1 = 10₂` → **wrong**
✅ `0 + 0 + 1 = 1` → **no carry**

❌ `1 + 1 = 1 carry 1` → **wrong**
✅ `1 + 1 = 0 carry 1`

❌ thinking carry depends on the result bit
✅ carry depends on the **total sum**

---

This note is now **100% correct**, **CPU-level accurate**, and **exam safe**.

If you want next, I can:

* do the same kind of **clean note** for **binary subtraction (borrow)**
* or connect this directly to **1’s & 2’s complement**

Just say which one.
