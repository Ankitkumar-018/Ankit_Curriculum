# <font color='#1d4ed8'>Lecture Script: Where LLMs Work and Fail</font>

---

## <font color='blue'>Agenda</font>

The lecture runs as four topics. Each topic ends with a quiz.

| Topic | What we do | Learning objectives covered | Minutes |
|:-:|:--|:--|:-:|
| 1 | Choose between hosted and open-weight models | Compare open-weight and proprietary hosted models on cost, control and deployment | 25 |
| 2 | Choose between a reasoning model and a standard chat model | Compare a reasoning model with a standard chat model on latency, cost and task fit | 25 |
| 3 | See what a model can read and why it can be wrong | Describe the input types a multimodal model accepts beyond text<br>Explain why a model can produce fluent text that is factually wrong | 30 |
| 4 | Sort tasks into reliable and unreliable | Classify tasks as reliable or unreliable for a hosted LLM without external tools | 25 |
| — | Closing: Outcome & Summary | | 15 |
| | **Total** | | **120** |

> <font color="red">**🎯 Instructor Note**</font> Pace: Topic 3 carries two ideas, so keep the input-type part short and spend the time on fluent but wrong answers. Learners need one free chat tool open: ChatGPT, Claude or Gemini.
> Costs, speeds and token counts are invented for teaching, because real prices and limits change. Model replies are never pasted here. Run each live step and read the real reply.

---

## <font color='blue'>Scenario</font>

**Five decisions on one whiteboard.** Ishaan leads the support team of an IRCTC-style train ticket app. He wants an AI helper for refund questions, and the whiteboard has five decisions.

1. Which kind of model: a hosted one or an open-weight one?
2. Which model for which question: a reasoning model or a standard chat model?
3. Can the helper read a photo of a damaged ticket?
4. What if the helper states a refund rule that does not exist?
5. Which tasks should the helper never do alone?

> <font color="red">**🎯 Instructor Note**</font> The company is only the setting. Do not claim it works this way. The team, the costs, the timings and the bill are invented for teaching. Today is Monday, 2 November 2026.

---

## <font color='blue'>Problem Statement</font>

Ishaan picks the "most powerful" setup for everything. He routes all chats, with passenger IDs, to a hosted model. He uses a slow, costly reasoning model for simple opening-hours questions. Then the helper tells a passenger, in perfect English, that a ticket cancelled 4 hours before departure gets a 50% refund. No such rule exists. The passenger claims it, and the team must pay or explain.

You know that a model predicts the next token, that its training has a cutoff date, and that fluent text can be false. Today we place these ideas into design choices.

> <font color='purple'>**How should Ishaan choose a model type, match models to questions, understand what the helper can read, and decide which tasks to trust it with?**</font>

> <font color="red">**🎯 Instructor Note**</font> Poll: "If an answer is fluent and confident, is it more likely to be correct?" Options: yes or no. Give learners 30 seconds to respond in chat. Reveal the answer in the Closing.

---

## <font color='blue'>What We Will Use</font>

A decision table for each topic and one free chat tool for the live checks. Where a topic uses numbers, they are invented for teaching.

| Topic | Ideas | In one line |
|:-:|:--|:--|
| 1 | Open-weight and hosted models | Compare cost, control and deployment |
| 2 | Reasoning and standard chat models | Compare latency, cost and task fit |
| 3 | Multimodal input, fluent but wrong text | See what a model can read, and why a smooth answer can be false |
| 4 | Reliable and unreliable tasks | Sort tasks for a model with no search, calculator or files |

---

## <font color='blue'>How: Walking Through Ishaan's Whiteboard</font>

```mermaid
flowchart LR
    A["Topic 1<br>Hosted or open-weight"] --> B["Topic 2<br>Reasoning or standard"]
    B --> C["Topic 3<br>Inputs, and fluent but wrong"]
    C --> D["Topic 4<br>Reliable and unreliable tasks"]
    D --> E["Closing<br>A safe design for the helper"]
    style A fill:#dbeafe,stroke:#2563eb
    style B fill:#dcfce7,stroke:#16a34a
    style C fill:#fef3c7,stroke:#d97706
    style D fill:#ede9fe,stroke:#7c3aed
    style E fill:#fee2e2,stroke:#dc2626
```

