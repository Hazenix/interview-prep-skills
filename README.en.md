# Interview Prep Skills

[简体中文](README.md) · [Ask AI to install](#installation) · [Examples in Chinese](docs/examples.md)

**Prepare your resume and practice for interviews.** Turn project notes and code into Chinese resume bullets, then use any bullet to generate a Markdown question set with follow-ups and optional sample answers.

When you want to practice responding in an interview, choose a frontend, Java/Go/C++ backend, or AI application development mock interview. The interviewer asks follow-ups based on your answers and gives feedback at the end.

| What you want to prepare | Skill | What to expect |
| --- | --- | --- |
| Resume bullets from project or internship materials | [Resume bullet writer](#resume-bullet-writer) | Candidate bullets in Chinese, a shortlist, and ways to verify estimated impact |
| Questions you might get about your resume | [Resume question generator](skills/resume-interview-question-generator/SKILL.md) | A Markdown question set grouped by resume bullet, with optional sample answers |
| Frontend, browser fundamentals, React or Vue | [Frontend mock interview](skills/frontend-interview-simulator/SKILL.md) | Project questions, technical follow-ups, optional coding, and feedback |
| Java, Go or C++ backend development | [Backend mock interview](skills/backend-interview-simulator/SKILL.md) | One question at a time, with follow-ups based on your answers |
| AI application development with agents, RAG or MCP | [AI application mock interview](skills/ai-dev-interview-simulator/SKILL.md) | Project questions, evaluation and implementation discussions, and optional exercises |

The skill instructions and worked examples are primarily in Chinese.

## Installation

Paste this request into an AI tool that supports Agent Skills and can access GitHub and its local skill directory.

```text
Install the following skills from https://github.com/Hazenix/interview-prep-skills:
- skills/resume-bullets/
- skills/resume-interview-question-generator/
- skills/frontend-interview-simulator/
- skills/backend-interview-simulator/
- skills/ai-dev-interview-simulator/

Follow this tool's installation rules, keep each skill directory intact, and list the installed skills.
```

Keep just the directory you need if you want to install a single skill.

## Resume bullet writer

[`resume-bullets`](skills/resume-bullets/SKILL.md) drafts and shortlists bullets from internship, personal project, or open-source work. It draws on project materials by default. Choose personal contribution mode to focus on your own commits and pull requests.

The draft labels estimates and explains how to verify them. By default, the Markdown document is saved under `./resume/` in your working directory.

```text
Use resume-bullets to draft Chinese resume bullets from the code and README in ./task-dashboard. Focus on the impact of retries and batch imports in this personal project.
```

[See a resume bullet example in Chinese](docs/examples.md#简历条目打磨)

## Resume question generator

```text
Use resume-interview-question-generator to create questions and follow-ups from this resume bullet. Questions only, please.
Resume bullet: I added Redis caching to a product details service to reduce database reads during peak traffic.
```

For this bullet, the question set could ask how you kept cached product details fresh, then follow up with what happens if a read writes an old value back after cache invalidation. A new Markdown file is saved under `./resume/` in your working directory by default.

## What the three mock interviews share

- **Difficulty by career stage.** Choose a regular internship, summer internship, new grad, or early career interview.
- **Six interviewer styles.** Choose a strict, encouraging, efficient, theory focused, practical, or balanced interviewer.
- **Follow-ups based on your answers.** The interviewer asks one question at a time and probes implementation, trade-offs, and how you verified your work.
- **Optional resume and job description.** Use your own project experience and a target role to guide the interview.
- **Coding or practical exercises.** Add an exercise relevant to the track.
- **Progress tracking and two correction modes.** Keep track of covered topics. Choose between a stricter simulation and immediate guidance when you make a mistake.
- **Feedback by dimension.** Get scores and suggestions tied to what you covered in the interview.

> **Candidate:** When a product changes, I update the database and then delete its Redis cache entry.
>
> **Interviewer:** What happens if a read fetches the old value before the update, then writes it back to the cache after the deletion?

```text
Use backend-interview-simulator for a Java backend mock interview.
Focus on this resume bullet: I added Redis caching to a product details service to reduce database reads during peak traffic.
```

## Contributing

Questions, follow-ups, fixes, and examples are welcome. Include a fictional or sanitized example that shows the behavior you want to improve. [Contribution guide in Chinese](CONTRIBUTING.md)

## License

[MIT](LICENSE)
