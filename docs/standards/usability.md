---
title: Usability
description: The Health NZ usability standards, set out in the order you do the work. Includes the questions to ask and AI prompts to create or update a usability test script.
---

# Usability standards

> **Work in progress**
> We're working with the Health NZ Standards team on how to apply the ISO 9241 international usability standards.

## The basics

1. Decide what you want to learn and what good looks like, before you start.
2. Test with real users.
3. Give them realistic scenarios to work through.
4. Share what you find with the team, so they can decide what to fix and what to do next.

---

## About Usability

Usability is the extent to which a system, product or service can be used by specified users to achieve specified goals with effectiveness, efficiency and satisfaction in a specified context of use (ISO 9241-11).

Usability is affected by:
- **the users:** who they are
- **their goals:** what they're trying to do
- **their situation:** where and how they use it ("context of use")

We can measure usability in three ways:

| Measure | Question | How we measure it | Example of what good looks like |
|---|---|---|---|
| Effectiveness | **Can people complete tasks correctly?** | Task completion and accuracy | Most people (80% or more) complete top tasks |
| Efficiency | **How much time and effort does it take?** | Time on task, number of clicks, effort (ease rating) | Most people rate it easy, and tasks take no more than about twice the time of an experienced user |
| Satisfaction | **Does it meet people’s needs and expectations?** | Satisfaction rating | Most people are satisfied (average rating of 3 or above out of 5) |

---

## Before you start

**This page covers usability testing.** It’s a **validation** method: checking that your design works (the **solution space**). It doesn’t cover discovery research, which is about understanding people’s needs before you design (the problem space).

### Ways to run the test

These standards focus on **testing with a facilitator** (moderated testing), where someone runs each session in person or on a video call.

Most also apply when people test on their own (unmoderated testing), but this needs a specialist online tool. Ask the Digital Health Strategy & Design team which tools are approved.

---

## The standards

The standards are grouped into five stages:

