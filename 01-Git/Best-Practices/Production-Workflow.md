# Production Git Workflow

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे

- Enterprise Git Workflow
- Code Production तक कैसे पहुँचता है?
- Developer का Daily Workflow
- Production Best Practices

---

# Production Workflow क्या है?

Production Workflow वह Standard Process है

जिसके माध्यम से Code

Developer के Computer से

Production Environment तक पहुँचता है।

Enterprise Companies

हमेशा एक Defined Workflow Follow करती हैं।

---

# Complete Workflow

```
Requirement

↓

Create Feature Branch

↓

Development

↓

Commit Changes

↓

Push to Remote

↓

Create Pull Request

↓

Code Review

↓

Approval

↓

Merge

↓

CI/CD Pipeline

↓

Testing

↓

Production Deployment
```

---

# Step 1

Requirement

Developer को नया Task मिलता है।

Example

```
Create Azure Virtual Network
```

---

# Step 2

Create Feature Branch

```
feature/azure-vnet
```

---

# Step 3

Development

Developer

Code लिखता है।

Testing करता है।

---

# Step 4

Commit

Meaningful Commit

```
feat: create Azure Virtual Network
```

---

# Step 5

Push

Code

Remote Repository में भेजा जाता है।

---

# Step 6

Pull Request

Developer

Review के लिए Request भेजता है।

---

# Step 7

Code Review

Senior Engineer

Code Review करता है।

Suggestions देता है।

---

# Step 8

Approval

Review Complete होने के बाद

Approval मिलता है।

---

# Step 9

Merge

Feature Branch

Main या Develop में Merge होती है।

---

# Step 10

CI/CD Pipeline

Pipeline Automatically

Build

↓

Test

↓

Deploy

करती है।

---

# Step 11

Testing

QA Team

या Automated Testing

Application Verify करती है।

---

# Step 12

Production

Application

Production में Deploy हो जाती है।

---

# Real Example

Developer

↓

feature/terraform-vnet

↓

Commit

↓

Push

↓

Pull Request

↓

Review

↓

Merge

↓

Azure DevOps Pipeline

↓

Terraform Apply

↓

Azure Resources Created

---

# Production Rules

✔ Feature Branch पर काम करें

✔ Main पर Direct Push न करें

✔ Pull Request Mandatory

✔ Code Review Mandatory

✔ Automated Testing

✔ CI/CD Pipeline

✔ Version Tags

---

# Common Mistakes

❌ Direct Push to Main

❌ No Code Review

❌ Large Commits

❌ Skip Testing

❌ Ignore Pipeline Failures

---

# Enterprise Workflow

```
Developer

↓

GitHub

↓

Pull Request

↓

Review

↓

Merge

↓

Azure DevOps

↓

Terraform

↓

Azure

↓

Production
```

---

# Summary

Production में

कोई भी Developer

Direct Production में Code Deploy नहीं करता।

हर Change

Review,

Approval,

Testing,

और CI/CD Pipeline

से होकर गुजरती है।

यही Professional Software Development Process है।

---

# ⭐ Real Enterprise Scenario

Task Received

↓

Azure DevOps Board

↓

Developer creates

feature/azure-vnet

↓

Development

↓

Commit

↓

Push

↓

Pull Request

↓

Reviewer Approval

↓

Merge

↓

Pipeline Starts

↓

Terraform Plan

↓

Terraform Apply

↓

Azure Infrastructure Created

↓

QA Testing

↓

Production

---


# 💡 Senior Engineer Notes

✔ Never Push Directly to Main

✔ Every Change Must Be Reviewed

✔ Every Merge Should Trigger CI/CD

✔ Production Deployment Should Be Automated

✔ Every Release Should Have a Tag

---