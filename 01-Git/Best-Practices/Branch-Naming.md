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