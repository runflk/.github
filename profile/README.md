<div align="center">
  <h1>flk</h1>

  <p>
    <strong>One tool. One state. Every platform.</strong>
  </p>

  <p>
    Provision GitHub repos, AWS infrastructure, Kubernetes clusters, and 
    Ansible-configured machines — from a single YAML codebase, tracked in 
    git, with encrypted secrets built in.
  </p>

  <img src="https://img.shields.io/badge/status-early%20development-orange" />
  <img src="https://img.shields.io/badge/license-AGPL%203.0-blue" />
  <img src="https://img.shields.io/badge/DCO-required-green" />
</div>

---

## What is flk?

Modern infrastructure is split across too many tools. Terraform provisions 
cloud resources. Ansible configures machines. Helm deploys services. GitHub 
Actions glues it together. Each tool has its own state, its own secrets, 
its own mental model.

**flk answers all of that from one place.**
```yaml
gh repo payments:
    create: true
    name: payments-service
    visibility: private

aws vpc main:
    create: true
    cidr_block: "10.0.0.0/16"
    lifecycle:
        depends_on: [gh.repo.payments]

mod workload payments:
    create: true
    environment: production
    vpc_id: aws.vpc.main.id
```
```sh
flk plan    # preview every change across every platform
flk apply   # provision everything, in parallel, in the right order
```

---

## Repositories

| Repo | Description | License |
|---|---|---|
| [flk](https://github.com/runflk/flk) | Core CLI | AGPL 3.0 |
| [sdk](https://github.com/runflk/sdk) | SDK for building platforms | Apache 2.0 |
| [platform-gh](https://github.com/runflk/platform-gh) | GitHub platform | Apache 2.0 |
| [platform-aws](https://github.com/runflk/platform-aws) | AWS platform | Apache 2.0 |
| [platform-ansible](https://github.com/runflk/platform-ansible) | Ansible platform | Apache 2.0 |
| [platform-k8s](https://github.com/runflk/platform-k8s) | Kubernetes platform | Apache 2.0 |
| [guides](https://github.com/runflk/guides) | Documentation and examples | MIT |
| [runflk.dev](https://github.com/runflk/runflk.dev) | Documentation site | MIT |

---

## Contributing

flk is in early development and we welcome contributions of all kinds:

- 🐛 Bug reports and fixes
- 💡 Feature suggestions
- 📖 Documentation improvements
- 🔌 Platform development

All contributions require a sign-off under the 
[Developer Certificate of Origin](https://github.com/runflk/.github/blob/main/DCO).
```sh
git commit -s -m "your commit message"
```

See [CONTRIBUTING.md](https://github.com/runflk/.github/blob/main/CONTRIBUTING.md) 
for full details.

---

## Status

flk is under active early development. APIs and configuration formats may 
change before the first public release.

Watch this space — or star a repo to follow along.

---

<div align="center">
  <sub>
    Thank you <a href="https://anthropic.com">Anthropic</a> & <a href="https://claude.ai">Claude</a>
    <br>
    Built with ❤️ ·
    <a href="https://runflk.dev">Documentation</a> ·
    <a href="https://runflk.com">Website</a>
  </sub>
</div>
