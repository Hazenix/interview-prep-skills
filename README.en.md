# Interview Prep Skills

[简体中文](README.md) · [Ask AI to install](#installation) · [Examples in Chinese](docs/examples.md)

Practice technical interviews with an AI interviewer that follows up on your answers. Start with a project from your resume, explain your decisions, and get feedback on what to practice next. You can also turn selected resume bullets into a Markdown question set with follow-ups and optional sample answers.

> **Candidate:** When a product changes, I update the database and then delete its Redis cache entry.
>
> **Interviewer:** What happens if a read fetches the old value before the update, then writes it back to the cache after the deletion?

| What you want to practice | Skill | What to expect |
| --- | --- | --- |
| Frontend, browser fundamentals, React or Vue | [Frontend mock interview](skills/frontend-interview-simulator/SKILL.md) | Project questions, technical follow-ups, optional coding, and feedback |
| Java, Go or C++ backend development | [Backend mock interview](skills/backend-interview-simulator/SKILL.md) | One question at a time, with follow-ups based on your answers |
| AI application development with agents, RAG or MCP | [AI application mock interview](skills/ai-dev-interview-simulator/SKILL.md) | Project questions, evaluation and implementation discussions, and optional exercises |
| Questions you might get about your resume | [Resume question generator](skills/resume-interview-question-generator/SKILL.md) | A Markdown question set grouped by resume bullet, with optional sample answers |

The skill instructions and worked examples are primarily in Chinese.

## Installation

Paste this request into an AI tool that supports Agent Skills and can access GitHub and its local skill directory.

```text
Install the following skills from https://github.com/Hazenix/interview-prep-skills:
- skills/frontend-interview-simulator/
- skills/backend-interview-simulator/
- skills/ai-dev-interview-simulator/
- skills/resume-interview-question-generator/

Follow this tool's installation rules, keep each skill directory intact, and list the installed skills.
```

Keep just the directory you need if you want to install a single skill.

## Try it

```text
Use backend-interview-simulator for a Java backend mock interview.
Focus on this resume bullet: I added Redis caching to a product details service to reduce database reads during peak traffic.
```

```text
Use resume-interview-question-generator to create questions and follow-ups from this resume bullet. Questions only, please.
Resume bullet: I added Redis caching to a product details service to reduce database reads during peak traffic.
```

The question generator saves a new Markdown file under `./resume/` in your working directory by default. Remove contact details and confidential information before sharing resume or project materials.

## Contributing

Questions, follow-ups, fixes, and examples are welcome. Include a fictional or sanitized example that shows the behavior you want to improve. [Contribution guide in Chinese](CONTRIBUTING.md)

## License

[MIT](LICENSE)
