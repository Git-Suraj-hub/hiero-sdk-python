```md
# Contributing Guide

This document explains how to contribute effectively to this project and outlines the required steps for submitting a complete and review-ready contribution.

---

## 1. Understand What “Contributing” Means

In this project, a contribution is considered **complete** only when it includes:

- Code changes (feature, fix, or improvement)
- A proper changelog entry under the **[Unreleased]** section
- A linked GitHub issue reference

**Contribution formula:**

```

Contribution = Code + Changelog Entry + Issue Reference

````

---

## 2. Step-by-Step Contribution Process

### Step 1: Find or Create an Issue

Before writing any code:

1. Go to the project’s **GitHub Issues**
2. Either:
   - Select an existing open issue, or
   - Create a new issue describing:
     - What is broken or missing
     - Why it matters
     - Expected behavior

You will receive an issue number such as `#123`.  
This issue number is **mandatory** for the changelog entry.

---

### Step 2: Fork the Repository

1. Click **Fork** on GitHub
2. Clone your fork locally:

```bash
git clone https://github.com/<your-username>/hiero-python-sdk.git
cd hiero-python-sdk
````

---

### Step 3: Create a Feature Branch

Never work directly on `main`.

```bash
git checkout -b fix-transfer-memo-null
```

Use a clear and descriptive branch name.

---

### Step 4: Make Your Code Changes

Examples of valid contributions:

* Fix a bug in a transaction file
* Add a new utility function
* Refactor existing code
* Improve documentation

Keep your changes focused on the linked issue.

---

## 3. Add the Required Changelog Entry (Very Important)

### Step 5: Open `CHANGELOG.md`

* Located in the repository root
* Find the **[Unreleased]** section at the top

---

### Step 6: Choose the Correct Section

| Type of Work               | Section       |
| -------------------------- | ------------- |
| New feature                | `### Added`   |
| Behavior change / refactor | `### Changed` |
| Bug fix                    | `### Fixed`   |

---

### Step 7: Write the Changelog Entry

Add your entry **at the top** of the chosen subsection.

**Required format:**

```md
- Brief description of the change (#IssueNumber)
```

#### Examples

**Bug fix**

```md
### Fixed
- Resolve `TypeError` when passing `None` as memo in `transfer_transaction.py` (#456)
```

**New feature**

```md
### Added
- Introduce helper function for automatic account balance queries with retry support (#321)
```

**Refactor**

```md
### Changed
- Refactor `query_balance.py` into modular helper functions to improve readability and error handling (#123)
```

---

## 4. Validate Before Committing

Before committing, confirm:

* Entry is under **[Unreleased]**
* Correct section is used (Added / Changed / Fixed)
* Issue number is included
* Entry is 1–2 sentences
* User impact is clearly described

---

## 5. Commit and Push

```bash
git add .
git commit -m "Fix transfer memo None handling (#456)"
git push origin fix-transfer-memo-null
```

---

## 6. Open a Pull Request (PR)

When creating the PR:

* Link the issue in the PR description
* Mention that a changelog entry is included
* Briefly explain:

  * What changed
  * Why it was needed
  * How it was tested

**Example PR description:**

```md
Fixes #456

This PR resolves a TypeError that occurred when passing None as the memo
parameter in transfer transactions. A changelog entry has been added under
[Unreleased] → Fixed.
```

---

## 7. Respond to Review Feedback

Maintainers may request:

* Improved changelog wording
* Moving the entry to a different section
* Clarification of behavior

This is normal. Make the requested updates and push again.

---

## 8. Common Mistakes to Avoid

* Adding changelog entries under released versions
* Forgetting the issue reference
* Writing vague entries such as “minor fix”
* Writing paragraphs instead of bullet points
* Skipping the changelog entry entirely

---

## 9. Beginner-Friendly Ways to Contribute

If you are new:

* Fix typos in documentation
* Improve error messages
* Refactor small scripts
* Add missing edge-case handling
* Improve examples

All of these still require a changelog entry.

---

## 10. Key Takeaway

For this project:

**No changelog entry = incomplete contribution**

```

---

If you want, I can also:
- Rename the file to match repo conventions
- Shorten it if maintainers prefer concise docs
- Write the **exact changelog entry** for adding this file

Just tell me.
```