---

## <font color='blue'>Topic 1: Choose between hosted and open-weight models</font> `25 min`

> <font color='purple'>**Ishaan's data includes passenger IDs. Who runs the model, and who pays for what?**</font>

### <font color='green'>Example: Three comparison points</font>

> <font color='purple'>**How do hosted and open-weight models differ on cost, control and deployment?**</font>

A **proprietary hosted model** is run by its provider. You reach it through the provider's app or a web service, and you do not get its weights. An **open-weight model** publishes its weights for download under a licence, so you can run it on machines you choose. Read the licence, because terms differ.

| | Proprietary hosted model | Open-weight model |
|:--|:--|:--|
| Cost | Pay per use or by subscription. No hardware to buy | No per-call fee to the model maker under many licences. You pay for hardware, hosting and staff time |
| Control | Provider sets the version, updates and filters. Your data travels to its servers under its terms | You choose the version, can adapt it and can keep data on your own machines. You also own the safety work |
| Deployment | Call it over the internet from any device | Run it on your own or rented machines, including without internet. Setup and upkeep are yours |

> <font color="red">**🎯 Instructor Note**</font> Ask learners which row matters most for passenger IDs. Expected: control, because the data can stay inside the company. Ask what the licence might limit. Expected: some uses or user counts.

> <font color='green'>**Result**</font> Hosted is easy to start and costs by use. Open-weight gives control and costs by running it yourself.

### <font color='green'>Extending it: When does a fixed cost win?</font>

> <font color='purple'>**At what volume does running your own server cost less than paying per request?**</font>

Suppose a hosted model costs Rs 0.40 per request, and an own server costs a fixed Rs 55,000 a month (both invented for teaching, and the server cost includes upkeep).

$$\boxed{ \text{break-even requests} = \frac{\text{fixed monthly cost}}{\text{cost per request}} = \frac{55000}{0.40} = 137{,}500 }$$

At 50,000 requests, hosted costs $50000 \times 0.40 = 20{,}000$ rupees. At 200,000 requests, it costs $200000 \times 0.40 = 80{,}000$ rupees, which is more than 55,000.

<p align="center"><img src="images/01_hosted_vs_own_cost.png" alt="Line chart of monthly cost: hosted rises with requests at Rs 0.40 each, own server stays at Rs 55,000, and they cross at 137,500 requests" width="900"></p>

> <font color="red">**🎯 Instructor Note**</font> Remind learners the numbers are invented, and that real prices change. The lesson is the shape: pay-per-use rises, a fixed cost is flat.

> <font color='green'>**Result**</font> Below 137,500 requests a month, hosted costs less. Above it, the own server costs less, if the team can run it.

> <font color='#b45309'>**Common mistake**</font> Calling open-weight models free. Fix: count hardware, hosting and the time of the people who run it.

### <font color='purple'>Quiz 1</font>

**Question:** A firm must keep customer chats on its own servers. It has the budget for hardware and staff. Which option fits best?

**Options:**
- A) A hosted model, because it needs no hardware
- B) An open-weight model run on its own servers
- C) Either one, because control does not matter
- D) Neither, because models cannot run on a server

**Correct Answer:** B

**Explanation:**
- **A)** Hosted models send data to the provider's servers.
- **B)** Correct. It gives control over where the data lives, at the cost of running it.
- **C)** Control over data location is the main requirement here.
- **D)** Open-weight models run on machines you choose.

---

## <font color='blue'>Topic 2: Choose between a reasoning model and a standard chat model</font> `25 min`

> <font color='purple'>**The model type is chosen. Does every question need the same kind of model?**</font>

### <font color='green'>Example: Same question, two models</font>

> <font color='purple'>**How do a reasoning model and a standard chat model differ on latency, cost and task fit?**</font>

A **standard chat model** replies directly. A **reasoning model** spends extra tokens working through the problem before it answers. That makes it slower and costlier per answer, and often better at multi-step problems. Many tools offer both, so check the tool's model picker.

Suppose both models answer one refund-rule question, with invented numbers.

