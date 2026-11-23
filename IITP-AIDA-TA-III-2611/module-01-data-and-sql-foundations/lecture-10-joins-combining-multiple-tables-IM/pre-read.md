## <span style="color:#2F7DDE">Joins: Combining Multiple Tables</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Joins: Combining Multiple Tables"]
  Q["<b>The Big Question</b><br/><i>How do we combine tables without losing the rows that matter?</i>"]
  CV["<b>Course use case</b><br/>Sellers, products and orders joined across 3 tables, where an inner join hid 3 sellers and 8 orders"]
  RL["<b>Real-world example</b><br/>A school clubs roster built from a student list, a membership list and a club list"]

  CUR ==> Q
  Q ==>|&nbsp;Used in the course&nbsp;| CV
  Q ==>|&nbsp;Seen in real life&nbsp;| RL

  classDef currSes fill:#ffe0b2,stroke:#ef6c00,color:#4e342e,stroke-width:3px
  classDef ask fill:#e3f2fd,stroke:#1565c0,color:#0d47a1,stroke-width:3px
  classDef val fill:#e8f5e9,stroke:#2e7d32,color:#1b5e20

  class CUR currSes
  class Q ask
  class CV,RL val

  linkStyle default stroke-width:3px
```

---

### <span style="color:#2F7DDE">What You'll Learn</span>

Have you ever wondered how a school finds every student who has not joined any club?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Identify**</span> the roll number that links the student list to the membership list.
- <span style="color:#D9660B">**Predict**</span> the number of lines in a combined list when one student joins 2 clubs.
- <span style="color:#D9660B">**Compare**</span> a list that keeps every student with a list that keeps only students in a club.
- <span style="color:#D9660B">**Examine**</span> a diagram of three lists to find which links a question needs.
- <span style="color:#D9660B">**Build**</span> a list of students with no club, using the student, membership and club lists.
- <span style="color:#D9660B">**Justify**</span> which way of combining fits a report, by the rows that must stay.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> keys, INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL JOIN, row counts, three tables.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Mr. Menon coordinates clubs at his school. He has three lists: students, memberships and clubs. He combines the student list with the membership list and keeps only matches. His new list shows 22 students. The school has 25. Three students joined no club and vanished from the list.

A <span style="color:#D9660B">**join**</span> means a way to combine two lists by matching a shared value, such as a roll number.

In this course, you will join tables on a key and pick the join that keeps the right rows.

> <span style="color:#2F7DDE">**Think about it:**</span> Which rule for combining the lists made three students disappear?

---

### <span style="color:#2F7DDE">The School Clubs Roster Puzzle</span>

Here are small pieces of the three lists.

| List | What it holds | Link |
|:----------:|:----------:|:----------:|
| Students | Roll number, name | Roll number |
| Memberships | Roll number, club number | Roll number and club number |
| Clubs | Club number, club name | Club number |

<span style="color:#D9660B">**What you want to happen:**</span>

- Mr. Menon sees every student, with the club if there is one.
- Mr. Menon lists only the students who have no club.
- Mr. Menon links students to club names through the membership list.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - What happens to a student with no membership when only matches are kept?
> - If Asha joins 2 clubs, does she appear once or twice?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. The school has 25 students and 3 have no club. What count of students do you see when you keep only matches?**
Hint: Remove the students with no partner.

**2. Ravi is in the Chess club and the Art club. What is the count of lines Ravi gives in the combined list?**
Hint: Count the matches for his roll number.

**3. To print a club name next to a student, which two links must you follow?**
Hint: Student to membership, then membership to club.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How does the choice of join decide which rows survive?**</span>
>
> Which list would you keep whole if you had to find students with no club?
