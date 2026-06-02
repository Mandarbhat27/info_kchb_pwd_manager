# Contributing to info_kchb_pwd_manager

Thanks for your interest in contributing! This project is an open-source, self-hostable enterprise account & password management system, and contributions of all kinds are welcome — bug reports, feature ideas, documentation, and code.

## Ways to contribute

- **Report a bug** — open an issue describing what happened, what you expected, and the steps to reproduce it.
- **Suggest a feature** — open an issue explaining the use case and the problem it solves.
- **Improve documentation** — fixes to the README, setup guides, or translations are very welcome.
- **Submit code** — pick up an open issue (look for `good first issue`) and send a pull request.

## Development setup

```bash
# 1. Fork and clone the repository
git clone https://github.com/<your-username>/info_kchb_pwd_manager.git
cd info_kchb_pwd_manager

# 2. Create a virtual environment
python -m venv venv
venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run database migrations and start the server
python manage.py migrate
python manage.py runserver
```

## Pull request guidelines

1. Create a branch from `main` with a descriptive name (e.g. `fix/login-error` or `feat/export-csv`).
2. Keep each pull request focused on a single change.
3. Write clear commit messages that explain *why* the change is made.
4. Make sure the project still runs locally before opening the PR.
5. Reference the related issue number in the PR description (e.g. `Closes #12`).

## Reporting security issues

This project handles sensitive credential data. **Do not** open a public issue for security vulnerabilities. Instead, please contact the maintainer privately so the issue can be addressed before disclosure. Never include real credentials, secrets, or `.env` files in issues, pull requests, or commits.

## Code of conduct

Be respectful and constructive. We want this to be a welcoming project for contributors of all experience levels.
