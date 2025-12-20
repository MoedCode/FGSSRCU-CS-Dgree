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
# **Subtract**
Exactly — that’s the key idea behind **binary borrowing**. Let me explain clearly:

---

## **Binary Borrow Rule**

1. In decimal subtraction, if you borrow 1 from the next column, it adds **10** to the current column.
2. In binary subtraction, if you borrow 1 from the next column, it adds **2 (10₂)** to the current column.

---

### **Example**

Suppose we subtract column by column:

```
Current column: 0
Subtract:       1
Need borrow:    Yes, borrow 1 from next column
```

* In binary, borrowing **adds 2** to the current column:

```
0 + 2 = 10₂
10₂ - 1 = 1 (result)
```

* The borrow is now **propagated to the next column on the left**.

---

### **Consecutive borrows**

If the next column is also 0, we **must borrow again**, and each time:

* You take 1 from the next left column
* Add 2 to the current column
* Subtract as usual

This can propagate **multiple consecutive borrows** until you reach a column with 1.

---

### **Illustration (simplified)**

```
Number1:  1 0 0 0 1
Number2:  0 1 1 1 1
```

Subtract **rightmost column**:

* Column 5: 1 - 1 = 0 → no borrow
* Column 4: 0 - 1 → borrow 1 from column 3 → 0 + 2 - 1 = 1 → borrow 1 to column 3
* Column 3: 0 - 1 - 1(borrow) → 0 + 2 - 1 -1 = 0 → borrow 1 to column 2
* Column 2: 0 - 1 -1(borrow) → 0 + 2 -1 -1 = 0 → borrow 1 to column 1
* Column 1: 1 -0 -1(borrow) = 0 → done

✅ Result: 0 0 0 1 0

---

So yes: **each borrow effectively adds 2 to the current column**, and **propagates left if needed**.

---

If you want, I can **redo the previous 1100101 – 0100111 example with a full “borrow added = 2” step-by-step table**, so you can **see exactly how 2 appears in each borrowed column**.

Do you want me to do that?
