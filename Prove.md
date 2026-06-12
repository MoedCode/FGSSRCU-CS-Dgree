
### ما هي القاعدة أو النمط السري لحل كل مسائل الـ Prove؟

السر الأكبر الذي إذا فهمته ستحل أي إثبات هو: **"فكّك الكلمات إلى تعريفاتها الرياضية (Unpack the Definitions)".**
لا يوجد إثبات يُحل بالتأمل؛ الإثبات يُحل بأن تأخذ المعطى، وتكتب تعريفه الرياضي أو البرمجي، وستجد الحل يظهر أمامك.

في منهجك الحالي، الإثباتات مقسمة إلى **4 قوالب (Patterns)** ثابتة لا خامس لها. بمجرد أن تحدد نوع المسألة، ستعرف كيف تبدأ السطر الأول فوراً:

#### 1. قالب المجموعات (Set Theory Proofs)

* **متى تستخدمه؟** عندما ترى علامات $\subseteq$ أو $\cap$ أو $\cup$ أو $=$.
* **النمط الثابت (كيف تبدأ؟):** * إذا طلب إثبات $A \subseteq B$: ابدأ فوراً بجملة **"Let $x \in A$"** (لنفرض أن هناك عنصراً اسمه $x$ موجود في $A$). ثم استخدم المعطيات لتصل في النهاية إلى أن $x \in B$.
* إذا طلب إثبات $A = B$: ستقوم بعمل الإثبات مرتين. مرة تثبت أن $A \subseteq B$ ومرة تعكس وتثبت أن $B \subseteq A$.



#### 2. قالب الاستقراء الرياضي (Mathematical Induction)

* **متى تستخدمه؟** عندما يطلب منك إثبات معادلة تحتوي على $n$ (مثل جمع متسلسلة أو إثبات مقسومية).
* **النمط الثابت (كيف تبدأ؟):** هنا لا يوجد $x$. النمط يتكون من 3 خطوات ميكانيكية:
1. **Base Case:** عوض بـ $1$ لتثبت أن الطرفين متساويان (تدفع أول حجر دومينو).
2. **Assume:** اكتب نفس المعادلة كما هي بالضبط واستبدل كل $n$ بحرف $k$ وقل "دعنا نفترض أن هذا صحيح".
3. **Prove:** اكتب المعادلة واستبدل كل $n$ بـ $k+1$، واستخدم الفرضية السابقة للوصول للناتج.



#### 3. قالب العلاقات (Relation & POSET Proofs)

* **متى تستخدمه؟** عندما يطلب منك إثبات أن العلاقة Reflexive أو Symmetric أو أنها تمثل POSET.
* **النمط الثابت (كيف تبدأ؟):** هنا نستخدم أزواجاً مرتبة $(a,b)$ وليس $x$ منفرداً:
* لإثبات الـ Reflexive: ابدأ بـ **"Let $a \in A$"**، واكتب شرط العلاقة لتثبت أن $aRa$ يتحقق.
* لإثبات الـ Symmetric: ابدأ بـ **"Assume $(a,b) \in R$"** وحاول الوصول إلى أن $(b,a) \in R$.



#### 4. قالب المنطق (Logic & Proposition Proofs)

