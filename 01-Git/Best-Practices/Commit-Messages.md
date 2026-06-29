# Commit Messages Best Practices

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे

- Professional Commit Messages
- Good vs Bad Commit Messages
- Conventional Commits
- Enterprise Standards
- Real Examples

---

# Commit Message क्या होना चाहिए?

Commit Message छोटा,

स्पष्ट,

और Meaningful होना चाहिए।

कोई भी Developer

6 महीने बाद भी Commit देखकर समझ जाए

कि क्या बदलाव किया गया था।

---

# Bad Examples

```
update

changes

work

done

test

fix

new

latest

abc
```

ऐसे Commit Messages कभी उपयोग न करें।

---

# Good Examples

```
Add Azure Virtual Network configuration

Fix NSG priority issue

Update Terraform variables

Create Dockerfile for Nginx

Configure Azure DevOps Pipeline

Add GitHub SSH authentication guide
```

---

# Standard Format

```
<type>: <short description>
```

Example

```
feat: add Azure VNet module

fix: resolve firewall policy issue

docs: update README

refactor: optimize Terraform module

test: add pipeline test cases
```

---

# Conventional Commit Types

| Type | Purpose | Example |
|------|----------|---------|
| feat | New Feature | feat: add Azure Bastion |
| fix | Bug Fix | fix: resolve SSH issue |
| docs | Documentation | docs: update Git notes |
| style | Formatting | style: format README |
| refactor | Improve Code | refactor: simplify module |
| test | Testing | test: add pipeline tests |
| chore | Maintenance | chore: update .gitignore |
| ci | CI/CD Changes | ci: update Azure Pipeline |
| build | Build Changes | build: update Docker image |
| perf | Performance | perf: optimize Terraform |

---

# Azure Examples

```
feat: create virtual network

feat: deploy Azure Firewall

fix: correct NSG priority

docs: add Azure networking notes
```

---

# Terraform Examples

```
feat: add VNet module

feat: create backend configuration

fix: update variable type

refactor: split modules

docs: add Terraform examples
```

---

# Azure DevOps Examples

```
feat: create YAML pipeline

ci: update build pipeline

fix: service connection issue

docs: add pipeline documentation
```

---

# Docker Examples

```
feat: add Dockerfile

feat: create docker-compose

fix: reduce image size
```

---

# Kubernetes Examples

```
feat: deploy nginx

feat: add ingress controller

fix: update deployment manifest
```

---

# Documentation Examples

```
docs: add Git notes

docs: update Linux README

docs: add networking diagrams
```

---

# Good vs Bad

❌

```
update files
```

✔

```
docs: update GitHub documentation
```

---

❌

```
fixed bug
```

✔

```
fix: resolve Azure Firewall rule conflict
```

---

❌

```
terraform changes
```

✔

```
feat: create reusable Terraform VNet module
```

---

# Writing Rules

✔ Use Present Tense

✔ Keep First Letter Lowercase (after type)

✔ Keep Message Short

✔ Describe What Changed

✔ One Commit = One Purpose

---

# Avoid

❌ Final Update

❌ Last Commit

❌ New Changes

❌ Testing

❌ Misc Update

❌ Work Done

---

# Best Practices

✔ Small Commit

✔ Clear Message

✔ Follow Conventional Commits

✔ Commit Frequently

✔ Don't Mix Multiple Changes

---

# Real Examples

```
feat: add Azure Bastion deployment

feat: create AKS cluster

fix: resolve Terraform backend issue

docs: update SSH guide

refactor: split networking module

ci: update Azure DevOps pipeline

chore: remove unused files
```

---

# Summary

एक अच्छा Commit Message

✔ छोटा होता है

✔ स्पष्ट होता है

✔ Meaningful होता है

✔ Future Developers के लिए आसानी से समझ आने वाला होता है।

---

# Real Commit History

feat: create Azure Virtual Network

feat: deploy Azure Bastion

feat: add NSG rules

fix: resolve subnet association issue

docs: update networking guide

refactor: split Terraform modules

ci: update Azure DevOps pipeline

chore: remove temporary files

---
