# 🤝 Contributing to Accenture Primer Revision

Thank you for your interest in contributing to **Accenture Primer Revision**! 🎉

This repository is designed to help learners prepare for the Accenture Primer program through organized revision notes, key concepts, examples, study resources, and progress tracking.

Whether you want to fix a typo, improve an explanation, add useful examples, or contribute new study material, your contribution is welcome.

---

## 🎯 Types of Contributions

There are several ways you can contribute to this repository.

### 📚 Revision Content

Help improve or expand the existing study material:

* Add missing concepts to existing topics
* Improve explanations of difficult concepts
* Add important definitions
* Add real-world examples
* Add interview or exam-oriented points
* Add useful diagrams or tables
* Improve existing revision notes

Relevant areas include:

* Software Fundamentals
* Web Technologies
* Generative AI
* Agile, DevOps & DevSecOps
* AWS
* MySQL & Relational Databases
* Python Programming

### 📝 Documentation Improvements

Help make the repository easier to understand and navigate:

* Improve `README.md` files
* Fix grammar and spelling mistakes
* Improve Markdown formatting
* Clarify confusing instructions
* Improve course descriptions
* Add useful navigation links
* Improve the repository structure

### 🧠 Practice Material

You can contribute learning and revision exercises such as:

* Practice questions
* Multiple-choice questions
* Short-answer questions
* Coding exercises
* SQL practice queries
* Python exercises
* Web development exercises
* Scenario-based questions

Make sure practice material is clearly related to the corresponding course.

### 🔗 Learning Resources

You can recommend useful external resources:

* Official documentation
* Tutorials
* Reference guides
* Learning websites
* Official course resources
* Useful videos

Whenever possible, prefer official and reliable sources.

### 🐛 Corrections

Help improve the accuracy of the repository by reporting or fixing:

* Incorrect technical information
* Outdated information
* Broken links
* Incorrect code examples
* Incorrect SQL queries
* Incorrect Python examples
* Formatting problems
* Typographical errors

If you are unsure about a technical correction, open an issue and explain what you found.

### ✨ Repository Improvements

You can also suggest improvements to the repository itself:

* Better folder organization
* Improved progress tracking
* New templates
* Issue templates
* Study checklists
* Revision workflows
* Automation ideas
* Better navigation

For large structural changes, please open an issue before submitting a pull request.

---

# 🚀 Getting Started

## 1. Fork the Repository

Click the **Fork** button at the top of the GitHub repository.

This creates your own copy of the repository where you can safely make changes.

## 2. Clone Your Fork

Clone your fork to your local computer:

```bash
git clone https://github.com/yourusername/accenture-primer-revision.git
cd accenture-primer-revision
```

Replace `yourusername` with your GitHub username.

## 3. Add the Original Repository as Upstream

Add the original repository as the `upstream` remote:

```bash
git remote add upstream https://github.com/original-owner/accenture-primer-revision.git
```

You can verify your remotes with:

```bash
git remote -v
```

## 4. Create a Branch

Create a separate branch for your contribution.

Examples:

```bash
git checkout -b docs/improve-software-fundamentals
```

```bash
git checkout -b notes/add-python-functions
```

```bash
git checkout -b fix/correct-mysql-example
```

```bash
git checkout -b practice/add-web-technology-questions
```

---

# 🌿 Branch Naming Convention

Use a descriptive branch name with one of the following prefixes:

| Prefix      | Purpose                      | Example                             |
| ----------- | ---------------------------- | ----------------------------------- |
| `docs/`     | Documentation changes        | `docs/update-course-readme`         |
| `notes/`    | Revision notes               | `notes/add-python-notes`            |
| `practice/` | Practice questions/exercises | `practice/add-sql-questions`        |
| `fix/`      | Corrections and fixes        | `fix/correct-aws-definition`        |
| `resource/` | Learning resources           | `resource/add-python-documentation` |
| `refactor/` | Repository organization      | `refactor/reorganize-notes`         |
| `feature/`  | New repository features      | `feature/add-progress-template`     |

### Examples

```text
docs/improve-gen-ai-readme
notes/add-devsecops-notes
practice/add-python-exercises
fix/broken-aws-link
resource/add-mysql-documentation
refactor/organize-electives
feature/add-study-checklist
```

