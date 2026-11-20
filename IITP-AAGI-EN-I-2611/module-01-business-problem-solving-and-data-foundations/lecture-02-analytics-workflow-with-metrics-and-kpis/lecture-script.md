# <font color='#1d4ed8'>Lecture Script: Analytics Workflow with Metrics and KPIs</font>

---

## <font color='blue'>Agenda</font>

The lecture runs as four topics. Each topic ends with a quiz.

| Topic | What we do | Learning objectives covered | Minutes |
|:-:|:--|:--|:-:|
| 1 | Follow one request through the analytics workflow | Describe the stages of an analytics workflow from business question to communicated insight | 20 |
| 2 | Turn a vague request into a data question | Rewrite a vague business request as a question the data can answer | 25 |
| 3 | Separate metrics from KPIs and define one | Classify a measure as a metric or a KPI by whether it tracks a stated business objective<br>Write a metric definition stating numerator, denominator, population and time window | 30 |
| 4 | Set a KPI target and test a KPI | Write a KPI target stating the metric, a number and a date<br>Evaluate a proposed KPI against being measurable, attributable and timely | 30 |
| — | Closing: Outcome & Summary | | 15 |
| | **Total** | | **120** |

> <font color="red">**🎯 Instructor Note**</font> Pace: keep Topic 1 brisk, since it only names the stages. Spend the extra minutes on the four parts of a metric definition in Topic 3 and on the three KPI tests in Topic 4.
> No software is needed. Learners write their answers in chat or on paper.

---

## <font color='blue'>Scenario</font>

**Before and after.** A BigBasket-style grocery app in Bengaluru has one meeting and two very different outcomes.

| | Before the analysis | After the analysis |
|:--|:--|:--|
| What the head of operations says | "Customers seem unhappy. Fix delivery." | "Cut the late-delivery rate from 13% to 8% by 30 June 2026." |
| What the analyst can do with it | Nothing clear | Pull data, check weekly, report progress |

> <font color="red">**🎯 Instructor Note**</font> The company is only the setting. Do not claim it uses these numbers. All numbers are invented for teaching. March 2026 is the month being studied.

---

## <font color='blue'>Problem Statement</font>

Kavya is a data analyst. The head of operations tells her, "Customers seem unhappy. Fix delivery." Kavya opens a dashboard and builds a chart of average delivery time. Two weeks later she presents it. The head says, "That is not what I meant." Two weeks are gone, and nobody knows if delivery got better.

Last session you learned that a prompt works better with a clear task, context, format and constraints. A business request needs the same clarity before anyone touches data.

> <font color='purple'>**How do we turn "customers seem unhappy" into a question, a measure and a target that the whole team can check?**</font>

> <font color="red">**🎯 Instructor Note**</font> Poll: "Is 'average delivery time' a metric, a KPI, or both?" Give learners 30 seconds to respond in chat. Reveal the answer in the Closing.

---

## <font color='blue'>What We Will Use</font>

No software today. We use five ideas and one small table of March 2026 numbers.

| Topic | Ideas | In one line |
|:-:|:--|:--|
| 1 | Analytics workflow | Six stages from a business question to a message people act on |
| 2 | Data question | A question with a measure, a group and a time window |
| 3 | Metric, KPI, metric definition | A metric counts something. A KPI is a metric tied to a stated objective |
| 4 | KPI target, three tests | A KPI target has a metric, a number and a date. A good KPI is measurable, attributable and timely |

March 2026 numbers (invented for teaching): 4 weeks, 3,000 delivered orders per week, 240 cancelled orders in the month.

| Week | Delivered orders | Late orders | Late rate |
|:-:|:-:|:-:|:-:|
| 1 | 3,000 | 420 | $14\%$ |
| 2 | 3,000 | 360 | $12\%$ |
| 3 | 3,000 | 390 | $13\%$ |
| 4 | 3,000 | 390 | $13\%$ |
| **Month** | **12,000** | **1,560** | **$13\%$** |

---

## <font color='blue'>How: Walking Through Kavya's Request</font>

```mermaid
flowchart LR
    A["Topic 1<br>Workflow stages"] --> B["Topic 2<br>Vague request to question"]
    B --> C["Topic 3<br>Metric, KPI, definition"]
    C --> D["Topic 4<br>Target and KPI tests"]
    D --> E["Closing<br>One clear request"]
    style A fill:#dbeafe,stroke:#2563eb
    style B fill:#dcfce7,stroke:#16a34a
    style C fill:#fef3c7,stroke:#d97706
    style D fill:#ede9fe,stroke:#7c3aed
    style E fill:#fee2e2,stroke:#dc2626
```

---

