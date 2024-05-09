---
theme: dracula
coverAuthor: Aligent - Daniel van der Ploeg
coverDate:
image: '/background.jpg'
layout: intro
transition: slide-left
---

# Demystifying DevOps

Automating Web Deployment with GitHub Pipelines

<!-- prettier-ignore-start -->

---
layout: image-right
image: technologist.svg
---
<!-- prettier-ignore-end -->

# Who am I?

- DevOps Engineer at Aligent
- Degree in Information Technology (Software Development)
- Previous job was a hybrid tech role
  - Full stack developer
  - SysAdmin
  - Coffee machine repair man ☕

<!-- prettier-ignore-start -->

---
layout: image-right
image: pipelines.jpg
---
<!-- prettier-ignore-end -->

# What is a DevOps Engineer?

- Bridge the gap between developers and operations
- Continuous Integration / Continuous deployment (CI/CD)
- Work closely with developers to automate processes
- Responsible for hosting infrastructure

<!-- prettier-ignore-start -->

---
layout: default
---
<!-- prettier-ignore-end -->

# Assumed Knowledge     

**git**: pushing, merging & pull requests and rebase    

```bash
# Git commands
git pull
git checkout
git add .
git commit
git push
git rebase
```

**npm**: install third party dependencies, run custom scripts    

```bash
nvm use
npm install react
npm ci
npm run ${custom_command}
```

**bash** scripting

<!-- prettier-ignore-start -->

---
layout: two-cols
---
<!-- prettier-ignore-end -->

# What are pipelines?

- Run commands in specific order
- Generally written in yaml

<br>

## What problems do they solve?

- Automate common tasks
  - Save developer (and operations) time
- Keep processes uniform
- Prevent "bad" code from being deployed to production

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
        run: npm ci

      - name: Build
        run: npm run build

      - name: Deploy
        id: deployment
        run: npm run deploy
```

<!-- prettier-ignore-start -->

---
layout: image-right
image: bitbucket-pipeline-01.png
---
<!-- prettier-ignore-end -->

# Real world examples

What do Aligent use pipelines for?

- Deployments
- Testing
- Code standards
- Security checks

<!-- prettier-ignore-start -->

---
layout: statement
---
<!-- prettier-ignore-end -->

# Demo

---

# Future optimistations

<v-click>
<ul>
  <li>Parallel steps</li>
  <li>Stricter test criteria</li>
  <li>Security scanning</li>
  <li>Lock node version to 18</li>
</ul>

</v-click>

<!-- prettier-ignore-start -->

---
layout: image-right
image: qr-code.svg
---
<!-- prettier-ignore-end -->

# Additional Resources

- [Demo GitHub Repo](https://github.com/TheOrangePuff/pipeline-presentation)
- [Fireship Video on GitHub Actions](https://www.youtube.com/watch?v=yfBtjLxn_6k)
- [Fireship Video - DevOps CI/CD Explained in 100 Seconds](https://www.youtube.com/watch?v=scEDHsr3APg)
- Get in contact 🤠
  - [My Personal Website](https://danielvdp.com)
  - [Email Me](mailto:danielvdp56@gmail.com)
