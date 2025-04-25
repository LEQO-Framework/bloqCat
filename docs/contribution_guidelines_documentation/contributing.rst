Contributing to bloqCat
=======================

Thanks for your interest in contributing! Here's how you can help:

- Fork the repo and create a new branch.
- Follow PEP8 for Python code.
- Include meaningful commit messages.
- Run tests before submitting a pull request.

Follow best practises outlined below:

1. General Guidelines
Never push directly to main: Always use branches and pull requests (PRs) for changes.
Keep main stable: The main branch should always be deployable and free of bugs.
Communicate: Keep your team informed about ongoing changes and reviews.
2. Workflow
Step 1: Sync Your Local Repository
Before starting work, ensure your local repository is up to date:

# Fetch the latest changes from the remote repository
git fetch origin

# Switch to the main branch and pull the latest updates
git checkout main
git pull origin main
Step 2: Create a New Branch
Create a feature branch for your changes:

# Create a new branch and switch to it
git checkout -b feature/your-branch-name
Branch naming conventions:

Use prefixes like feature/, bug/, or fix/.
Keep branch names descriptive and concise (e.g., feature/add-login-page).
Step 3: Commit Changes
Make atomic commits with clear, descriptive messages:

# Stage your changes
git add .

# Commit your changes
git commit -m "[Scope] Short description of the change"
Commit message format:

Scope: What part of the codebase does this change affect? (e.g., [UI], [Backend])
Description: A concise summary of the change.
Example:

[UI] Add login button to navbar
Step 4: Push the Branch to Remote
Push your branch to the remote repository:

# Push the branch to the remote repository
git push origin feature/your-branch-name
Step 5: Open a Pull Request (PR)
Open a PR on GitHub to merge your branch into main:

Assign reviewers from your team (include the supervisors).
Provide a clear description of the changes.
Link to any relevant issues or tickets.
3. Code Review Process
Review Early: Request a review as soon as your PR is ready.
Be Responsive: Address feedback promptly and update the PR as needed.
Focus on Quality: Reviewers should verify that:
Code is clean, maintainable, and well-documented.
4. Merging the Pull Request
Before Merging:
Ensure all checks (CI/CD, tests, linting) pass, if set-up.
Confirm at least one reviewer has approved the PR. Most of the time, we also merge after all comments are resolved
Final Step:
After merging, delete the feature branch on GitHub to keep the repository clean.