## <font color='blue'>Topic 1: Follow one request through the analytics workflow</font> `20 min`

> <font color='purple'>**Where did Kavya's two weeks go?**</font>

### <font color='green'>Example: The six stages</font>

> <font color='purple'>**What stages should her work have gone through?**</font>

An **analytics workflow** is the path from a business question to an insight people can use. It has six stages.

```mermaid
flowchart LR
    S1["1. Business question"] --> S2["2. Data question"]
    S2 --> S3["3. Get and prepare data"]
    S3 --> S4["4. Analyse"]
    S4 --> S5["5. Insight"]
    S5 --> S6["6. Communicate"]
```

| Stage | What happens | Kavya's example |
|:-:|:--|:--|
| 1 | Name what the business wants | "Customers seem unhappy. Fix delivery." |
| 2 | Turn it into a question the data can answer | "What share of March orders arrived late?" |
| 3 | Get the data and clean it | Pull 12,000 delivered orders, drop 240 cancelled orders |
| 4 | Work out the numbers | 1,560 late orders out of 12,000 |
| 5 | Say what the numbers mean | 13% of orders are late, and the rate has not moved in 4 weeks |
| 6 | Share it so someone acts | One slide: "13% late. Target 8%." |

#### <font color='#c2410c'>Logic Explanation</font>

- **Stage 1 to 2** is where Kavya skipped ahead. She went from "unhappy customers" to a chart without choosing a question.
- **Stage 3** removes orders that never reached a customer. Cancelled orders cannot be late.
- **Stage 5 to 6** turns $\frac{1560}{12000} = 0.13$ into a sentence a manager can act on.

> <font color='green'>**Result**</font> Kavya's chart came from Stage 4 with no Stage 2. That is why her work missed the point.

<p align="center"><img src="images/01_weekly_late_rate.png" alt="Bar chart of the late-delivery rate for four weeks of March 2026: 14, 12, 13 and 13 percent" width="900"></p>

### <font color='green'>Extending it: Place each action in its stage</font>

> <font color='purple'>**Which stage is each action?**</font>

> <font color="red">**🎯 Instructor Note**</font> Read the three actions and ask learners to type a stage number. Expected: "Remove the 240 cancelled orders" is 3, "Present one slide to the head" is 6, "Decide the real question is about lateness" is 2.

> <font color='green'>**Result**</font> Every action belongs to one stage. If an action cannot be placed, the work has no clear question.

### <font color='purple'>Quiz 1</font>

**Question:** Which stage comes right after "Get and prepare data"?

**Options:**
- A) Business question
- B) Communicate
- C) Analyse
- D) Data question

**Correct Answer:** C

**Explanation:**
- **A)** The business question is Stage 1. It starts the workflow.
- **B)** Communicate is Stage 6, the last stage.
- **C)** Correct. Once the data is ready, you analyse it to get the numbers.
- **D)** The data question is Stage 2. It comes before the data is collected.

---

## <font color='blue'>Topic 2: Turn a vague request into a data question</font> `25 min`

> <font color='purple'>**Stage 2 was the missing stage. How do we do it?**</font>

### <font color='green'>Example: "Customers seem unhappy. Fix delivery."</font>

> <font color='purple'>**What is wrong with this request, and what question can the data answer?**</font>

A vague request hides four choices: which customers, which measure, compared with what, and over what time. A data question states all four.

| Part | Vague request | Data question |
|:--|:--|:--|
| Who | "Customers" | Delivered orders in Bengaluru |
| What | "Unhappy", "Fix delivery" | Orders delivered after the promised slot |
| Compared with | Nothing | Share of all delivered orders |
| When | Nothing | March 2026 |

> <font color='green'>**Result**</font> "What share of delivered Bengaluru orders in March 2026 arrived after the promised slot?" The answer is $\frac{1560}{12000} = 13\%$.

#### <font color='#c2410c'>Logic Explanation</font>

- The new question has a measure (late orders), a group (delivered Bengaluru orders), a base (all delivered orders) and a period (March 2026).
- Two analysts reading it will pull the same data and get the same number.

### <font color='green'>Extending it: Rewrite a second request</font>

> <font color='purple'>**"We should look at our best customers." What is the data question?**</font>

> <font color="red">**🎯 Instructor Note**</font> Ask learners to write their version in chat. Accept any version with the four parts. Sample: "Which 100 customers placed the most delivered orders between 1 January and 31 March 2026?"

> <font color='green'>**Result**</font> "Best" became a count of delivered orders, "customers" became 100 people, and "look at" became a ranked list for a stated period.

> <font color='#b45309'>**Common mistake**</font> Keeping words like "best", "unhappy" or "slow" in the question. Fix: replace each one with a count, a share or a time.

