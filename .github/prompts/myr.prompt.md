---
description: "Structured entry point for the myr team. Use this slash command to submit a task — VS Code will ask for your input, keeping every request consistently formatted and token-efficient."
name: "myr"
argument-hint: "Describe your task (e.g. 'write a FastAPI endpoint for user auth' or 'design VPC for prod on AWS')"
agent: "myr"
---
Be concise. No preamble, no summary, no closing remarks. Show code directly when relevant.

Task: $args