| | Standard chat model | Reasoning model |
|:--|:-:|:-:|
| Time to answer | 2 s | 14 s |
| Tokens used | 300 | 2,100 |
| Cost at Rs 0.50 per 1,000 tokens | Rs 0.15 | Rs 1.05 |

$$\text{cost} = \frac{\text{tokens}}{1000} \times 0.50: \quad \frac{300}{1000} \times 0.50 = 0.15, \qquad \frac{2100}{1000} \times 0.50 = 1.05$$

The reasoning model is $\frac{2100}{300} = 7$ times the tokens, 7 times the cost and 7 times the wait.

<p align="center"><img src="images/02_reasoning_vs_standard.png" alt="Two bar charts: time to answer is 2 seconds for the standard model and 14 seconds for the reasoning model; cost per answer is Rs 0.15 and Rs 1.05" width="900"></p>

> <font color="red">**🎯 Instructor Note**</font> Learners may try the same 3-condition question in two models if their tool offers both. Say that the numbers above are invented, and ask them to note the real wait for the two replies.

> <font color='green'>**Result**</font> A reasoning model costs more time and money per answer, so use it where the extra thinking pays off.

### <font color='green'>Extending it: Match the question to the model</font>

> <font color='purple'>**Which questions deserve the reasoning model?**</font>

| Question | Better fit | Why |
|:--|:--|:--|
| "What are the opening hours of the helpline?" | Standard chat model | One lookup in pasted text, no steps |
| "Rewrite this reply politely." | Standard chat model | Wording only |
| "A booking has 2 tickets, one confirmed and one waitlisted, cancelled 6 hours before departure. Work out the refund using the pasted refund rule." | Reasoning model | Several conditions combine |

For 10,000 simple FAQ questions a month, the standard model costs $10000 \times 0.15 = 1{,}500$ rupees and the reasoning model costs $10000 \times 1.05 = 10{,}500$ rupees in these invented numbers.

> <font color="red">**🎯 Instructor Note**</font> Ask learners to sort 2 more questions of their own into the table. Expected: multi-condition rules and maths go to reasoning, wording and lookups go to standard.

> <font color='green'>**Result**</font> Use the standard model for simple questions, and the reasoning model for multi-step work. You still check the answer in both cases.

> <font color='#b45309'>**Common mistake**</font> Assuming a reasoning model never errs. Fix: it can still be fluent and wrong, so check its result.

### <font color='purple'>Quiz 2</font>

**Question:** Ishaan must answer 10,000 simple opening-hours questions a month. Which choice fits?

**Options:**
- A) The reasoning model, because it is always better
- B) The reasoning model, because it is faster
- C) Either, because cost does not change
- D) The standard chat model, because it is quicker and costs less per answer

**Correct Answer:** D

**Explanation:**
- **A)** "Always better" is wrong. Simple questions do not need extra steps.
- **B)** It is slower, not faster, in the invented numbers.
- **C)** Cost differs: Rs 1,500 against Rs 10,500 for 10,000 answers.
- **D)** Correct. Simple lookups do not need extra thinking, so the cheaper and faster model fits.

---

## <font color='blue'>Topic 3: See what a model can read and why it can be wrong</font> `30 min`

> <font color='purple'>**A passenger sends a photo of a damaged ticket. Can the helper read it, and can it still be wrong?**</font>

### <font color='green'>Example: Input types beyond text</font>

> <font color='purple'>**Which input types does a multimodal model accept besides text?**</font>

A **multimodal model** accepts more than one type of input. Beyond text, models may accept images, audio, video and documents such as PDFs. Which types a particular tool takes depends on the tool, so check its attach button.

| Input type | Ishaan's example |
|:--|:--|
| Image | A photo of a damaged ticket |
| Audio | A voice note from a passenger |
| Video | A short clip of a faulty ticket machine |
| Document | A scanned PDF of a refund form |

Here is an invented sample bill. Learners save the image and attach it to their tool.

<p align="center"><img src="images/03_sample_bill.png" alt="Invented sample restaurant bill: Veg Thali 2 at 180 is 360, Masala Chai 3 at 25 is 75, Gulab Jamun 1 at 60 is 60, subtotal 495.00, GST 5 percent 24.75, total 519.75" width="900"></p>

