---
theme: dracula
coverAuthor: Aligent - Daniel van der Ploeg
coverDate:
paginationPagesDisabled: true
paginationX: undefined
paginationY: undefined
image: '/background.jpg'
layout: intro
---

# Automation Made Easy

Revolutionize Your Development with Pipelines

---
layout: image-right
image: technologist.svg
---

# Who am I?

- DevOps Engineer at Aligent
- Degree in Information Technology (Software Development)
- Previously worked in a hybrid tech role

---
layout: image-right
image: /pipelines.jpg
---

# What is a DevOps Engineer?

- Bridge the gap between developers and operations
- Work closely with developers to automate processes
- Continuous Integration / Continuous development (CI/CD)

---
layout: image-right
image: git.png
---

# Pipeline Talk Prerequisites

- git
  - Pushing, merging
  - Pull requests
- npm
  - Node package manager
  - Install third party dependencies
  - Run custom scripts (e.g. `npm build`)
- basic bash scripting

---
layout: two-cols
---

# What are pipelines?

- Run commands in specific order
- Generally written in yaml

<br>

## What problems do they solve?

- Automate common tasks
- Save developer time
- Keep processes uniform
- Prevent bad code from being deployed to production

::right::

```yaml
name: Deploy Application

on:
  push:
    branches:
      - main

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - uses: actions/setup-node@v3
        with:
          node-version: 'lts/*'

      - name: Install dependencies
        run: npm install

      - name: Build
        run: npm build

      - name: Deploy
        id: deployment
        run: npm deploy
```

---
layout: image-right
image: bitbucket-pipeline.png
---

# Real world examples

What do Aligent use pipelines for?
- Deployments
- Testing
- Code standards
- Security checks

---
layout: statement
---

# Demo

---

# Future optimistations

- Parallel steps
- Stricter test criteria
- Security scanning

---
layout: default
---

# Extra Resources

- [Demo GitHub Repo]()
- [Fireship Video on GitHub Actions](https://www.youtube.com/watch?v=yfBtjLxn_6k)
- [My Personal Website](https://danielvdp.com)
- [Email Me](mailto:danielvdp56@gmail.com)