---

# 📋 Contribution Guidelines

## Keep Content Course-Specific

Place your contribution in the correct course directory.

For example:

```text
essentials/
├── 01-software-fundamentals/
├── 02-web-technologies/
├── 03-gen-ai/
└── 04-agile-devops-devsecops/
```

and:

```text
electives/
├── 01-aws/
├── 02-mysql-relational-databases/
└── 03-python-programming/
```

Avoid putting course-specific material in the root directory.

---

## Adding a Course

To add a new course, create a folder in the appropriate section and include a `README.md` overview and a `notes.md` file.

Use the next available numbered folder and update `sidebar.md` with links to both files. Keep the course content inside its own folder so the navigation and revision notes stay organized.

Example:

```text
essentials/05-new-course/
├── README.md
└── notes.md
```

---

## 📝 Writing Revision Notes

When adding notes:

* Use clear headings.
* Keep explanations beginner-friendly.
* Define technical terms.
* Include examples when useful.
* Avoid unnecessary repetition.
* Focus on concepts useful for revision.
* Use Markdown consistently.

### Example

````markdown
## Functions in Python

A function is a reusable block of code that performs a specific task.

### Syntax

```python
def greet(name):
    return f"Hello, {name}"
````

### Key Points

* Functions can accept parameters.
* Functions can return values.
* Functions help reduce code duplication.

````

---

# 🧪 Adding Practice Questions

When adding practice questions, clearly identify the topic.

Example:

```markdown
## Python - Functions

### Question 1

What is the primary purpose of a function in Python?

A. To store data permanently  
B. To reuse a block of code  
C. To create a database  
D. To install a package  

**Answer:** B. To reuse a block of code
````

For multiple-choice questions, make sure the answer is technically correct.

Avoid adding questions that are unrelated to the course material.

---

# 💻 Code Contribution Guidelines

For programming-related contributions:

* Use readable code.
* Follow the conventions of the relevant language.
* Include comments when they improve understanding.
* Make examples beginner-friendly.
* Test code before submitting it.

For example, Python contributions should be placed under:

```text
electives/03-python-programming/
```

SQL-related material should be placed under:

```text
electives/02-mysql-relational-databases/
```

---

# 🔗 External Resources

When adding external resources:

* Prefer official documentation.
* Verify that the link works.
* Make sure the resource is relevant.
* Avoid spam or promotional links.
* Do not add resources that require users to provide sensitive information unnecessarily.

Example:

```markdown
## Useful Resources

- Python Documentation
- AWS Documentation
- MySQL Documentation
```

---

# ✍️ Commit Message Guidelines

Use clear and descriptive commit messages.

### Good Examples

```text
docs: improve software fundamentals README
```

```text
notes: add Python functions revision notes
```

```text
practice: add SQL normalization questions
```

```text
fix: correct DevOps terminology
```

```text
resource: add AWS documentation links
```

### Avoid

```text
update
```

```text
changes
```

```text
fix
```

```text
new stuff
```

A good commit message should give the maintainer an idea of what changed.

---

# 🔄 Keep Your Branch Updated

Before starting work, it is recommended to update your local repository:

```bash
git checkout main
git pull upstream main
```

Then create your feature branch:

```bash
git checkout -b notes/add-new-topic
```

If you have already created your branch, you can update it with:

```bash
git fetch upstream
git merge upstream/main
```

Resolve any conflicts before submitting your pull request.

---

# 📤 Submit a Pull Request

After completing your changes:

### 1. Check Your Changes

```bash
git status
```

Review the files you modified.

### 2. Add Your Changes

```bash
git add .
```

### 3. Commit Your Changes

```bash
git commit -m "notes: add Python functions revision notes"
```

### 4. Push Your Branch

```bash
git push origin notes/add-new-topic
```

### 5. Create a Pull Request

Open your fork on GitHub and select **Compare & pull request**.

Explain what you changed and why it would be useful to learners.

---

# 📝 Pull Request Guidelines

## Pull Request Title

Use a clear title that describes the contribution.

### Good Examples

* `Add Python functions revision notes`
* `Improve Web Technologies README`
* `Fix incorrect MySQL example`
* `Add AWS practice questions`
* `Update Gen AI learning resources`