### <font color='purple'>Quiz 2</font>

**Question:** Which request is already a question the data can answer?

**Options:**
- A) "Improve the customer experience."
- B) "What share of Bengaluru orders in March 2026 used a coupon?"
- C) "Make delivery better."
- D) "Find out why people are leaving."

**Correct Answer:** B

**Explanation:**
- **A)** "Experience" has no measure, group or time.
- **B)** Correct. It names a share, a group (Bengaluru orders) and a period (March 2026).
- **C)** "Better" is not a number, and no period is given.
- **D)** "Leaving" and "why" are open. No measure or period is stated.

---

## <font color='blue'>Topic 3: Separate metrics from KPIs and define one</font> `30 min`

> <font color='purple'>**Kavya now asks the right question. Which number should the team watch?**</font>

### <font color='green'>Example: Metric or KPI?</font>

> <font color='purple'>**Which of these measures track the objective "Deliver groceries on time"?**</font>

A **metric** is any measure you can count. A **KPI** (key performance indicator) is a metric that tracks a stated business objective. The test is one question: which stated objective does this measure track?

| Measure | Tracks the objective "Deliver groceries on time"? | Metric or KPI |
|:--|:-:|:-:|
| Orders per week | No | Metric |
| Average basket value | No | Metric |
| Late-delivery rate | Yes | KPI |
| App opens per day | No | Metric |

> <font color='green'>**Result**</font> All four are metrics. Only the late-delivery rate is also a KPI for this objective.

> <font color="red">**🎯 Instructor Note**</font> This sets up the poll. "Average delivery time" tracks "Deliver groceries on time" only if the objective says so. Do not reveal the poll answer yet.

### <font color='green'>Extending it: Write the metric definition</font>

> <font color='purple'>**What exactly is "late-delivery rate"?**</font>

A metric definition has four parts, and each one removes a disagreement.

$$\boxed{ \text{late-delivery rate} = \frac{\text{orders delivered after the promised slot}}{\text{all delivered orders}} }$$

| Part | Late-delivery rate |
|:--|:--|
| Numerator | Orders delivered after the end of the promised slot |
| Denominator | All delivered orders |
| Population | Bengaluru orders, cancelled orders excluded |
| Time window | One calendar week, Monday to Sunday |

For March 2026: $\frac{1560}{12000} = 13.0\%$.

> <font color='green'>**Result**</font> With these four parts, any analyst gets the same 13.0%.

### <font color='green'>Extending it: See what a loose definition does</font>

> <font color='purple'>**What if one analyst keeps the 240 cancelled orders in the denominator?**</font>

> <font color="red">**🎯 Instructor Note**</font> Ask for a prediction first. Expected: a smaller rate. The same 1,560 late orders are divided by a bigger base.

$$\frac{1560}{12000 + 240} = \frac{1560}{12240} \approx 12.7\%$$

> <font color='green'>**Result**</font> The same orders give 13.0% or 12.7%, depending on the population. The definition decides the number.

<p align="center"><img src="images/02_two_denominators.png" alt="Bar chart comparing 13.0 percent with delivered orders only and 12.7 percent when cancelled orders are included" width="900"></p>

> <font color='#b45309'>**Common mistake**</font> Leaving out the population or the time window. Fix: write all four parts before sharing the number.

### <font color='purple'>Quiz 3</font>

**Question:** Which part of a metric definition says "delivered Bengaluru orders, cancelled orders excluded"?

**Options:**
- A) Numerator
- B) Denominator only
- C) Time window
- D) Population

**Correct Answer:** D

**Explanation:**
- **A)** The numerator is the count on top, here the late orders.
- **B)** The denominator is the base count. The population says which orders are allowed into both counts.
- **C)** The time window is the period, such as one calendar week.
- **D)** Correct. The population says who or what is included.

---

## <font color='blue'>Topic 4: Set a KPI target and test a KPI</font> `30 min`

> <font color='purple'>**The KPI is chosen. How do we say how much it has to improve, and is it the right KPI?**</font>

### <font color='green'>Example: Write the KPI target</font>

> <font color='purple'>**What does "fix delivery" become as a target?**</font>

A **KPI target** has three parts: the metric, a number and a date.

| Part | Example |
|:--|:--|
| Metric | Weekly late-delivery rate |
| Number | 8% (from 13%) |
| Date | 30 June 2026 |

"Reduce the weekly late-delivery rate from 13% to 8% by 30 June 2026."

The gap is $13\% - 8\% = 5$ percentage points.

> <font color='green'>**Result**</font> Anyone can check this target on 30 June 2026 against one number.

