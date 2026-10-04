# Clear Explanations

**Turn complex AI output into explanations people can understand and use.**

A reusable AI skill for clear writing, diagrams, interactive pages, and explainer videos. Built for technical explanations, client communications, and social posts.

Inspired by [Andrej Karpathy's post](https://x.com/karpathy/status/2105819303471976479): as AI does more work, people need better ways to understand its output. The post discusses simplified technical English, diagrams, interactive HTML pages, and custom video explainers.

## What it does

The skill helps an agent choose an explanation format, use plain language, and preserve accuracy. It defaults to the simplest useful output. A client email can stay an email; a complicated workflow may benefit from a diagram.

| Need | Useful format |
| --- | --- |
| Understand an answer or take an action | Clear text |
| See a workflow or relationships | Diagram |
| Explore how inputs change an outcome | Interactive page |
| Follow a process through time | Narrated video |

This is instruction-based guidance, not a standalone application. Media production depends on the tools available to your agent.

## Install

Clone the repository into your agent's personal skills directory. If the target already exists, update it instead of overwriting local changes.

### Codex - PowerShell

```powershell
git clone https://github.com/AI-Ops1/clear-explanations.git "$env:USERPROFILE/.codex/skills/clear-explanations"
```

### Codex - macOS or Linux

```bash
git clone https://github.com/AI-Ops1/clear-explanations.git ~/.codex/skills/clear-explanations
```

### Other agents

Use the skills directory documented by your agent. Keep `SKILL.md` and its `references/` directory together. For agents without skill support, provide the contents of `SKILL.md` as instructions and include `references/formats.md` when making visual explanations.

Start a new session if your agent has not discovered the new skill. In Codex, invoke it explicitly with `$clear-explanations`.

## Make it a standing preference

Add this to your agent's main instructions file, such as `AGENTS.md`, and adjust the path to your installation:

> Use the clear-explanations skill for every client communication and social media post wherever relevant, including technical explanations. Lead with the main point, use plain words and consistent terms, and explain with concrete examples. Preserve accuracy, necessary qualifications, and brand voice. Use diagrams, interactive pages, or videos when they make understanding easier. Apply this by default; it does not authorize sending or publishing content.

A skill alone does not guarantee that every agent will apply it to every response. The standing instruction makes your preference explicit.

## Try it

```text
$clear-explanations Explain API rate limits to a sales operations manager.
Include one example and the action they should take.
```

```text
$clear-explanations Rewrite this client email so the scope change,
price impact, and approval needed are clear. Preserve all conditions.
```

```text
$clear-explanations Write a LinkedIn post explaining webhooks to
nontechnical founders. Use a concrete example. Do not invent results.
```

```text
$clear-explanations Create a diagram of this approval workflow.
Label decisions and the exception path.
```

```text
$clear-explanations Create an interactive HTML explanation of how
extra project hours affect profit. Label all example numbers.
```

```text
$clear-explanations Create a 60-second storyboard explaining scope
changes. Align each scene with narration; identify production requirements.
```

## Example

Before:

> It is advisable to facilitate comprehensive validation of contractual modifications prior to invoice generation.

After:

> Check that the customer approved the scope change before you create the invoice.

See [worked examples](examples/before-after.md) and the [format guide](references/formats.md).

## Why flexible STE?

[ASD-STE100](https://www.asd-ste100.org/about_STE.html) is a controlled language for technical documentation. It combines writing rules with a controlled dictionary. This skill borrows clarity principles, including consistent terminology and direct instructions, without enforcing the full vocabulary or grammar restrictions.

Karpathy suggests relaxing the standard for ordinary explanations. His “80%” framing is an informal preference, not a compliance score. This repository does not reproduce the STE dictionary, certify compliance, or claim that simpler wording makes a statement true.

## Contributing

Open an issue with the audience, the original explanation, and what was difficult to understand. For changes, include a before/after example and explain how meaning and accuracy were preserved. Use synthetic or publication-authorized content.

## Attribution and license

Independent project inspired by [Andrej Karpathy's post](https://x.com/karpathy/status/2105819303471976479) and [ASD-STE100](https://www.asd-ste100.org/about_STE.html). No affiliation or endorsement is implied. Refer to the original sources for their own terms.

Original repository material is licensed under [MIT](LICENSE). The license does not cover linked third-party standards, posts, or media.