Avoid vague titles such as:

* `Update`
* `Changes`
* `My contribution`
* `Fixes`

---

## Pull Request Description

Use the following template when appropriate:

```markdown
## 📝 Description

Briefly explain what this pull request changes.

## 🎯 Type of Contribution

- [ ] Revision notes
- [ ] Practice questions
- [ ] Documentation
- [ ] Bug fix / correction
- [ ] Learning resource
- [ ] Repository improvement
- [ ] Other

## 📚 Course

- [ ] Software Fundamentals
- [ ] Web Technologies
- [ ] Gen AI
- [ ] Agile, DevOps & DevSecOps
- [ ] AWS
- [ ] MySQL Relational Databases
- [ ] Python Programming

## ✅ Changes Made

- Change 1
- Change 2
- Change 3

## 🔍 Verification

- [ ] Checked Markdown formatting
- [ ] Checked links
- [ ] Verified technical information
- [ ] Tested code examples where applicable
- [ ] Checked that changes are in the correct directory

## 🎓 Educational Value

Explain how this contribution helps learners prepare and revise.
```

---

# 🔍 Review Process

Contributions will be reviewed based on:

### Accuracy

Technical information should be correct and, where appropriate, current.

### Clarity

Content should be understandable to learners.

### Relevance

Contributions should support the purpose of the Accenture Primer revision repository.

### Organization

New material should be placed in the appropriate course directory.

### Consistency

Follow the existing Markdown structure, naming conventions, and writing style.

### Educational Value

Contributions should help learners understand, practice, or revise the relevant topic.

---

# 📖 Content Style Guide

## Markdown

Use:

```markdown
# Main Heading

## Section

### Subsection
```

Use code blocks for code and terminal commands:

```bash
git status
```

Use tables when comparing multiple concepts.

Use bullet points for concise revision information.

---

## Keep Explanations Beginner-Friendly

Instead of:

> HTTP is an application-layer stateless request-response protocol operating over TCP/IP.

Prefer:

> HTTP is a protocol used for communication between web browsers and web servers. A browser sends a request and the server sends a response.

Technical terminology is welcome, but explain it clearly.

---

# 🚫 What Not to Contribute

Please do not contribute:

* Unrelated content
* Spam or promotional material
* Plagiarized content
* Confidential or proprietary information
* Passwords, API keys, tokens, or credentials
* Unverified technical claims
* Malicious code
* Intentionally misleading study material
* Large structural changes without prior discussion

Do not include private information belonging to yourself or others.

---

# 💡 Before Opening an Issue

Before creating an issue:

* Search existing issues.
* Check the relevant course README.
* Check whether the problem already exists.
* Provide enough information for someone else to understand the issue.

Useful issue topics include:

* Incorrect information
* Missing topic
* Broken link
* Suggested learning resource
* Documentation improvement
* New practice material
* Repository improvement

---

# ❓ Questions and Suggestions

If you are unsure about a contribution, open an issue before making a large change.

When asking a question, include:

* The course or topic involved
* What you are trying to contribute
* What you are unsure about
* Any relevant examples

This makes it easier to provide useful feedback.

---

# 📋 Contributor Checklist

Before submitting a pull request, make sure:

* [ ] I have read `CONTRIBUTING.md`
* [ ] I have selected the correct course directory
* [ ] I created a descriptive branch
* [ ] My commit messages are clear
* [ ] My contribution is relevant to the repository
* [ ] I checked the technical accuracy of my content
* [ ] I checked Markdown formatting
* [ ] I checked external links
* [ ] I tested code examples where applicable
* [ ] I did not include passwords, API keys, or private information
* [ ] My pull request clearly explains the changes
* [ ] I have explained the educational value of my contribution

---

# 🏆 Recognition

Contributors who make valuable improvements may be recognized in the repository's acknowledgments.

Every contribution matters — whether it is fixing a typo, correcting a technical concept, adding a useful example, or creating an entirely new revision section.

---

# 🎉 Thank You!

Thank you for helping improve **Accenture Primer Revision**! 🙌

This repository is built around collaborative learning. Your contribution can help another learner understand a difficult concept, practice an important topic, or prepare more effectively.

**Learn → Revise → Practice → Contribute → Grow 🚀**
