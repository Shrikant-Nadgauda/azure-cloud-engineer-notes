# Git Best Practices

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे

- Professional Git Workflow
- Enterprise Best Practices
- Common Mistakes
- Production Rules

---

# Why Best Practices Matter?

Git केवल Commands सीखने का नाम नहीं है।

Professional Engineer बनने के लिए

सही Workflow और Discipline Follow करना भी उतना ही जरूरी है।

---

# 1. Commit Frequently

✔ छोटे-छोटे Commit करें

❌ पूरा Project एक ही Commit में न डालें।

Good

```
feat: add Azure VNet

feat: add NSG

docs: update README
```

Bad

```
Final Project
```

---

# 2. Write Meaningful Commit Messages

Commit देखकर ही समझ आ जाना चाहिए

क्या Change हुआ है।

✔

```
fix: resolve SSH authentication issue
```

❌

```
update
```

---

# 3. Use Feature Branches

नई Feature के लिए हमेशा नई Branch बनाएं।

✔

```
feature/azure-vnet
```

❌

```
main
```

पर Direct Development न करें।

---

# 4. Never Commit Directly to Main

Main Branch

हमेशा Stable Code के लिए होती है।

Workflow

```
Feature Branch

↓

Pull Request

↓

Code Review

↓

Merge

↓

Main
```

---

# 5. Pull Before Push

काम शुरू करने से पहले

हमेशा Latest Changes ले लें।

```
git pull
```

इससे Merge Conflict कम होते हैं।

---

# 6. Review Before Commit

Commit करने से पहले

हमेशा देखें

```
git status
```

```
git diff
```

गलत File Commit होने से बच जाएगी।

---

# 7. Never Commit Secrets

Repository में कभी भी

❌ Password

❌ API Keys

❌ SSH Private Keys

❌ Access Tokens

Commit न करें।

इनके लिए

```
.gitignore
```

या Secret Manager उपयोग करें।

---

# 8. Keep Repository Clean

अनावश्यक Files Remove करें।

```
temp/

logs/

cache/

build/
```

Repository Professional दिखनी चाहिए।

---

# 9. Use .gitignore

इन Files को Track न करें।

```
.env

*.log

.terraform/

terraform.tfstate

node_modules/

__pycache__/
```

---

# 10. One Commit = One Purpose

एक Commit में केवल एक ही Logical Change करें।

✔

```
feat: add Azure Bastion
```

✔

```
docs: update README
```

❌

```
Azure + Docker + Linux + Terraform Changes
```

---

# 11. Delete Merged Branches

Merge होने के बाद

पुरानी Branch Delete कर दें।

Repository Clean रहती है।

---

# 12. Keep Branch Names Meaningful

✔

```
feature/login

bugfix/api

hotfix/security
```

❌

```
test

abc

new
```

---

# 13. Sync Repository Regularly

Remote Repository के साथ

Repository को Updated रखें।

```
git fetch

git pull
```

---

# 14. Use Tags for Releases

Version Track करने के लिए

```
v1.0

v1.1

v2.0
```

Tags का उपयोग करें।

---

# 15. Always Test Before Push

Code

↓

Build

↓

Test

↓

Push

यही Professional Workflow है।

---

# Common Mistakes

❌ Push Without Testing

❌ Huge Commits

❌ Direct Push to Main

❌ Random Branch Names

❌ Poor Commit Messages

❌ Secrets in Repository

❌ Ignoring Merge Conflicts

---

# Production Checklist

✅ Pull Latest Code

✅ Create Feature Branch

✅ Make Changes

✅ Review Changes

✅ Commit

✅ Push

✅ Create Pull Request

✅ Code Review

✅ Merge

---

# Daily Git Workflow

```
git pull

↓

git checkout -b feature/task

↓

Code

↓

git status

↓

git add .

↓

git commit

↓

git push

↓

Pull Request

↓

Merge
```

---

# Senior Engineer Tips

✔ Commit Small

✔ Push Often

✔ Review Before Commit

✔ Never Force Push on Main

✔ Never Share Secrets

✔ Delete Old Branches

✔ Follow Team Standards

✔ Keep History Clean

---

# Summary

Professional Git केवल Commands जानने से नहीं आता।

Professional Git आता है

Discipline,

Clean History,

Meaningful Commits,

Proper Branching,

और Team Collaboration से।