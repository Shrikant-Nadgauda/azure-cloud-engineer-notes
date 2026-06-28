# Commit

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Commit क्या होता है?
- Commit क्यों आवश्यक है?
- git commit क्या करता है?
- Commit Message कैसे लिखें?
- Real Industry Example

---

# Commit क्या है?

Commit Git में एक Snapshot होता है।

जब हम Commit करते हैं,

तो Git उस समय Project की सभी Staged Files की एक Permanent Copy (Snapshot) अपनी History में Save कर देता है।

सरल भाषा में,

> Commit = Project की उस समय की तस्वीर (Snapshot)

---

# आसान उदाहरण

मान लो तुम एक किताब लिख रहे हो।

हर दिन थोड़ा-थोड़ा लिखते हो।

अगर रोज़ एक PDF Save कर लो,

तो बाद में किसी भी दिन वाली PDF खोल सकते हो।

Git भी बिल्कुल यही करता है।

हर Commit Project का एक नया Version बना देता है।

---

# Git Workflow

```
Working Directory
        │
    git add
        │
 Staging Area
        │
  git commit
        │
 Local Repository
        │
   git push
        │
    GitHub
```

Commit हमेशा Staging Area की Files को Save करता है।

Working Directory की नहीं।

---

# git commit क्या करता है?

Command

```bash
git commit -m "Initial project setup"
```

इसका मतलब

Git को बताना:

> "जो Files मैंने Stage की हैं,
> उन्हें इस Message के साथ History में Save कर दो।"

---

# Commit Message क्या होती है?

Commit Message बताती है कि

उस Commit में क्या बदलाव किए गए हैं।

उदाहरण

✔ Good

```text
Add Azure VNet deployment
```

```text
Fix Terraform variable validation
```

```text
Update README documentation
```

---

❌ Bad

```text
Update
```

```text
Changes
```

```text
Test
```

ऐसे Messages से बाद में कुछ समझ नहीं आता।

---

# Practical

Status देखें

```bash
git status
```

Stage करें

```bash
git add .
```

Commit करें

```bash
git commit -m "Add Git commit documentation"
```

अब History देखें

```bash
git log
```

---

# Verification

Command

```bash
git log
```

Output में दिखाई देगा

```
commit a4b8f6d...

Author: Shrikant Nadgauda

Date: ...

Add Git commit documentation
```

इसका मतलब Commit Successfully बन चुका है।

---

# Commit ID (Hash)

हर Commit का एक Unique ID होता है।

उदाहरण

```
8c45af3
```

या

```
8c45af3c64f3d8a27b8d...
```

इसे Commit Hash कहते हैं।

दुनिया में दो Commits का Hash कभी समान नहीं होता।

---

# Real Industry Example

मान लो तुम Azure Infrastructure पर काम कर रहे हो।

आज तुमने केवल Virtual Network बनाया।

Commit Message

```text
Add Azure Virtual Network
```

अगले दिन NSG बनाया।

Commit Message

```text
Configure Network Security Groups
```

तीसरे दिन Bastion बनाया।

Commit Message

```text
Deploy Azure Bastion Host
```

अब अगर Bastion में Problem आए,

तो आसानी से पता चल जाएगा कि किस Commit में बदलाव हुआ था।

---

# Common Mistakes

❌ बहुत सारे Changes एक ही Commit में डाल देना।

❌ बिना Message के Commit करना।

❌ Meaningless Message लिखना।

❌ Code Test किए बिना Commit करना।

---

# Best Practices

✔ एक Feature = एक Commit

✔ Clear Commit Message लिखो।

✔ छोटे-छोटे Commits करो।

✔ Commit करने से पहले

```bash
git status
```

ज़रूर देखो।

---

# 🏭 Production Note

Enterprise Projects में Commit Messages के लिए Standard Follow किया जाता है।

उदाहरण

```text
feat: add Azure Bastion deployment
```

```text
fix: resolve Terraform variable issue
```

```text
docs: update Git documentation
```

```text
refactor: improve pipeline structure
```

इससे पूरी Team आसानी से समझ जाती है कि Commit का उद्देश्य क्या है।

---

# Interview Questions

Q1. Git Commit क्या है?

Q2. Commit और Save में क्या अंतर है?

Q3. Commit Hash क्या होता है?

Q4. git commit केवल किन Files को Save करता है?

Q5. एक अच्छे Commit Message की विशेषताएँ क्या हैं?

---

# 🧠 Quick Revision

Working Directory

↓

git add

↓

Staging Area

↓

git commit

↓

Local Repository

↓

git push

↓

GitHub

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Commit

✔ Snapshot

✔ Commit Message

✔ Commit Hash

✔ git log

✔ Industry Standard Messages

✔ Best Practices

अगले Chapter में हम Branches सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Staging Area

➡ Next: Branches

---

# 💻 Practical (अभी करके देखो)

git status

git add .

git commit -m "docs(git): add commit documentation"

git log --oneline

---

# 🚀 Topic Complete होने के बाद
git add .
git commit -m "docs(git): add commit documentation"
git push