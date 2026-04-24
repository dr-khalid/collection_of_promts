# Secure Repository Detachment & Sanitization Prompt

## Purpose
This prompt is designed for AI agents to safely detach a cloned/copied repository from its original remote source, eliminate security risks, and prepare it for safe future use in a private environment.

---

## Prompt

You are an expert software engineer, security auditor, and DevOps specialist.

I have copied/cloned a repository from GitHub (or another remote source). Your job is to fully detach this repository from its original source and harden it to prevent any accidental data leaks, credential exposure, or unintended external communication.

This is a security-critical task. Assume the repository may contain sensitive data.

### Important Context
- This repository must remain **fully local and isolated for now**
- Later, I may connect it to a **new private GitHub repository**, but ONLY after everything is cleaned and secured

---

## 1. Disconnect from All Remotes
- Remove ALL git remotes (origin, upstream, etc.)
- Verify no remote URLs remain
- Ensure no branches are tracking remote branches
- Confirm the repository is fully local-only

---

## 2. Prevent Accidental Pushes
- Ensure no default remote exists
- Add safeguards to prevent accidental pushes
- Create a pre-push hook that blocks pushes unless explicitly disabled
- Clearly document how to re-enable pushing later

---

## 3. Audit and Secure Git Hooks
- Inspect `.git/hooks/` for any existing hooks
- Remove or sanitize any hooks that:
  - Send data externally
  - Trigger network activity
  - Run unknown or unsafe scripts
- Add a safe default pre-push hook to block unintended pushes
- Explain what each hook does and why it is safe

---

## 4. Scan for Sensitive Data
Search the entire repository (including history if possible) for:
- API keys, tokens, secrets
- Passwords or credentials
- Private/internal URLs or endpoints
- Hardcoded environment variables
- Certificates or private keys

If found:
- Remove or redact them
- Replace with environment variable usage
- Document all changes clearly

---

## 5. Sanitize Git History
- Check commit history for exposed secrets
- If any are found:
  - Rewrite history to remove them
- If cleanup is complex or uncertain:
  - Reinitialize the repository with a clean history

---

## 6. Harden `.gitignore`
Ensure `.gitignore` includes:
- `.env` and secret config files
- Logs and temp files
- Build/dist artifacts
- OS/system files
- Dependency caches
- Any directories likely to contain sensitive local data

---

## 7. Standardize Environment Configuration
- Create a `.env.example` file with placeholder variables only
- Ensure real `.env` files are ignored
- Refactor code to use environment variables instead of hardcoding

---

## 8. Audit Dependencies and External Communication
- Identify dependencies that may:
  - Send telemetry
  - Call external APIs
- Flag unnecessary or risky network activity
- Suggest safer alternatives if applicable

---

## 9. Remove or Flag Automation Risks
- Inspect for:
  - CI/CD configs (GitHub Actions, GitLab CI, etc.)
  - Deployment scripts
  - Background jobs or cron tasks
- Disable or sanitize anything that:
  - Pushes code
  - Sends data externally
  - Uses stored credentials

---

## 10. Prepare for Future Private Repository
- Do NOT connect to any remote yet
- Ensure the repo is clean and safe for future publishing
- Provide instructions for later safely connecting to a NEW private GitHub repo:
  - Adding a new remote
  - Verifying no sensitive data remains before first push

---

## 11. Output Requirements
Provide:
1. Exact terminal commands to execute
2. Any modified or new file contents (full code)
3. A summary of all risks found
4. A clear explanation of all changes made
5. Any remaining risks or recommendations
6. Instructions for safely reconnecting to a private remote later

---

## Constraints
- Do NOT assume a specific programming language or framework
- Work generically across any repo structure
- Prioritize privacy, isolation, and security
- Do not remove functionality unless it poses a real security risk

---

## Goal
A fully local, secure, sanitized repository with:
- Zero connection to the original source
- No exposed secrets or credentials
- No hidden automation or unsafe hooks
- Safe readiness for future connection to a private GitHub repository
