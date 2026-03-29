# Contributing to flk

Thank you for your interest in contributing to flk. This document covers
everything you need to know to get started.

---

## Table of contents

- [Code of conduct](#code-of-conduct)
- [Developer Certificate of Origin](#developer-certificate-of-origin)
- [How to contribute](#how-to-contribute)
- [Reporting bugs](#reporting-bugs)
- [Requesting features](#requesting-features)
- [Submitting pull requests](#submitting-pull-requests)
- [Commit conventions](#commit-conventions)
- [Platform development](#platform-development)

---

## Code of conduct

Be respectful. We are committed to providing a welcoming and inclusive
environment for everyone. Harassment, discrimination, and abusive behavior
of any kind will not be tolerated.

---

## Developer Certificate of Origin

All contributions to flk must be signed off under the
[Developer Certificate of Origin (DCO)](DCO).

This is a lightweight way to certify that you wrote or have the right to
submit the contribution. It is not a CLA — you retain full copyright over
your contributions.

### How to sign off

Add the following line to every commit message:

```
Signed-off-by: Your Name <your@email.com>
```

The easiest way is to use the `-s` flag:

```sh
git commit -s -m "fix: correct typo in README"
```

Pull requests with commits missing a sign-off will be blocked from merging
automatically by our DCO check.

### Fixing a missing sign-off

If you forgot to sign off on previous commits:

```sh
# Sign off the last N commits
git rebase HEAD~N --signoff
git push --force-with-lease
```

---

## How to contribute

### Reporting bugs

Use the [Bug Report](https://github.com/runflk/flk/issues/new?template=bug_report.yml)
issue template. Include as much detail as possible — version, OS, platform,
steps to reproduce, and relevant configuration.

Always remove sensitive values before sharing configuration.

### Requesting features

Use the [Feature Request](https://github.com/runflk/flk/issues/new?template=feature_request.yml)
issue template. Describe the problem you're trying to solve and your
proposed solution.

### Requesting a new platform

Use the [Platform Request](https://github.com/runflk/flk/issues/new?template=platform_request.yml)
issue template. New official platforms are created and maintained by the
flk team, but community contributions are welcome.

---

## Submitting pull requests

1. **Open an issue first** for significant changes. This avoids wasted effort
   if the direction doesn't align with the project's roadmap.

2. **Fork the repository** and create a branch from `main`:

   ```sh
   git checkout -b fix/your-fix-name
   ```

3. **Make your changes** and ensure they are well-tested.

4. **Sign off all commits**:

   ```sh
   git commit -s -m "fix: your fix description"
   ```

5. **Open a pull request** against `main`. Fill in the PR template completely.

6. **Wait for review.** A maintainer will review your PR and may request
   changes. Please be responsive to feedback.

---

## Commit conventions

flk uses [Conventional Commits](https://www.conventionalcommits.org):

```
<type>: <short description>

[optional body]

Signed-off-by: Your Name <your@email.com>
```

Common types:

| Type | When to use |
|---|---|
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `refactor` | Code change that is not a fix or feature |
| `test` | Adding or updating tests |
| `chore` | Build process, tooling, dependencies |

---

## Platform development

New platforms must be built using the
[flk SDK](https://github.com/runflk/flk-plugin-sdk).

The SDK documentation is available at
[runflk.dev/docs/sdk](https://runflk.dev/docs/sdk).

To request a new official platform, open a
[Platform Request](https://github.com/runflk/flk/issues/new?template=platform_request.yml)
issue. The flk team will create the repo and coordinate development with
interested contributors.

---

## Questions?

Open a [Discussion](https://github.com/orgs/runflk/discussions) — issues
are for bugs and feature requests only.