* **متى تستخدمه؟** عندما ترى $\rightarrow$ أو $\equiv$ أو يطلب منك إثبات التكافؤ (Equivalence).
* **النمط الثابت (كيف تبدأ؟):** هنا لا تفترض أي عناصر على الإطلاق. أنت تستخدم إما:
1. **Truth Table (جدول الحقيقة):** ترص الاحتمالات وتثبت أن العمود الأخير للطرف الأيمن يطابق العمود الأخير للطرف الأيسر.
2. **قوانين دي مورجان (De Morgan's):** تستخدم القوانين لتفكيك الأقواس والنفي خطوة بخطوة حتى تصل للطرف الآخر.



### نصيحة أخيرة للامتحان:

في أي مسألة إثبات، إذا توقفت ولم تعرف كيف تكمل، **اكتب المعطى والمطلوب والتعريف الرياضي لهما**. الدكتور يعطي درجات على "هيكلة الإثبات" (أنك تعرف من أين تبدأ وما هو هدفك) حتى لو أخطأت في خطوة جبرية في المنتصف.



---

### 1. Proof by Contradiction (إثبات بالتناقض)

**Question:**
Prove that if $A \subseteq B$, then $A - B = \emptyset$.

**Answer:**
**Proof (By Contradiction):**

1. Assume the opposite of the conclusion. Assume that $A - B \neq \emptyset$.
2. This means there exists at least one element $x$ such that $x \in (A - B)$.
3. By the definition of set difference, $x \in (A - B)$ implies that $x \in A$ **and** $x \notin B$.
4. However, the given premise is $A \subseteq B$. The definition of a subset states that if $x \in A$, it MUST be true that $x \in B$.
5. We have reached a logical contradiction: $x$ cannot be in $B$ and not in $B$ at the exact same time.
6. Since our assumption led to a contradiction, the original statement must be true. Therefore, $A - B = \emptyset$.

---

### 2. Proof of Set Equality using Subsets (إثبات التساوي بفك المجموعتين)

**Question:**
Consider the sets $A$ and $B$ where:
$A = \{a \in \mathbb{Z} \mid a = 2k, \text{ for some integer } k\}$
$B = \{b \in \mathbb{Z} \mid b = 2j - 2, \text{ for some integer } j\}$
Does $A = B$? If yes, prove it.

**Answer:**
**Yes, $A = B$.**
**Proof (To prove $A = B$, we must prove $A \subseteq B$ and $B \subseteq A$):**

**Part 1: Prove $A \subseteq B$**

1. Let $x \in A$. By the definition of set $A$, $x = 2k$ for some integer $k$.
2. We need to express this in the form of set $B$ ($2j - 2$). Let $k = j - 1$ (since $j$ and $k$ are arbitrary integers, we can map them).
3. Substitute $k$: $x = 2(j - 1) = 2j - 2$.
4. Since $x$ now perfectly matches the definition of $B$, $x \in B$. Thus, $A \subseteq B$.

**Part 2: Prove $B \subseteq A$**

1. Let $x \in B$. By the definition of set $B$, $x = 2j - 2$.
2. Factor out the 2: $x = 2(j - 1)$.
3. Let $k = j - 1$.
4. Substitute $k$: $x = 2k$.
5. Since $x$ now matches the definition of $A$, $x \in A$. Thus, $B \subseteq A$.
Conclusion: Since both are subsets of each other, $A = B$.

---

### 3. Proof of Intersection and Subsets (إثبات التقاطع)

**Question:**
Prove that for arbitrary sets $A$, $B$, and $C$, knowing that $A \subseteq B$ and $A \subseteq C$ implies that $A \subseteq B \cap C$.

**Answer:**
**Proof:**

1. Let $x$ be an arbitrary element in $A$ ($x \in A$).
2. Based on the given fact $A \subseteq B$, it must be true that $x \in B$.
3. Based on the given fact $A \subseteq C$, it must also be true that $x \in C$.
4. Since $x$ is present in $B$ **and** $x$ is present in $C$ simultaneously, by the definition of intersection, $x \in (B \cap C)$.
5. Therefore, $A \subseteq B \cap C$.

---

### 4. Proof of Cartesian Product Equality (إثبات حاصل الضرب الديكارتي)

**Question:**
Prove the following identity for arbitrary, nonempty sets: $A \times (B \cup C) = (A \times B) \cup (A \times C)$.

**Answer:**
**Proof (Showing both sides are subsets of each other. Note: We use ordered pairs $(x,y)$ instead of just $x$):**

**Part 1: Prove $LHS \subseteq RHS$**

1. Let $(x,y) \in A \times (B \cup C)$.
2. By the definition of Cartesian product, $x \in A$ and $y \in (B \cup C)$.
3. By the definition of union, $y \in (B \cup C)$ means $y \in B$ **or** $y \in C$.
4. If $y \in B$, then the pair $(x,y) \in A \times B$.
5. If $y \in C$, then the pair $(x,y) \in A \times C$.
6. In both logical branches, the pair belongs to either $A \times B$ or $A \times C$, which means $(x,y) \in (A \times B) \cup (A \times C)$.

**Part 2: Prove $RHS \subseteq LHS$**

1. Let $(x,y) \in (A \times B) \cup (A \times C)$.
2. By definition of union, $(x,y) \in A \times B$ **or** $(x,y) \in A \times C$.
3. In both cases, it is guaranteed that $x \in A$.
4. It is also guaranteed that $y \in B$ **or** $y \in C$, which implies $y \in (B \cup C)$.
5. Therefore, $(x,y) \in A \times (B \cup C)$.
Conclusion: Since both contain each other, $A \times (B \cup C) = (A \times B) \cup (A \times C)$.

---

### 5. Proof by Disjoint Sets (إثبات التقاطع الفارغ)

**Question:**
Prove that for any three arbitrary sets $A$, $B$, and $C$, if $C \subseteq B - A$, then $A \cap C = \emptyset$.

**Answer:**
**Proof (By Contradiction):**

1. Assume the opposite. Assume that $A \cap C \neq \emptyset$.
2. This implies there is at least one element $x$ such that $x \in (A \cap C)$.
3. By definition, this means $x \in A$ **and** $x \in C$.
4. We are given the premise that $C \subseteq B - A$. Since we established $x \in C$, it must follow that $x \in (B - A)$.
5. By the definition of set difference, $x \in (B - A)$ strictly means $x \in B$ **and** $x \notin A$.
6. We have a contradiction! In step 3, we said $x \in A$, but in step 5, we derived $x \notin A$.
7. Because our assumption caused a logical breakdown, the assumption is false. Therefore, $A \cap C = \emptyset$.

---

### 6. Algebraic Proof (الإثبات الجبري بقوانين التوزيع)

*ملاحظة: هذا الإثبات يمكن حله بطريقة $x \in \dots$، ولكن حله بقوانين التوزيع أسرع وأذكى برمجياً.*

**Question:**
Prove that if $A \cup B = U$ and $A \cap B = \emptyset$, then $(A \cup C) \cap (B \cup C) = C$.

**Answer:**
**Proof (Using Distributive Laws):**

1. Take the left-hand side (LHS): $(A \cup C) \cap (B \cup C)$.
2. Using the distributive law of sets backwards (factoring out the union of $C$), we can rewrite this as: $(A \cap B) \cup C$.
3. We are given the premise that $A \cap B = \emptyset$. Substitute this into the equation: $\emptyset \cup C$.
4. The union of any set with an empty set is the set itself (Identity Law). Therefore, $\emptyset \cup C = C$.
5. LHS = RHS. The statement is proven.

---

هل تلاحظ كيف أن النمط متكرر؟ مجرد تمرير الـ Variable وفك تعريفه باستخدام شروط المسألة. هل تريد أن ننتقل الآن إلى القالب الثاني ونقوم بحل كل مسائل **الاستقراء الرياضي (Mathematical Induction)** بنفس الطريقة؟
