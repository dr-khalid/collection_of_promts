# Collection of Prompts

A curated personal library of AI prompts designed to be reused, adapted, and shared. This repository covers a growing range of topics — from security hardening and DevOps workflows to general-purpose AI agent instructions. Each prompt is self-contained, clearly structured, and ready to drop into any AI workflow or chat interface.

## Repository Structure

```
collection_of_promts/
├── prompts/
│   ├── secure-repo-clean-lite.md                       # Lite prompt: detach & sanitize a cloned repo
│   └── secure-repo-detachment-and-sanitization-prompt.md  # Full prompt: secure repo detachment & hardening
├── LICENSE
└── README.md
```

## Prompt Descriptions

| File | Description |
|------|-------------|
| [`secure-repo-clean-lite.md`](prompts/secure-repo-clean-lite.md) | A concise prompt for quickly disconnecting a cloned repository from its remote, blocking accidental pushes, removing secrets, and preparing it for safe private use. |
| [`secure-repo-detachment-and-sanitization-prompt.md`](prompts/secure-repo-detachment-and-sanitization-prompt.md) | A comprehensive, step-by-step prompt for fully auditing and hardening a cloned repository — covering remote removal, hook auditing, secret scanning, history sanitization, `.gitignore` hardening, and safe reconnection instructions. |

## Usage

Browse the `prompts/` folder to find the prompt relevant to your use case. Each file is self-contained and can be copied directly into any AI chat interface or agent workflow.

## Contributing

Feel free to open a PR to add new prompts or improve existing ones. Keep each prompt in its own `.md` file under the `prompts/` directory.
