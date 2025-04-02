Structured AI-Assisted Development: Auto-Coder Template

Overview

This repository provides a template for Structured AI-Assisted Development, a methodology designed to help developers simulate a full tech company workflow using markdown files as “departments” and local AI models for code generation. By automating best practices in security, testing, deployment, and documentation, this approach enables solo developers and small teams to build high-quality, secure, and scalable software with minimal overhead.

The template is optimized for efficiency, automation, and documentation-driven workflows, enabling developers to create self-documenting projects that serve as both production-ready software and training data for AI models.

Features
	•	Simulate Tech Company Workflow: Use markdown files to organize development tasks and best practices.
	•	Automated Best Practices: Automate security, testing, deployment, and code review processes using local AI models.
	•	Self-Documenting Projects: Each project doubles as both the software itself and training data for AI-powered tools.
	•	Portable Institutional Knowledge: Documentation works across LLMs and tools, ensuring reusable knowledge.

Getting Started

Prerequisites

Before starting, ensure that you have the following tools installed:
	•	VSCode: Code editor
	•	Cline: AI code review tool for VSCode
	•	Twinny: Local model integration tool for AI
	•	Continue.dev: Prompt management for your development workflow
	•	Local LLMs: Qwen2.5, Mistral, or Mixtral
	•	Version Control: GitHub or GitLab
	•	Deployment: Netlify or Render for free-tier deployment

Clone the Template Repository

To get started, clone the template repository:

git clone https://github.com/kliewerdaniel/workflow.git
cd workflow

Customizing Core Documentation

Once you’ve cloned the repository, you can customize the core documentation for your project:
	1.	Edit prompts.md: This file contains task-specific instructions for AI tools. Customize it based on your project’s needs.
	2.	Set Deployment Targets in deployment.md: Define your deployment process, environment, and targets for CI/CD integration.


Review & Annotate Code

Once AI generates the code, you can review it and annotate any security or quality issues. Flag issues with the following format:
```
# SECURITY_REVIEW_NEEDED
```
Once reviewed and validated, commit the code using Conventional Commits.

Deployment

The template includes automated deployment configurations using Netlify for the frontend and Render for a Dockerized backend. The pipeline will automatically deploy the frontend with prerendering for SEO and run post-deploy accessibility scans.

Documentation Structure

The core documentation files are organized as follows:

docs/  
├─ ai_guidelines.md   # AI orchestration rules  
├─ prompts.md         # Task-specific AI instructions  
├─ standards.md       # Coding conventions  
├─ security.md        # OWASP compliance checklist  
└─ sop.md             # Step-by-step development procedures  

	•	ai_guidelines.md: Rules and strategies for orchestrating AI in your workflow.
	•	prompts.md: Specific task instructions for the AI model.
	•	standards.md: Coding conventions and best practices.
	•	security.md: Security guidelines, including OWASP compliance.
	•	sop.md: Standard operating procedures for each step of the development process.

