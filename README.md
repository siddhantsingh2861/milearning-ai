# MiLearning.AI – UI Mockup

A clickable mobile mockup of **MiLearning.AI**, an AI learning assistant built as a module inside an enterprise employee app.

Employees tell it what they want to learn, by typing or speaking. It returns courses, videos and articles from Coursera, Udemy, YouTube, Microsoft Learn and the web. It also tracks the learning goals HR assigns.

**Open it:** download `index.html` and open it in any browser. No build step, no dependencies.

> This repo is a **sanitized design mockup**. The organization name is removed and all content is sample data. Nothing here connects to a real system.

---

## What the mockup covers

| Screen | What it does |
| --- | --- |
| Home tile | Today's picks, progress on the HR-assigned goal, a "pick up where you left off" row, time-based filters, and an ask bar with a mic |
| Chat | Topic → level → recommendations. Quick-reply chips, voice input, and a tabbed recommendation card |
| Leave-and-return sheet | Shows cost, certificate and language before sending the user to an external platform. Asks how far they got when they come back |
| My Learning | Assigned, Saved and History in one place, with a status and one action per item |

## Design decisions

Built around how employees in Indian workplaces actually use apps:

- **Voice first.** Many users would rather send a voice note than type in English. The composer takes Hindi, English or Hinglish.
- **Time chips.** People learn on the commute or between meetings. They pick by available time ("Under 10 min") more than by topic.
- **Cost and certificate up front.** "Is it free?" and "Do I get a certificate?" decide whether someone taps. Cards show Free / Paid / Free to audit, Certificate, and a हिंदी badge for Hindi content.
- **Visible progress against the HR goal.** Formal, appraisal-linked targets drive action. The tile shows "1/4 done · due 31 Mar".
- **Gentler level question.** "Just starting / I know the basics / I'm quite confident / Not sure, you decide" replaces Beginner/Expert. People tend to undersell themselves on those labels. If HR already set the level, the question is skipped.
- **Completion check-in.** External platforms don't report completion back. A one-tap "Finished / Halfway / Not started" on return gives HR completion data, not just clicks.
- **One hub.** Saved, History and Assigned live under a single "My Learning" button instead of three unlabelled icons.
- **Larger tap targets and text** for budget Android phones with large font settings.

## What's mocked

- All courses, ratings, providers and dates are placeholders.
- Voice input fills a fixed Hinglish sample after a short delay. A real build needs a speech-to-text service that supports `hi-IN`.
- "Continue to [platform]" jumps straight to the check-in. A real build would open the link and show the check-in when the user returns.
- Share, Applications and other app tiles show a toast only.

## How it connects to the agent

The underlying agent runs in Microsoft Teams. It captures the learning need in chat. A Power Automate flow then posts the recommendations back as an Adaptive Card. This mockup explores the same experience as a native module inside the employee app.

## Tech

Single HTML file. Vanilla JavaScript, CSS, inline SVG icons, Poppins from Google Fonts.