> <font color="red">**🎯 Instructor Note**</font> Learners ask: "List each item, quantity, price and the total on this bill." Compare with the bill. Expected key: items total $360 + 75 + 60 = 495$, GST $495 \times 0.05 = 24.75$, total 519.75. If the tool has no image option, describe the bill in words instead.

> <font color='green'>**Result**</font> A multimodal model can read an image, but you still compare what it read with the original.

### <font color='green'>Extending it: Why fluent text can be false</font>

> <font color='purple'>**Why would the helper state a refund rule that does not exist?**</font>

A model writes the most likely next tokens. It does not look a fact up, and it has no built-in check for truth. Four causes lead to smooth but false text.

| Cause | Plain meaning |
|:--|:--|
| Trained to sound plausible | The goal is likely-sounding text, not verified text |
| No lookup | A rule is produced from patterns, not read from the rule book |
| Rare or recent facts | Facts seen rarely, or after the cutoff, are weak or missing |
| False premise in the prompt | A question that assumes a made-up fact often gets an answer that accepts it |

> <font color="red">**🎯 Instructor Note**</font> Live step: ask the tool, "What is the 50% refund rule for tickets cancelled 4 hours before departure?" The rule is invented. Read the reply and ask if it accepted the premise.

> <font color='green'>**Result**</font> Fluent does not mean true. A confident reply to a question with a false premise is a warning sign.

> <font color='#b45309'>**Common mistake**</font> Treating tone as evidence. Fix: ask for the rule's source, and check it in the official rule book.

### <font color='purple'>Quiz 3</font>

**Question:** The helper states a refund rule that does not exist, in smooth language. Why can that happen?

**Options:**
- A) It generates likely-sounding text and has no built-in fact check
- B) It always copies rules from the official rule book
- C) Smooth language proves the rule is real
- D) Models cannot write about refunds

**Correct Answer:** A

**Explanation:**
- **A)** Correct. A model predicts plausible tokens and does not verify them.
- **B)** It does not read the rule book unless you supply it.
- **C)** Smooth language and truth are separate.
- **D)** Models can write about refunds, and that is the problem when they write wrongly.

---

## <font color='blue'>Topic 4: Sort tasks into reliable and unreliable</font> `25 min`

> <font color='purple'>**Ishaan now knows the model's limits. Which tasks can the helper do alone?**</font>

### <font color='green'>Example: Eight tasks, two groups</font>

> <font color='purple'>**Which tasks are reliable, and which are unreliable, for a hosted model with no search, calculator or files?**</font>

"Without external tools" means the model has only its training and what you paste into the chat. A task is **reliable** when the answer depends on the text you supplied or on wording. It is **unreliable** when it needs live facts, exact long calculations, sources or letter-level work.

> <font color="red">**🎯 Instructor Note**</font> Cover the last two columns. Ask learners to sort each task in chat, then reveal. Expected: 1 to 4 reliable, 5 to 8 unreliable.

| # | Task | Verdict | Why |
|:-:|:--|:--|:--|
| 1 | Rewrite a pasted refund reply in a polite tone | Reliable | Wording of supplied text |
| 2 | Summarise a pasted 200-word policy into 3 bullets | Reliable | Answer comes from the pasted text |
| 3 | Explain "waitlist" in simple words | Reliable | A well-known concept, but read the answer |
| 4 | Brainstorm 10 subject lines for a reminder | Reliable | No fact needs to be right |
| 5 | Give the live waiting-list status of a named train | Unreliable | Needs live data the model does not have |
| 6 | Multiply 48,371 by 6,294 exactly | Unreliable | Long arithmetic needs a calculator. The true product is 304,447,074 |
| 7 | Quote the current refund rule with its page number | Unreliable | No source, and the rule may be newer than the cutoff |
| 8 | Count the letter "r" in "extraordinarily irregular timetable" | Unreliable | Models see tokens, not letters. The true count is 6 |

<p align="center"><img src="images/04_task_reliability.png" alt="Bar chart of eight tasks sorted: 4 reliable without tools and 4 unreliable without tools" width="900"></p>

#### <font color='#c2410c'>Logic Explanation</font>

- A reliable task still needs a read-through. "Reliable" means the risk is low, not zero.
- For each unreliable task, the fix is a tool or a source: a search, a calculator or the real rule book.
- $48371 \times 6294 = 304{,}447{,}074$, computed in Python as the answer key.