<p align="center"><img src="images/04_kpi_target.png" alt="Bar chart showing the current 13 percent late rate and the 8 percent target for 30 June 2026" width="900"></p>

### <font color='green'>Extending it: Test four proposed KPIs</font>

> <font color='purple'>**Which proposed KPIs pass the three tests: measurable, attributable and timely?**</font>

**Measurable** means a number can be calculated from data you have. **Attributable** means the team being judged can change it. **Timely** means the number arrives often enough to act on.

> <font color="red">**🎯 Instructor Note**</font> Fixed facts for the exercise: there is no agreed survey question for "happiness". The survey runs once a quarter. Revenue is reported once a year. The delivery team does not run app marketing.

| Proposed KPI | Measurable | Attributable | Timely | Why |
|:--|:-:|:-:|:-:|:--|
| Weekly late-delivery rate | Yes | Yes | Yes | Counted from orders, driven by delivery, available every week |
| Customer happiness | No | No | No | No agreed question, many causes, quarterly survey |
| App downloads | Yes | No | Yes | Counted daily, but delivery does not drive downloads |
| Annual revenue | Yes | No | No | Many teams drive it, and it arrives once a year |

> <font color='green'>**Result**</font> Only the weekly late-delivery rate passes all three tests.

<p align="center"><img src="images/03_kpi_tests.png" alt="Table of four proposed KPIs against the three tests, with only weekly late-delivery rate passing all three" width="900"></p>

> <font color='#b45309'>**Common mistake**</font> Picking a KPI because it is easy to find on a dashboard. Fix: run the three tests first.

### <font color='purple'>Quiz 4</font>

**Question:** Which is a complete KPI target?

**Options:**
- A) Reduce the weekly late-delivery rate from 13% to 8% by 30 June 2026
- B) Improve the late-delivery rate
- C) Reach 8% late deliveries
- D) Late-delivery rate by 30 June 2026

**Correct Answer:** A

**Explanation:**
- **A)** Correct. It has the metric, a number (8%) and a date (30 June 2026).
- **B)** It names the metric but gives no number and no date.
- **C)** It has a number but no date, and "late deliveries" is not a defined metric.
- **D)** It has a metric and a date but no number to reach.

---

## <font color='blue'>Closing: Outcome & Summary</font> `15 min`

Back to Kavya. We answer the Problem Statement using each topic once.

> <font color='purple'>**1. Which stages was Kavya missing? (Topic 1)**</font>

Stage 2. She went from the business question straight to analysis.

> <font color='purple'>**2. What is the data question? (Topic 2)**</font>

"What share of delivered Bengaluru orders in March 2026 arrived after the promised slot?"

> <font color='purple'>**3. What is the KPI and how is it defined? (Topic 3)**</font>

The late-delivery rate: late delivered orders divided by all delivered orders, Bengaluru, cancelled excluded, per calendar week. March 2026 gives $\frac{1560}{12000} = 13\%$.

> <font color='purple'>**4. What is the target and does the KPI pass? (Topic 4)**</font>

Reduce the weekly late-delivery rate from 13% to 8% by 30 June 2026. The KPI is measurable, attributable and timely.

### <font color='green'>Outcome</font>

| | Kavya's first request | Kavya's final request |
|:--|:--|:--|
| Question | "Customers seem unhappy" | Share of late delivered orders, March 2026 |
| Measure | Average delivery time (unstated objective) | Weekly late-delivery rate |
| Target | None | 8% by 30 June 2026 |
| Can the team check it? | No | Yes |

> <font color='green'>**Therefore,**</font> A request becomes useful once it has a data question, a defined KPI and a target with a number and a date. Kavya can now start work, and the head of operations can check progress weekly.

> <font color="red">**🎯 Instructor Note**</font> Reveal the poll: average delivery time is a metric. It becomes a KPI only if the stated objective is about delivery time. Here the objective is "on time", so the late-delivery rate is the KPI.

### <font color='green'>Summary</font>

| Learning objective | Takeaway |
|:--|:--|
| Analytics workflow | Six stages from business question to communicated insight |
| Rewrite a vague request | Replace each vague word with a measure, a group, a base and a period |
| Metric or KPI | A KPI is a metric that tracks a stated business objective |
| Metric definition | Numerator, denominator, population and time window |
| KPI target | Metric, a number and a date |
| Evaluate a KPI | Measurable, attributable and timely |
| **Practical value** | Every request you receive at work can be turned into a question, a KPI and a target before you open any data |

---

# <font color='red'>Launch the Feedback Poll</font>

> <font color="red">**🎯 Instructor Note**</font> Reminder: launch the feedback poll now to collect learner feedback.
