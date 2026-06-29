# 📘 Topic 23 - Git Status
# Git Status

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Git Status क्या है?
- Git Status की आवश्यकता क्यों होती है?
- Working Directory की स्थिति कैसे देखें?
- Staged और Unstaged Changes कैसे पहचानें?
- Untracked Files क्या होती हैं?
- Production में Git Status का उपयोग

---

# Git Status क्या है?

Git Status एक Command है जो Repository की वर्तमान स्थिति (Current State) दिखाती है।

यह बताती है

✔ कौन-सी Files बदली हैं

✔ कौन-सी Files Stage में हैं

✔ कौन-सी Files Commit होने वाली हैं

✔ कौन-सी Files Git Track नहीं कर रहा

---

# आसान उदाहरण

मान लो

Project

```
README.md

main.tf

variables.tf
```

तुमने

```
main.tf
```

में बदलाव किया।

अब

```bash
git status
```

चलाओ।

Git बताएगा

```
modified : main.tf
```

---

# Basic Command

```bash
git status
```

Example Output

```
On branch main

Changes not staged for commit

modified: README.md
```

---

# Git Status किन-किन चीज़ों को दिखाता है?

Git Status हमें बताता है

✔ Current Branch

✔ Modified Files

✔ Staged Files

✔ Untracked Files

✔ Merge Conflict

✔ Rebase Progress

✔ Clean Working Tree

---

# Untracked Files

नई File बनाई

```
notes.md
```

अभी

```bash
git add
```

नहीं किया।

Status

```
Untracked files

notes.md
```

---

# Staged Files

अब

```bash
git add notes.md
```

Status

```
Changes to be committed

new file: notes.md
```

---

# Modified Files

अगर

Stage करने के बाद

फिर से File बदल दी

तो

Status

```
Modified
```

भी दिखाएगा।

---

# Clean Working Tree

सब Commit हो गया।

Status

```
nothing to commit

working tree clean
```

यानी

Repository पूरी तरह Clean है।

---

# Short Status

```bash
git status -s
```

Example

```
M README.md

A notes.md

?? test.txt
```

Meaning

```
M = Modified

A = Added

?? = Untracked
```

---

# Git Status Workflow

```
File Create

↓

git status

↓

Untracked

↓

git add

↓

git status

↓

Staged

↓

git commit

↓

git status

↓

Working Tree Clean
```

---

# Real Industry Example

Deployment से पहले

Senior Engineer हमेशा

```bash
git status
```

चलाता है।

अगर कोई Extra File दिखाई देती है,

तो पहले उसे Review किया जाता है।

फिर ही Commit या Push होता है।

---

# Common Mistakes

❌ Status देखे बिना Commit करना।

❌ Secret File Commit कर देना।

❌ Untracked Files भूल जाना।

❌ Merge Conflict Ignore करना।

---

# Best Practices

✔ हर Commit से पहले

```bash
git status
```

चलाएँ।

✔ हर Push से पहले

```bash
git status
```

देखें।

✔ Working Tree Clean रखें।

✔ Untracked Files Review करें।

---

# 🏭 Production Note

Enterprise Projects में

लगभग हर Git Command से पहले

```
git status
```

चलाना अच्छी आदत मानी जाती है।

इससे गलत Files Commit होने से बच जाती हैं।

---

# Interview Questions

Q1. Git Status क्या है?

Q2. Untracked File क्या होती है?

Q3. Working Tree Clean का क्या मतलब है?

Q4. git status -s क्या करता है?

Q5. Git Status Production में क्यों महत्वपूर्ण है?

---

# 🧠 Quick Revision

```
git status

↓

Current Branch

↓

Modified Files

↓

Staged Files

↓

Untracked Files

↓

Repository Status
```

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Git Status

✔ Working Tree

✔ Staged Files

✔ Untracked Files

✔ Short Status

✔ Production Workflow

अगले Chapter में हम Git Diff सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Git Log

➡ Next: Git Diff

----

# 🔥 Important Note / Git Status कोई बदलाव नहीं करता

Git Status केवल Repository की वर्तमान स्थिति दिखाता है।

यह किसी File या Commit में कोई बदलाव नहीं करता।

इसी कारण इसे पूरी तरह Safe Command माना जाता है।

---

# 🔥 Real Production Scenario Production Deployment Checklist

मान लो

तुम Production Deployment करने वाले हो।

Deploy करने से पहले

```bash
git status
```

चलाया।

Output

```
modified: .env

modified: terraform.tfvars
```

अब तुम्हें तुरंत पता चल गया कि अभी Local Changes मौजूद हैं।

अगर बिना देखे Push कर देते,

तो Sensitive Information या अधूरा Code Production में जा सकता था।

इसीलिए Enterprise Teams में Deployment से पहले `git status` चलाना Standard Practice है।

---

# 💻 Practical

Repository की स्थिति देखें

git status

Short Status

git status -s

नई File बनाएँ

touch demo.txt

Status देखें

git status

Stage करें

git add demo.txt

फिर देखें

git status

Commit करें

git commit -m "Add demo file"

अंत में

git status

Output

On branch main

nothing to commit, working tree clean

-----


# 🚀 Topic Complete होने के बाद

git add .

git commit -m "docs(git): add git status documentation"

git push

---

# 💡 Senior Engineer Tip (Golden Habit)

एक आदत बना लो:

Code लिखा

↓

git status

↓

git add

↓

git status

↓

git commit

↓

git status

↓

git push

↓

git status

अगर तुम्हारा git status अंत में हमेशा यह दिखाए:

nothing to commit, working tree clean

तो समझो तुमने Professional तरीके से अपना Git Workflow पूरा किया है।

----

# 🧠 10 सेकंड का Interview Answer

अगर Interviewer पूछे:

"git status का उपयोग क्या है?"

तो सीधे बोलना:

git status Git Repository की वर्तमान स्थिति दिखाता है। इससे Current Branch, Modified Files, Staged Files, Untracked Files और Working Tree की स्थिति पता चलती है। यह Commit या Push से पहले Repository Verify करने के लिए सबसे अधिक उपयोग की जाने वाली Git Command है।
---