> <font color='green'>**Result**</font> Four tasks are fit for the helper alone, with a read-through. Four need a tool or a human with a source.

### <font color='green'>Extending it: Test one unreliable task live</font>

> <font color='purple'>**What happens when we ask the multiplication in task 6?**</font>

> <font color="red">**🎯 Instructor Note**</font> Learners ask the question in their tool and compare with 304,447,074. Some tools run a calculator behind the scenes, so say which behaviour you saw. Read the reply before judging.

> <font color='green'>**Result**</font> Compare the reply with the key. A wrong or unchecked answer shows why long arithmetic needs a calculator.

> <font color='#b45309'>**Common mistake**</font> Judging a task from one lucky reply. Fix: classify by what the task needs, not by one result.

### <font color='purple'>Quiz 4</font>

**Question:** Which task is reliable for a hosted model with no external tools?

**Options:**
- A) Giving today's seat availability on a named train
- B) Multiplying two 5-digit numbers exactly
- C) Summarising a pasted 200-word policy into 3 bullets
- D) Quoting the current rule with its page number

**Correct Answer:** C

**Explanation:**
- **A)** Needs live data the model does not have.
- **B)** Long exact arithmetic needs a calculator.
- **C)** Correct. The answer comes from text you supplied.
- **D)** Needs a source, and the rule may be newer than the cutoff.

---

## <font color='blue'>Closing: Outcome & Summary</font> `15 min`

Back to Ishaan. We answer the Problem Statement using each topic once.

> <font color='purple'>**1. Hosted or open-weight? (Topic 1)**</font>

For passenger IDs, control matters, so he considers an open-weight model run on his own servers. Below 137,500 requests a month in the invented numbers, hosted costs less. He compares cost, control and deployment, not only price.

> <font color='purple'>**2. Reasoning or standard? (Topic 2)**</font>

Simple FAQs go to the standard model at Rs 0.15 an answer. Multi-condition refund rules go to the reasoning model at Rs 1.05, and a person checks the result.

> <font color='purple'>**3. What can the helper read, and why was it wrong? (Topic 3)**</font>

A multimodal model can take images, audio, video and documents, and he compares what it read with the original. The invented 50% rule came from plausible text, with no lookup and no check.

> <font color='purple'>**4. What can it do alone? (Topic 4)**</font>

Wording and summaries of pasted text, with a read-through. Live status, exact sums and rule citations need a tool or the real rule book.

### <font color='green'>Outcome</font>

| | "Most powerful for everything" | Matched design |
|:--|:-:|:-:|
| Model for passenger IDs | Hosted, all chats | Chosen on control, cost and deployment |
| Opening-hours questions | Reasoning model, Rs 1.05 each | Standard model, Rs 0.15 each |
| Refund rule in a reply | Invented rule, sent as fact | Sourced from the rule book |
| Long sums and live status | Asked of the model | Calculator and live system |

> <font color='green'>**Therefore,**</font> Ishaan should pick the model type by cost, control and deployment, give each question the cheapest model that fits, treat smooth text as unverified, and keep live facts, long sums and rule citations out of the helper's solo tasks.

> <font color="red">**🎯 Instructor Note**</font> Reveal the poll: no. Fluent tone and correctness are separate, which is why every refund rule is checked against the rule book.

### <font color='green'>Summary</font>

| Learning objective | Takeaway |
|:--|:--|
| Open-weight and hosted models | Hosted is easy and pay-per-use. Open-weight gives control and costs running it |
| Reasoning and standard models | Reasoning costs more time and money. Use it for multi-step work |
| Multimodal input | Text, images, audio, video and documents, depending on the tool |
| Fluent but wrong text | Models predict plausible text and do not verify it |
| Reliable and unreliable tasks | Reliable: supplied text and wording. Unreliable: live data, long sums, sources, letters |
| **Practical value** | You can choose a model, give it work that suits it, and know when to check or hand the task to a tool |

---

# <font color='red'>Launch the Feedback Poll</font>

> <font color="red">**🎯 Instructor Note**</font> Reminder: launch the feedback poll now to collect learner feedback.
