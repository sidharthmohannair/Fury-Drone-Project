
# Contributing to Fury Drone Project

First off, thanks for taking the time to contribute! 🚀  
This document outlines the guidelines for contributing to the **Fury Drone Project**.

---

## How Can You Contribute?

1. **Reporting Bugs**:  
   Found a bug? Create a [new issue](https://github.com/sidharthmohannair/Fury-Drone-Project/issues) on GitHub.
   
2. **Suggesting Enhancements**:  
   Have ideas for improvements? Open an issue with your suggestion.

3. **Fixing Issues**:  
   Pick an open issue and submit a pull request (PR) with your solution.

4. **Improving Documentation**:  
   Enhance clarity, fix typos, or add missing details in the documentation.

---

## Prerequisites

Before you start contributing, ensure you have the following:
- [Git](https://git-scm.com/)
- A code editor, e.g., [VS Code](https://code.visualstudio.com/)
- Required build or testing tools (if applicable)

---

## Setting Up Your Environment

1. Fork the repository to your GitHub account.
2. Clone your fork locally:
   ```bash
   git clone https://github.com/yourusername/Fury-Drone-Project.git
   cd Fury-Drone-Project
   ```
3. Follow the **Installation Guide** (`docs/INSTALLATION.md`) to set up the project.

---

## Contribution Workflow

1. **Create a New Branch**:  
   Work on a feature or fix in a new branch.
   ```bash
   git checkout -b your-branch-name
   ```

2. **Make Changes**:  
   Modify the code or documentation.

3. **Commit Changes**:  
   Write clear and concise commit messages.
   ```bash
   git add .
   git commit -m "Your detailed description of changes."
   ```

4. **Push Your Branch**:  
   Push the branch to your forked repository.
   ```bash
   git push origin your-branch-name
   ```

5. **Open a Pull Request**:  
   - Go to the main repository on GitHub.
   - Click **Compare & pull request**.
   - Fill out the PR template and submit your changes for review.

---

## Areas for Contribution

We welcome contributions in the following areas:
- Expanding the `/tests` folder with more performance test logs.
- Enhancing the ROS integration for RealSense cameras.
- Improving and updating the project documentation.
- Fixing open issues (check the [Issues](https://github.com/sidharthmohannair/Fury-Drone-Project/issues) tab).

---

## Writing and Running Unit Tests

1. Include test cases for any new functionality you add.
2. Ensure all existing tests pass before submitting a PR:
   ```bash
   ./run_tests.sh
   ```
3. Add test logs or results under the `/tests` folder, where applicable.

---

## Reporting Bugs

If you encounter a bug, please:
- Search the [existing issues](https://github.com/sidharthmohannair/Fury-Drone-Project/issues) to ensure it hasn’t been reported.
- Open a [new issue](https://github.com/sidharthmohannair/Fury-Drone-Project/issues/new) with the following details:
  - Version of Fury Drone Project you’re using.
  - Steps to reproduce the issue.
  - Any relevant logs or screenshots.

---

## Pull Request Process

1. Ensure the code compiles and passes all tests.
2. Keep your pull request small and focused on a single issue or feature.
3. Write a clear PR title and description, referencing related issues (e.g., `Fixes #123`).
4. Submit your pull request for review.
5. Respond promptly to feedback and make requested changes.

---

## Coding Standards

- **Coding Style**: Follow the [Google C++ Style Guide](https://google.github.io/styleguide/cppguide.html).
- **Commit Messages**: Write clear and descriptive commit messages.
- **Unit Tests**: Add tests for new features or bug fixes.

---

## Code of Conduct

Please adhere to the [Code of Conduct](/CODE_OF_CONDUCT.md) in all interactions.

---

## License

By contributing to this project, you agree that your contributions will be licensed under the project’s [MIT License](LICENSE).

---
