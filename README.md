# Purpos3 Engineering Best Practices

This repository contains the official guidelines and best practices for software development at Purpos3. Our primary goal is to **avoid human error** by establishing clear, consistent, and automated workflows.

## Guiding Principle: Keep it Clean and Simple

Everything we do should aim to reduce complexity and increase clarity. A clean `main` branch, understandable commit history, and consistent processes are key to our success.

---

## Git Workflow

Our Git workflow is designed to maintain a clean and linear project history in the `main` branch.

### 1. Squash Merges Only

All pull requests (PRs) targeting the `main` branch **must** be squash merged. This condenses the feature's entire commit history into a single, meaningful commit on the `main` branch.

*   **Why?** It keeps the `main` branch history clean, readable, and focused on features and fixes rather than incremental work-in-progress commits.

### 2. One Pull Request Per Feature Branch

Each feature branch should be created for a single, specific purpose and result in exactly one pull request.

*   **Process:** Once the pull request is merged, the feature branch is automatically closed and should be deleted. This prevents branch proliferation and confusion.

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

---

*This document is a living standard. Suggestions for improvement can be made via pull requests to this repository.*