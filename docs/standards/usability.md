---
title: Usability standards
description: Health NZ usability standards, set out in the order you do the work. Includes the questions to ask and AI prompts to create or update a usability test script.
---

# Usability standards

> **About this page**
> We're working with the Health NZ Standards team on how to apply the ISO 9241 international usability standards. Work in progress.

These standards are for anyone delivering a digital product or service at Health NZ. Use them to plan, run and report a usability test before go-live.

**Usability** is the extent to which a system, product or service can be used by specified users to achieve specified goals with effectiveness, efficiency and satisfaction in a specified context of use. In other words:

| Measure | Question | How we measure it |
|---|---|---|
| Effectiveness | **Can people do it?** | Task completion and accuracy |
| Efficiency | **How much effort does it take?** | Time on task, number of clicks, effort (ease rating) |
| Satisfaction | **How does it feel?** | Satisfaction rating |

Usability is affected by:

- **the users**: who are they
- **their goals**: what are they trying to do, or the intended outcome
- **their usage situation** ("context of use"): where and how they use it

---

## The minimum

1. Test with **real end users**, not just the project team, **before go-live**.
2. Test the **tasks people do most often** and the **tasks that must go right**.
3. Write each task as a **real situation** that doesn't give away the answer.
4. Report results against your **[success criteria](#1-decide-what-to-test)**.
5. **Fix** anything that misses a target before go-live, or **record why not**.

---

## Key terms

| Term | What it means |
|---|---|
| **End user** | The person who will actually use the product day to day. |
| **Participant** | An end user who takes part in a test. |
| **Subject matter expert** | Someone with deep knowledge of the work or process. They may not be an end user. |
| **Facilitator** | The person running the test session. |

---

## The standards

**MUST** = required. **SHOULD** = expected unless you have a good reason not to.

On every rating scale, **1 = bad and 5 = good**.

### 1. Decide what to test

| # | Standard | Level |
|---|---|---|
| 1.1 | Identify **who will use it** (the end users), for example identify specific role types or job titles. | MUST |
| 1.2 | Describe **where they'll use it**, for example in the office, remotely, in front of consumers, on a laptop. | MUST |
| 1.3 | List the tasks to test:<br>• the **tasks people do most often** (high frequency), for example logging in, finding a case or adding a case note<br>• the **tasks that must go right** (most important), even if they're not high frequency, for example escalating a high-risk case | MUST |
| 1.4 | If it **replaces a system or process**, note what people use now, for example an old system or systems, a spreadsheet or a paper form. | MUST |
| 1.5 | **Define success criteria** for the tasks and ratings. For example:<br>• at least 4 of 5 participants (80%) complete a task done most often without help<br>• an average satisfaction rating of 3 or above | MUST |
| 1.6 | Plan to test **before go-live**. | MUST |
| 1.7 | Plan to test again **after any big change**, for example a new workflow, a redesigned screen or a new group of users. | SHOULD |
| 1.8 | Plan a separate walkthrough with **managers and/or subject matter experts**. Their views add to end-user testing; they don't replace it. A subject matter expert who uses the product can take part as an end user. | MUST |

### 2. Set up the test

| # | Standard | Level |
|---|---|---|
| 2.1 | Recruit **end users**, not just the project team. | MUST |
| 2.2 | Recruit a **mix of participants** (one person can cover several of these):<br>• new users (MUST)<br>• experienced users (MUST)<br>• people less confident with computers (MUST)<br>• people with disabilities or impairments, such as vision, hearing, mobility or cognitive (SHOULD)<br>• Māori and Pacific participants (SHOULD) | MUST |
| 2.3 | Recruit at least **5 participants** for each round of testing. | SHOULD |
| 2.4 | Turn each task from 1.3 into a **real situation or scenario** that doesn't give away the answer. Describe the situation, not the steps, and don't use on-screen labels. For example:<br><br>**Add a case note**<br>❌ "Click Add case note"<br>✅ "You've just spoken to someone on the phone about their case. Record what you discussed."<br><br>**Find a case**<br>❌ "Use the search bar to find case 12345"<br>✅ "Someone calls and gives you their name. Find their details."<br><br>**Escalate a high-risk case**<br>❌ "Click the Escalate button"<br>✅ "You're worried someone on your caseload is at risk. Let your team leader know." | MUST |
| 2.5 | If you can, test the **same tasks on the current system first** to get a baseline. | SHOULD |
| 2.6 | Set up **test data**. Never use real patient or personal information. Ask your delivery or test team for a test environment. | MUST |

### 3. Run the test (your test script)

**This stage is your test script.** The standards below are in the order you'll run them in each session: consent, warm-up, tasks, ratings and wrap-up. Your tasks come from 1.3, written as scenarios in 2.4. To turn this into a ready-to-use script, use the [AI prompts](#create-or-update-a-test-script-with-ai) at the end of this page.

**To save time**, you can do consent (3.1) and the warm-up questions (3.2) before the session, for example by email or a short online form.

| # | Standard | Level |
|---|---|---|
| 3.1 | Get each participant's **informed consent** before the session. Explain that recording is optional, their name won't be in reports, and they can stop at any time. Record their consent in writing or on the recording. | MUST |
| 3.2 | Start with a few **warm-up questions** (about 5 minutes) to help the person relax and give you context. Adapt the wording to suit your product. For example:<br>• "What's your role?"<br>• "Can you describe a typical day in your work?"<br><br>**Experience:** "How would you describe your experience with [the product, or what you use now]?"<br>1. New to it<br>2. Still learning<br>3. Can do the usual tasks, but sometimes need help<br>4. Confident without help<br>5. Expert, and help or train others<br><br>**Frequency:** "How often do you do this kind of work?"<br>1. Less than once a month, or never<br>2. About once a month<br>3. About once a week<br>4. About once a day<br>5. Several times a day | MUST |
| 3.3 | Ask people to do each task **without help**. Only step in if they're stuck and can't move on. Record whether they:<br>• completed it (pass)<br>• completed it with help (pass with help)<br>• didn't complete it (fail)<br><br>If a failure was caused by the test itself, such as a broken test environment or wrong test data, don't count it. Fix the problem and rerun the task, with the same participant or another one. | MUST |
| 3.4 | Record the **number of clicks** each person takes to finish each task. Before testing, work out the expected number (the shortest route) so you can compare. Recordings make this easier. | SHOULD |
| 3.5 | Straight after each **task that must go right**, ask the **ease question**. You can ask it after other tasks too if you have time. Keep the question and scale as written, so results can be compared.<br><br>**Ease:** "How easy or difficult was that task?"<br>1. Very difficult<br>2. Difficult<br>3. Neither easy nor difficult<br>4. Easy<br>5. Very easy | MUST |
| 3.6 | After every rating, ask **"Why did you give that rating?"** and write down the answer in the person's own words. | SHOULD |
| 3.7 | At the end of the test, ask the **satisfaction question**, and the **comparison question** if the product replaces something. Keep the questions and scales as written, so results can be compared.<br><br>**Satisfaction:** "Overall, how satisfied are you with your experience?"<br>1. Very dissatisfied<br>2. Dissatisfied<br>3. Neither satisfied nor dissatisfied<br>4. Satisfied<br>5. Very satisfied<br><br>**Comparison:** "Compared with [what you used before], how would you rate this?"<br>1. Much worse<br>2. Worse<br>3. About the same<br>4. Better<br>5. Much better | MUST |

### 4. Report results

> **To be confirmed.** This section is a work in progress, including a results template you can copy.

### 5. Act on feedback

> **To be confirmed.** This section is a work in progress. We're reviewing how feedback is actioned, including feedback added directly to prototypes.

| # | Standard | Level |
|---|---|---|
| 5.1 | Before go-live, **fix anything that doesn't meet the success targets**. | MUST |
| 5.2 | For any failure on a **task that must go right**, record the decision: fix before go-live, or the reason it doesn't need fixing. Record it wherever your team tracks work, for example the backlog. | MUST |
| 5.3 | For every problem, decide **how to address it**: fix in the product, training and guidance, communications, or a combination. Training supports a good design; it doesn't replace one. If people need training for a task they do every day, it's usually a design problem. | MUST |
| 5.4 | Share findings with **whoever is responsible for training and communications** (for example, the change and training team). Include tasks new users struggled with, words people didn't understand, what's different from the old system, and what people liked. | MUST |
| 5.5 | Add all other problems to the **backlog, with an owner**. | SHOULD |

---

## Create or update a test script with AI

Copy a prompt into Copilot or another AI tool and attach this page. Always check the output before you use it.

The script follows stage 3, using your tasks from 1.3 and scenarios from 2.4.

<details>
<summary><strong>Option A: Create a new test script</strong></summary>

```text
Create a usability testing script that meets the Health NZ Usability Standards (attached).

About the product:
- Product or service: [name and one-line description]
- End users: [e.g. case managers, team leaders]
- Where they use it: [e.g. office, remote, mobile]
- What it replaces (if anything): [e.g. old case system, spreadsheet, paper form]
- Is it live yet: [yes / no]
- Tasks people do most often: [list]
- Tasks that must go right: [list]
- Success criteria: [e.g. 80% complete without help, satisfaction of 3 or above]
- Format: [in person / remote], about [30–45] minutes

Rules:
1. Meet every standard in stages 1 to 3 (Decide what to test, Set up the test,
   Run the test) that applies to a test script.
2. Structure: introduction and consent, warm-up questions, tasks, wrap-up.
3. Use the questions in stage 3 as a guide. Adapt the warm-up questions to suit
   the product and users. Keep the rating questions and 5-point scales as written.
4. Write each task as a real situation in everyday words, following the examples in
   standard 2.4. Don't use on-screen labels or give away the answer. Cover both tasks
   done most often and tasks that must go right.
5. Use neutral, open questions only. No leading or yes/no questions.
6. For every task, state its success criteria and the expected number of clicks,
   and record task completion and clicks taken. After each task that must go right,
   ask the ease question with the full labelled scale.
7. At the end, ask the satisfaction question. If the product replaces something,
   also ask the comparison question. Use the full labelled scales.
8. After each rating, ask "Why did you give that rating?"
9. On every rating scale, 1 = bad and 5 = good. Never reverse the scale.
10. Use plain New Zealand English. Use test data only. Never include real patient
    or personal information.
11. Don't invent product details, tasks or user groups. Mark gaps as [TO CONFIRM].

Output:
A) The full script, ready for a facilitator to read from.
B) A note-taking sheet with a row per participant and task.
C) A list of [TO CONFIRM] items.
```

</details>

<details>
<summary><strong>Option B: Update an existing test script</strong></summary>

Attach your existing script as well as this page.

```text
Update the attached usability testing script so it meets the Health NZ Usability
Standards (attached).

Rules:
1. Keep the original goals, product context and tasks unless they break the standards.
2. Check the script against every standard in stages 1 to 3 (Decide what to test,
   Set up the test, Run the test) that applies to a test script. Add anything missing.
3. Add the warm-up questions from stage 3 if missing, adapted to suit the product
   and users.
4. Check the tasks cover both tasks done most often and tasks that must go right.
   Flag gaps as [TO CONFIRM].
5. Add the success criteria (standard 1.5) to every task.
6. Rewrite any task that uses on-screen labels or gives away the answer as a real
   situation, following the examples in standard 2.4.
7. Rewrite any leading or yes/no question as a neutral, open question.
8. Add the ease question after each task that must go right, and the satisfaction
   and comparison questions at the end, with the full labelled scales. Replace any
   other rating scales. On every scale, 1 = bad and 5 = good.
9. After each rating, ask "Why did you give that rating?"
10. Use plain New Zealand English. Use test data only. Never include real patient
    or personal information.
11. Don't invent product details, tasks or user groups. Mark gaps as [TO CONFIRM].

Output:
A) The full updated script.
B) A short table of changes: | What changed | Why (standard number) |
C) A list of [TO CONFIRM] items.
```

</details>

---

## References

- ISO 9241-11:2018: Usability: Definitions and concepts
- ISO 9241-210:2019: Human-centred design for interactive systems
- [ISO Online Browsing Platform](https://www.iso.org/obp/ui/): view the official ISO 9241-11 contents and terms for free
- Health NZ Accessibility Guidelines

**Need help?** Contact the Digital Health Strategy & Design team.
