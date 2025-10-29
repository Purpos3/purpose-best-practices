# Purpose Engineering Best Practices

This repository contains the official guidelines and best practices for software development at Purpose. Our primary goal is to **avoid human error** by establishing clear, consistent, and automated workflows.

Our standards are open source under the [MIT License](LICENSE).

---

## Table of Contents
1. [Guiding Principle](#guiding-principle-keep-it-clean-and-simple)
2. [Repository Naming Conventions](#repository-naming-conventions)
3. [Git Workflow](#git-workflow)
4. [Commit Message Conventions](#commit-message-conventions)

---

## Guiding Principle: Keep it Clean and Simple

Everything we do should aim to reduce complexity and increase clarity. A clean `main` branch, understandable commit history, and consistent processes are key to our success.

## Repository Naming Conventions

To maintain a clear and organized structure within our GitHub organization, all repositories should follow a consistent naming scheme.

### Application and Service Repositories

All repositories that are part of our core application or related microservices must be prefixed with `purpose-`. The name should be lowercase and use hyphens to separate words.

**Format:** `purpose-<service-or-app-name>`

**Examples:**
* `purpose-backend`
* `purpose-employer-webapp`
* `purpose-jobseeker-mobileapp`

### Foundational & Meta Repositories

Repositories that serve a foundational or organizational purpose (e.g., documentation, organization-wide configurations) may omit the prefix for clarity.

**Examples:**
* `.github` (For organization-wide profile and settings)
* `purpose-best-practices` (This repository)
* `design-system`

---

## Git Workflow

Our Git workflow is designed to maintain a clean and linear project history in the `main` branch. All changes, even to this document, must be made via a pull request.

### 1. Squash Merges Only

All pull requests (PRs) targeting the `main` branch **must** be squash merged. This condenses the feature's entire commit history into a single, meaningful commit on the `main` branch.

*   **Why?** It keeps the `main` branch history clean, readable, and focused on features and fixes rather than incremental work-in-progress commits.
*   **PR Required:** Every merge to `main` must be associated with a pull request. Direct commits to `main` are not allowed.
*   **PR Number Required:** All squash merge commit titles must include the PR number in brackets at the end (e.g., `feat: Add user authentication (#42)`). This creates traceability between commits and their corresponding pull requests.

### 2. One Pull Request Per Feature Branch

Each feature branch should be created for a single, specific purpose and result in exactly one pull request.

*   **Process:** Once the pull request is merged, the feature branch is automatically closed and should be deleted. This prevents branch proliferation and confusion.

### 3. Auto-Delete Head Branches

All repositories **must** have the "Automatically delete head branches" setting enabled in GitHub.

*   **How to enable:** Go to Settings → General → Pull Requests → Check "Automatically delete head branches"
*   **Why?** This automatically cleans up feature branches after PRs are merged, reducing manual overhead and keeping the repository tidy. Deleted branches can still be restored if needed.

---

## Commit Message Conventions

We follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification to create an explicit and readable commit history.

Each commit message should be prefixed with a type. The most common types are:

*   **feat:** A new feature for the user.
*   **fix:** A bug fix for the user.
*   **docs:** Changes to documentation.
*   **style:** Formatting, missing semi-colons, etc.; no production code change.
*   **refactor:** Refactoring production code, e.g., renaming a variable.
*   **test:** Adding missing tests, refactoring tests; no production code change.
*   **chore:** Updating grunt tasks etc.; no production code change.

**Example:** `feat: Add user authentication endpoint`

### Commit Message Body Guidelines

When adding a commit body (the detailed description after the subject line), keep it concise and focused:

*   **Maximum 3 bullet points:** Commit bodies should contain no more than 3 bullet points of description.
*   **Why?** This enforces clarity and prevents commits from becoming too large or unfocused. If you need more than 3 points, consider breaking the work into smaller, more atomic commits.
*   **Applies to all commits:** This guideline applies to merge commits, squash commits, and regular commits alike.

---

*This document is a living standard. Suggestions for improvement can be made via pull requests to this repository.*