1. **[Decide what to test](#1-decide-what-to-test)**
2. **[Set up the test](#2-set-up-the-test)**
3. **[Run the test](#3-run-the-test-your-test-script)**
4. **[Report results](#4-report-results)**
5. **[Act on feedback](#5-act-on-feedback)**

### 1. Decide what to test

| # | Standard | Level |
|---|---|---|
| 1.1 | Identify **who will use it** (the real users), for example identify specific role types or job titles. | MUST |
| 1.2 | Describe **where they'll use it**, for example in the office, remotely, in front of consumers, on a laptop. | SHOULD |
| 1.3 | List the top tasks to test:<br>• the **tasks people do most often** (high frequency), for example logging in, finding a case or adding a case note<br>• the **critical tasks**, where a mistake could cause harm or serious problems, even if they're not high frequency, for example escalating a high-risk case | MUST |
| 1.4 | If it **replaces a system or process**, note what people use now, for example one or more old systems, a spreadsheet or a paper form. | SHOULD |
| 1.5 | **Define success criteria** for the tasks and ratings. For example:<br>• at least 80% of participants complete top tasks without help<br>• an average satisfaction rating of 3 or above | MUST |
| 1.6 | Plan to test **before go-live**. | MUST |
| 1.7 | Plan a separate walkthrough with **managers and/or subject matter experts**. Their views add to testing with real users; they don't replace it. A subject matter expert who uses the product can take part as a real user. | SHOULD |

### 2. Set up the test

| # | Standard | Level |
|---|---|---|
| 2.1 | Recruit **real users**, not just the project team. | MUST |
| 2.2 | Recruit a **mix of participants** (one person can cover several of these):<br>• new users<br>• experienced users<br>• people less confident with computers<br>• people with disabilities or impairments, such as vision, hearing, mobility or cognitive<br>• Māori and Pacific participants | SHOULD |
| 2.3 | Recruit at least **5 participants** for each round of testing. | SHOULD |
| 2.4 | Turn each task from 1.3 into a **real situation or scenario** that doesn't give away the answer. Describe the situation, not the steps, and don't use on-screen labels. For example:<br><br>**Add a case note**<br>Instead of: "Click Add case note"<br>Try: "You've just spoken to someone on the phone about their case. Record what you discussed."<br><br>**Find a case**<br>Instead of: "Use the search bar to find case 12345"<br>Try: "Someone calls and gives you their name. Find their details."<br><br>**Escalate a high-risk case**<br>Instead of: "Click the Escalate button"<br>Try: "You're worried someone on your caseload is at risk. Let your team leader know." | MUST |
| 2.5 | If you can, test the **same tasks on the current system first** to get a baseline. | SHOULD |
| 2.6 | Set up **test data**. Never use real patient or personal information. Ask your delivery or test team for a test environment. | MUST |

### 3. Run the test (your test script)

**This stage is your test script.** The standards below are in the order you'll run them in each session: consent, warm-up, tasks, ratings and wrap-up. Your tasks come from 1.3, written as scenarios in 2.4. Your script also needs each task's success criteria (1.5), and test data only (2.6). To turn this into a ready-to-use script, use the [AI prompts](#create-or-update-a-test-script-with-ai) at the end of this page.

**To save time**, you can do consent (3.1) and the warm-up questions (3.2) before the session, for example by email or a short online form.

| # | Standard | Level |
|---|---|---|
| 3.1 | Get each participant's **informed consent** before the session. Explain that recording is optional, their name won't be in reports, and they can stop at any time. Record their consent in writing or on the recording. | MUST |
| 3.2 | Start with a few **warm-up questions** to help the person relax and give you context. Keep this to about 5 minutes. It's not a discovery interview. Adapt the wording to suit your product. For example:<br>• "What's your role or job title?"<br>• "How long have you been working in [role]?"<br>• "Can you describe a typical day in your work?"<br><br>**Experience:** "How would you describe your experience with [the product or service]?"<br>1. New to it<br>2. Still learning<br>3. Can do the usual tasks, but sometimes need help<br>4. Confident without help<br>5. Expert, and help or train others<br><br>**Frequency:** "How often do you use [the product or service]?"<br>1. Less than once a month, or never<br>2. About once a month<br>3. About once a week<br>4. About once a day<br>5. Several times a day | SHOULD |
| 3.3 | Ask people to do each task **without help**. Only step in if they're stuck and can't move on. Record whether they:<br>• completed it (pass)<br>• completed it with help (pass with help)<br>• didn't complete it (fail)<br><br>If a failure was caused by the test itself, such as a broken test environment or wrong test data, don't count it. Fix the problem and rerun the task, with the same participant or another one. | MUST |
| 3.4 | Record the **time** and **number of clicks** each person takes to finish each task, and note any wrong turns or retries, for example going to the wrong screen or starting again. You don't need to do this during the session. If you record it, you can count afterward. Before testing, time an experienced user doing each task and count their clicks, so you can compare. | SHOULD |
| 3.5 | For tasks you want to know more about, such as **critical tasks**, ask the **ease question** straight after. Finishing a task doesn't always mean it was easy.<br><br>**Ease:** "How easy or difficult was [that task]?"<br>1. Very difficult<br>2. Difficult<br>3. Neither easy nor difficult<br>4. Easy<br>5. Very easy | SHOULD |
| 3.6 | If you need more context about a rating, ask **"Why did you give that rating?"** | SHOULD |
| 3.7 | At the end of the test, ask the **overall ease question**. Keep the question and scale as written, so results can be compared.<br><br>**Overall ease:** "Overall, how easy or difficult was [the product or service] to use?"<br>1. Very difficult<br>2. Difficult<br>3. Neither easy nor difficult<br>4. Easy<br>5. Very easy | MUST |
| 3.8 | Ask the **satisfaction question**. Keep the question and scale as written.<br><br>**Satisfaction:** "Overall, how satisfied are you with your experience?"<br>1. Very dissatisfied<br>2. Dissatisfied<br>3. Neither satisfied nor dissatisfied<br>4. Satisfied<br>5. Very satisfied | MUST |
| 3.9 | If the product replaces something, ask the **comparison question**. Keep the question and scale as written.<br><br>**Comparison:** "Compared with [what you used before], how would you rate this?"<br>1. Much worse<br>2. Worse<br>3. About the same<br>4. Better<br>5. Much better | SHOULD |
| 3.10 | Wrap up: **thank them for their time**, ask if they have anything else to add, and tell them what happens next with their feedback. | SHOULD |

### 4. Report results

> **More guidance coming soon**, including a results template you can copy.

| # | Standard | Level |
|---|---|---|
| 4.1 | **Check your results against your success criteria** (1.5). For each task and rating, say whether it met the criteria. Report counts alongside percentages, for example 4 of 5 (80%), because the numbers are small. | MUST |
| 4.2 | Make sure **all feedback is recorded and available to act on**, including people's reasons in their own words (3.6). Share it with the project team, and with the change and training team for anything that affects training or rollout. | MUST |

### 5. Act on feedback

> **To be confirmed.** This section is a work in progress. We're reviewing how feedback is actioned, including feedback added directly to prototypes.

---

## Create or update a test script with AI

Copy a prompt into Copilot or another AI tool. If your tool can't open web pages, paste this page's content into the chat as well. Always check the output against stage 3 before you use it.

**Create a new test script**

```text
Create a short usability test script that meets the Health NZ Usability Standards:
https://tewhatuora.github.io/design-docs-playground/standards/usability/

Product: [name and one-line description]
Users: [for example case managers, team leaders]
What it replaces (if anything): [for example old system, spreadsheet, paper form]
Tasks people do most often: [list]
Critical tasks: [list]
How it will run: [with a facilitator / people on their own]

Follow stage 3, and show which parts are must and which are should. Give me a
script a facilitator can read from and a simple note-taking sheet. Keep it concise
and use plain New Zealand English. Mark anything you don't know as [TO CONFIRM].
```

**Update an existing test script** (attach your script)

```text
Check the attached usability test script against stage 3 of the Health NZ
Usability Standards:
https://tewhatuora.github.io/design-docs-playground/standards/usability/

Add anything missing, keep everything else as it is, and list what you changed.
Mark anything you don't know as [TO CONFIRM].
```

---

## References

- ISO 9241-11:2018: Usability: Definitions and concepts
- ISO 9241-210:2019: Human-centred design for interactive systems
- [The NCredible Framework](https://uxinsight.org/a-practical-tool-for-prioritising-research-questions-and-ensuring-that-they-dont-all-end-up-in-a-usability-test/) (twig+fish research practice): prioritising research questions

**Need help?** Contact the Digital Health Strategy & Design team.
