यह छोटा Topic है, लेकिन हर Developer और DevOps Engineer के लिए Mandatory है। इसमें सीखोगे कि किन Files को Git में कभी Track नहीं करना चाहिए, जैसे:

.env
terraform.tfstate
*.log
node_modules
__pycache__
Secrets & Credentials

यही Topic Repository को Professional और Secure बनाता है। 🔥

अगर .gitignore नहीं है तो समझो Repository Professional नहीं है।

Azure, Terraform, Docker, Python, Linux, DevOps — हर जगह इसका उपयोग होता है।

# 📘 Topic 21 - Git Ignore

# Git Ignore

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Git Ignore क्या है?
- इसकी आवश्यकता क्यों होती है?
- .gitignore File कैसे बनाते हैं?
- Common Ignore Patterns
- Terraform, Python, Linux और Azure Projects में इसका उपयोग
- Production Best Practices

---

# Git Ignore क्या है?

Git Ignore एक Special File है

```
.gitignore
```

जिसमें हम उन Files और Folders के नाम लिखते हैं जिन्हें Git Track नहीं करेगा।

यानी

वे Files Local Machine पर रहेंगी,

लेकिन Git Repository में Add नहीं होंगी।

---

# Git Ignore की आवश्यकता क्यों होती है?

हर File Repository में Store करना सही नहीं होता।

कुछ Files

✔ Temporary होती हैं।

✔ Automatically Generate होती हैं।

✔ Secrets रखती हैं।

✔ Logs होती हैं।

✔ Cache Files होती हैं।

ऐसी Files को Ignore किया जाता है।

---

# आसान उदाहरण

मान लो Project में

```
Project

│

├── app.py

├── README.md

├── .env

├── terraform.tfstate

├── debug.log

└── .gitignore
```

अगर

```
.gitignore
```

में

```
.env

*.log

terraform.tfstate
```

लिख दिया,

तो Git इन Files को Track नहीं करेगा।

---

# Git Ignore File कैसे बनाएं?

```bash
touch .gitignore
```

Windows

```bash
echo. > .gitignore
```

---

# Common Patterns

सभी Log Files

```text
*.log
```

Environment File

```text
.env
```

Python Cache

```text
__pycache__/
```

Terraform State

```text
*.tfstate
```

VS Code

```text
.vscode/
```

Linux Swap

```text
*.swp
```

Temporary Files

```text
tmp/
```

---

# Example .gitignore

```text
# Logs

*.log

# Environment

.env

# Terraform

*.tfstate

*.tfstate.backup

.terraform/

# VS Code

.vscode/

# Python

__pycache__/

*.pyc

# Temporary

tmp/

cache/
```

---

# Git Ignore कैसे काम करता है?

Git केवल Untracked Files पर Ignore Rule लागू करता है।

अगर कोई File पहले से Track हो रही है,

तो केवल .gitignore में नाम लिखने से वह Ignore नहीं होगी।

---

# Track हो चुकी File को Ignore कैसे करें?

पहले Git Index से हटाएँ

```bash
git rm --cached filename
```

फिर

.gitignore में Add करें।

अब वह Future में Track नहीं होगी।

---

# Real Industry Example

Terraform Project

```
terraform.tfstate
```

में Cloud Infrastructure की जानकारी होती है।

इस File को GitHub पर Push नहीं करना चाहिए।

इसे हमेशा

```
.gitignore
```

में रखें।

---

# Azure DevOps Example

```
.env
```

में

Client Secret

Password

API Key

Token

हो सकते हैं।

अगर इसे Push कर दिया,

तो Security Risk बन जाएगा।

---

# Common Mistakes

❌ .env Push कर देना।

❌ terraform.tfstate Commit कर देना।

❌ Password वाली Files Repository में डाल देना।

❌ Large Log Files Commit करना।

---

# Best Practices

✔ Secret Files Ignore करें।

✔ Logs Ignore करें।

✔ Cache Ignore करें।

✔ IDE Files Ignore करें।

✔ Terraform State Ignore करें।

✔ Credentials कभी Commit न करें।

---

# 🏭 Production Note

Enterprise Projects में

Repository Create करते ही

सबसे पहले

```
.gitignore
```

Configure किया जाता है।

इसके बिना Repository Production Ready नहीं मानी जाती।

---

# Interview Questions

Q1. .gitignore क्या है?

Q2. Git Ignore कब उपयोग करते हैं?

Q3. Tracked File को Ignore कैसे करेंगे?

Q4. Terraform में कौन-सी Files Ignore करनी चाहिए?

Q5. .env File को GitHub पर क्यों नहीं Push करना चाहिए?

---

# 🧠 Quick Revision

```
.gitignore

↓

Git Ignore Rules

↓

Sensitive Files

↓

Git Track नहीं करेगा
```

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ .gitignore

✔ Ignore Patterns

✔ Tracked File Remove

✔ Security

✔ Production Best Practices

अगले Chapter में हम Git Log सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Cherry-pick

➡ Next: Git Log

-----

# 🔥 Important Note .gitignore पहले बनाएं, बाद में Coding करें

Production Projects में Repository Create करते ही

सबसे पहले

.gitignore

बनाई जाती है।

इससे गलती से Secret Files, Logs और Temporary Files GitHub पर Push नहीं होतीं।

# 🔥  Real Production Scenario Terraform Project Security

मान लो

तुम Azure Infrastructure Terraform से Deploy कर रहे हो।

Project में ये Files हैं:

```
main.tf

variables.tf

terraform.tfvars

terraform.tfstate
```

अगर

```
terraform.tfstate
```

GitHub पर Push हो गई,

तो Infrastructure की Sensitive Information Repository में चली जाएगी।

इसीलिए Production Projects में हमेशा

```
*.tfstate

.terraform/

terraform.tfstate.backup
```

को `.gitignore` में रखा जाता है।

इसी तरह

```
.env
```

में Password, API Keys और Client Secrets हो सकते हैं।

उन्हें भी कभी Commit नहीं करना चाहिए।

----

# 💻 Practical

नई .gitignore File बनाएं

touch .gitignore

Sample Content

*.log
.env
.vscode/
.terraform/
*.tfstate
__pycache__/

Status देखें

git status

अगर File पहले से Track हो रही है

git rm --cached .env

Commit करें

git add .

git commit -m "Add .gitignore rules"

Push करें

git push

---

# 🚀 Topic Complete होने के बाद

git add .

git commit -m "docs(git): add gitignore documentation"

git push

----

# 💡 Senior Engineer Tip (Golden Rule)

यह Rule हमेशा याद रखना:

Code GitHub पर Push करो.

Secrets कभी Push मत करो.

और यह छोटी-सी List हमेशा याद रखो:

✅ Ignore करो

.env
*.log
*.tfstate
.terraform/
.vscode/
__pycache__/
node_modules/
❌ Push करो

README.md
Source Code
Terraform Files (.tf)
YAML Pipelines
Documentation
Scripts

----

# 🧠 10 सेकंड का Interview Answer

अगर Interviewer पूछे:

".gitignore क्या है और इसका उपयोग क्यों किया जाता है?"

तो सीधे बोलना:

.gitignore एक Special File है जो Git को बताती है कि किन Files और Directories को Track नहीं करना है। इसका उपयोग Logs, Cache, Temporary Files, IDE Files, Terraform State Files और Sensitive Information जैसे .env को Repository से बाहर रखने के लिए किया जाता है। Enterprise Projects में यह Security और Repository Cleanliness के लिए आवश्यक होता है।

----