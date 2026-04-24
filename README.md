# Collection of Prompts

A curated personal library of AI prompts designed to be reused, adapted, and shared. This repository covers a growing range of topics — from security hardening and DevOps workflows to deep codebase analysis. Each prompt is self-contained, clearly structured, and ready to drop into any AI workflow or chat interface.

## About This Repo

This repo is a living collection of high-quality, battle-tested prompts built for real engineering workflows. Instead of rewriting prompts from scratch every time, the goal is to maintain a single source of truth for prompts that can be copy-pasted into any AI assistant — whether that's ChatGPT, Claude, Copilot, or any other LLM.

Prompts here are:
- **Practical** — built around real tasks engineers face day to day
- **Self-contained** — each file can be used independently, no setup required
- **Structured** — written with clear roles, rules, and expected outputs so the AI stays on track
- **Reusable** — generic enough to apply across different projects, languages, and codebases

The collection will grow over time as new workflows are refined and proven useful.

## Repository Structure

```
collection_of_promts/
├── prompts/
│   ├── deep-repo-analysis-multipass.md                     # Deep, multi-pass codebase analysis prompt
│   ├── secure-repo-clean-lite.md                           # Lite prompt: detach & sanitize a cloned repo
│   └── secure-repo-detachment-and-sanitization-prompt.md  # Full prompt: secure repo detachment & hardening
├── LICENSE
└── README.md
```

## Prompt Descriptions

| File | Description |
|------|-------------|
| [`deep-repo-analysis-multipass.md`](prompts/deep-repo-analysis-multipass.md) | A structured, multi-pass prompt that guides an AI through deep, context-safe analysis of an entire codebase — producing an executive document covering architecture, data flow, key components, and risks. |
| [`secure-repo-clean-lite.md`](prompts/secure-repo-clean-lite.md) | A concise prompt for quickly disconnecting a cloned repository from its remote, blocking accidental pushes, removing secrets, and preparing it for safe private use. |
| [`secure-repo-detachment-and-sanitization-prompt.md`](prompts/secure-repo-detachment-and-sanitization-prompt.md) | A comprehensive, step-by-step prompt for fully auditing and hardening a cloned repository — covering remote removal, hook auditing, secret scanning, history sanitization, `.gitignore` hardening, and safe reconnection instructions. |

## Usage

Browse the `prompts/` folder to find the prompt relevant to your use case. Each file is self-contained and can be copied directly into any AI chat interface or agent workflow.

## Contributing

Feel free to open a PR to add new prompts or improve existing ones. Keep each prompt in its own `.md` file under the `prompts/` directory.
