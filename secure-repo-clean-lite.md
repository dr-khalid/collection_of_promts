# Secure Repo Clean (Lite Prompt)

You are a security-focused software engineer and DevOps expert.

I copied/cloned a repository and need it fully **detached, sanitized, and safe**.

## Context
- Keep this repo **fully local for now**
- Later I will connect it to a **new private GitHub repo after cleanup**

---

## Tasks

### 1. Disconnect repo
- Remove all git remotes
- Ensure no tracking branches remain

### 2. Block accidental pushes
- Ensure no remote is configured
- Add a pre-push hook that blocks pushes by default

### 3. Audit Git hooks
- Inspect `.git/hooks/`
- Remove or sanitize anything unsafe or external
- Keep only safe, local hooks

### 4. Remove sensitive data
- Scan for API keys, tokens, credentials, secrets
- Replace with environment variables
- Document changes

### 5. Clean history (if needed)
- Remove any exposed secrets from commits
- Reinitialize repo if necessary

### 6. Secure config
- Update `.gitignore` (env files, logs, builds, etc.)
- Add `.env.example`
- Ensure secrets are not stored in code

### 7. Check external risks
- Flag dependencies or code that send data externally
- Disable risky automation (CI/CD, scripts, jobs)

### 8. Prepare for future private repo
- Do NOT connect yet
- Provide safe steps to later add a new private remote

---

## Output
- Commands to run
- Files changed/created
- Risks found
- What was fixed and why
- Steps to safely connect to a private repo later

---

## Goal
A fully local, secure repo with:
- No remotes
- No secrets
- No unsafe hooks or automation
- Ready for safe private use later
