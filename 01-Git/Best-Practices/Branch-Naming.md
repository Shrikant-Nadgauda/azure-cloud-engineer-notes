# Branch Naming Best Practices

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे

- Professional Branch Naming Convention
- अच्छे और खराब Branch Names
- Enterprise Naming Standards
- Azure DevOps / GitHub Examples

---

# Branch Naming क्या है?

Branch का नाम ऐसा होना चाहिए

जिसे देखकर बिना Branch खोले ही उसका उद्देश्य समझ आ जाए।

❌ गलत

test

new

abc

mybranch

latest

✔ सही

feature/login

bugfix/api-timeout

hotfix/security-patch

---

# Standard Naming Pattern

```
type/description
```

Example

```
feature/login-page

bugfix/payment-api

hotfix/nginx-crash
```

---

# Common Branch Prefixes

| Prefix | Purpose | Example |
|---------|----------|---------|
| feature | New Feature | feature/user-login |
| bugfix | Development Bug | bugfix/api-timeout |
| hotfix | Production Issue | hotfix/firewall-rule |
| release | Release Version | release/v2.0 |
| experiment | POC / Testing | experiment/github-actions |
| docs | Documentation | docs/readme-update |
| chore | Maintenance | chore/update-gitignore |

---

# Azure Examples

```
feature/azure-vnet

feature/azure-firewall

feature/key-vault

feature/aks-cluster

feature/load-balancer
```

---

# Terraform Examples

```
feature/terraform-module

feature/state-backend

feature/remote-backend

feature/vnet-module

feature/nsg-module
```

---

# Azure DevOps Examples

```
feature/yaml-pipeline

feature/service-connection

feature/release-pipeline

feature/variable-group
```

---

# Linux Examples

```
feature/nginx

feature/apache

feature/systemd

feature/bash-script
```

---

# Docker Examples

```
feature/dockerfile

feature/docker-compose

feature/private-registry
```

---

# Kubernetes Examples

```
feature/deployment

feature/service

feature/ingress

feature/configmap
```

---

# Monitoring Examples

```
feature/prometheus

feature/grafana

feature/alertmanager
```

---

# Documentation Examples

```
docs/git-readme

docs/network-notes

docs/terraform-guide

docs/azure-labs
```

---

# Maintenance Examples

```
chore/update-dependencies

chore/update-readme

chore/cleanup-files
```

---

# Ticket Based Naming

Enterprise Projects में

Branch Name के साथ Ticket Number भी जोड़ा जाता है।

Example

```
feature/ADO-125-create-vnet

bugfix/BUG-210-api-timeout

hotfix/INC-550-firewall
```

---

# Good Examples

```
feature/login-page

feature/payment-api

feature/terraform-module

feature/github-actions

bugfix/firewall-policy

hotfix/security-patch

release/v2.0

docs/readme

chore/update-ignore
```

---

# Bad Examples

```
test

new

abc

work

latest

branch1

temp

feature

login

azure
```

---

# Naming Rules

✔ Lowercase Letters

✔ Hyphen (-)

✔ Forward Slash (/)

✔ Short

✔ Meaningful

✔ English Only

---

# Avoid

❌ featureLogin

❌ LoginFeature

❌ MY-BRANCH

❌ final-final

❌ testing123

❌ branch-new

---

# Best Practices

✔ एक Branch = एक Feature

✔ हमेशा Prefix उपयोग करें

✔ Ticket Number हो तो Add करें

✔ छोटे नाम रखें

✔ Spaces का उपयोग न करें

✔ CamelCase Avoid करें

✔ Random Names Avoid करें

---

# Quick Examples

```
feature/login

feature/terraform

feature/azure-vnet

bugfix/api

bugfix/nginx

hotfix/firewall

release/v1.0

docs/readme

chore/gitignore

experiment/github-actions
```

---

# Summary

एक अच्छा Branch Name देखकर ही Developer समझ जाए

- यह किस काम के लिए है
- किस Technology का है
- Production है या Development
- Documentation है या Feature

---

# 50 Ready-to-Use Branch Names

feature/login-page
feature/signup-page
feature/azure-vnet
feature/aks-cluster
feature/github-actions
feature/docker-compose
feature/prometheus
feature/grafana
feature/terraform-module
feature/private-endpoint
bugfix/api-timeout
bugfix/nsg-rule
bugfix/firewall-policy
bugfix/docker-build
hotfix/prod-api
hotfix/security-patch
hotfix/ssl-certificate
release/v1.0
release/v2.0
docs/readme-update
chore/update-gitignore
experiment/aks

----

| Branch Type   | Purpose                  | Example                     |
| ------------- | ------------------------ | --------------------------- |
| `main`        | Production Code          | `main`                      |
| `develop`     | Development Integration  | `develop`                   |
| `feature/`    | New Feature              | `feature/azure-vnet`        |
| `bugfix/`     | Development Bug Fix      | `bugfix/login-error`        |
| `hotfix/`     | Production Emergency Fix | `hotfix/security-patch`     |
| `release/`    | Release Preparation      | `release/v1.0`              |
| `experiment/` | POC / Research           | `experiment/github-actions` |

---

# 💻 Practical

- नई Feature Branch

git checkout -b feature/login-page

- Bug Fix

git checkout -b bugfix/api-timeout

- Hotfix

git checkout -b hotfix/security-patch

- Release

git checkout -b release/v1.0

- Experiment

git checkout -b experiment/github-actions

सभी Branch देखें

git branch

---

# 🔥 Real Production Scenario / Branch Naming in Enterprise

मान लो Team में 50 Developers हैं।

GitHub Repository में 300 Branches बनी हुई हैं।

अगर Branches के नाम ऐसे हों:

test

new

abc

temp

तो किसी को नहीं पता चलेगा कि कौन-सी Branch किस काम के लिए है।

लेकिन अगर नाम ऐसे हों:

feature/terraform-vnet

bugfix/nsg-priority

hotfix/firewall-rule

release/v2.0

तो बिना Branch खोले ही उसका उद्देश्य समझ आ जाता है।

यही कारण है कि Enterprise Companies Branch Naming Standard को Mandatory रखती हैं।

---


💡 Senior Engineer Tips
✅ Branch Name = Task Name

अगर तुम्हारे पास Azure DevOps या Jira Ticket है:

ADO-145

तो Branch ऐसे बनाओ:

feature/ADO-145-azure-vnet

या

bugfix/ADO-210-nsg-rule

इससे Branch देखकर ही Ticket Trace हो जाती है।

✅ एक Branch = एक काम

❌ गलत:

feature/login-payment-firewall-docker

✔ सही:

feature/login
feature/payment
feature/firewall

हर Branch का केवल एक उद्देश्य होना चाहिए।

# 🧠 10 सेकंड का Interview Answer

अगर Interviewer पूछे:

"Branch Naming Convention क्यों महत्वपूर्ण है?"

तो बोलना:

Branch Naming Convention Repository को व्यवस्थित, पढ़ने योग्य और Team Collaboration के लिए आसान बनाती है। Enterprise Projects में feature/, bugfix/, hotfix/ और release/ जैसी Naming Standards का उपयोग किया जाता है ताकि Branch का उद्देश्य उसके नाम से ही स्पष्ट हो जाए।