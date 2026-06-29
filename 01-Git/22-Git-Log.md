# 📘 Topic 22 - Git Log

# Git Log

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Git Log क्या है?
- Git Log की आवश्यकता क्यों होती है?
- Git Log के महत्वपूर्ण Options
- Commit History कैसे देखें?
- किसी Specific User या Date के Commits कैसे देखें?
- Production में Git Log का उपयोग

---

# Git Log क्या है?

Git Log एक Command है जिसका उपयोग Repository की पूरी Commit History देखने के लिए किया जाता है।

यह हमें बताती है

✔ किसने Commit किया

✔ कब किया

✔ किस Commit का ID क्या है

✔ Commit Message क्या है

---

# आसान उदाहरण

मान लो Repository में

Developer A

↓

Developer B

↓

Developer C

ने अलग-अलग Commits किए।

अगर हमें पूरी History देखनी है

तो

```bash
git log
```

चलाएंगे।

---

# Basic Command

```bash
git log
```

Output

```
commit 4b2f3a8c

Author: Shrikant

Date: Sun Jun 28

Add Terraform Modules
```

---

# Compact History

```bash
git log --oneline
```

Output

```
8ab4512 Add Azure Notes

4cd5121 Add Terraform

91af111 Initial Commit
```

यह सबसे ज़्यादा उपयोग होने वाला Format है।

---

# Graph के साथ History

```bash
git log --oneline --graph
```

Output

```
* 8ab4512 Add Azure

* 4cd5121 Add Terraform

* 91af111 Initial Commit
```

अगर Branches होंगी,

तो Graph उन्हें भी दिखाएगा।

---

# सभी Branch की History

```bash
git log --all --graph --oneline
```

यह Command Enterprise Projects में बहुत उपयोग होती है।

---

# केवल Last 5 Commits

```bash
git log -5
```

या

```bash
git log --oneline -5
```

---

# किसी Specific Author के Commit

```bash
git log --author="Shrikant"
```

---

# किसी Date के बाद के Commit

```bash
git log --since="7 days ago"
```

या

```bash
git log --since="2026-06-01"
```

---

# किसी Date तक के Commit

```bash
git log --until="2026-06-30"
```

---

# किसी File की History

```bash
git log README.md
```

अब केवल उसी File के Commits दिखेंगे।

---

# किसी Commit की Details

```bash
git show <commit-id>
```

उदाहरण

```bash
git show a7d4521
```

---

# Real Industry Example

Production Server पर Bug आया।

Manager पूछता है

"यह File किसने बदली?"

Developer

```bash
git log app.py
```

चलाता है।

अब तुरंत पता चल जाता है

कि किस Commit में बदलाव हुआ था।

---

# Common Mistakes

❌ केवल git log देखकर Exit करना भूल जाना।

(Exit के लिए)

```
q
```

दबाएँ।

❌ Commit ID Copy गलत करना।

❌ History Verify किए बिना Reset करना।

---

# Best Practices

✔ हमेशा

```bash
git log --oneline
```

से शुरुआत करें।

✔ बड़ी Repository में

```bash
git log --graph --all
```

उपयोग करें।

✔ Commit Message Meaningful रखें।

---

# 🏭 Production Note

Enterprise Projects में

Code Review

Bug Investigation

Audit

Release Verification

सबकी शुरुआत

```
git log
```

से होती है।

---

# Interview Questions

Q1. Git Log क्या है?

Q2. git log --oneline क्या करता है?

Q3. Graph Option क्यों उपयोग करते हैं?

Q4. किसी File की History कैसे देखेंगे?

Q5. किसी Author के Commit कैसे देखेंगे?

---

# 🧠 Quick Revision

```
git log

↓

Commit History

↓

Author

↓

Date

↓

Commit ID

↓

Message
```

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Git Log

✔ Commit History

✔ Oneline

✔ Graph

✔ Author Filter

✔ Date Filter

✔ File History

अगले Chapter में हम Git Status सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Git Ignore

➡ Next: Git Status


----

# 🔥 Important Note Git Log केवल History दिखाता है

Git Log Repository में कोई बदलाव नहीं करता।

यह केवल Commit History को Read करता है।

इसलिए इसे Safe Command माना जाता है।

-----

# 🔥 Real Production Scenario / Production Investigation

मान लो

Production Server पर Application Error आ रही है।

Manager पूछता है

"पिछले 24 घंटे में किसने बदलाव किए?"

Developer Commands चलाता है

```bash
git log --since="1 day ago" --oneline
```

फिर

```bash
git show <commit-id>
```

अब तुरंत पता चल जाता है

- किस Developer ने Commit किया
- क्या बदलाव हुए
- कब हुए

यही तरीका Enterprise Teams में Root Cause Analysis (RCA) के दौरान उपयोग किया जाता है।

---

# 💻 Practical

- पूरी History देखें

git log

- Compact History

git log --oneline

- Graph के साथ

git log --oneline --graph

- सभी Branches

git log --all --graph --oneline

- Last 5 Commits

git log --oneline -5

- README की History

git log README.md

-  Commit Details

git show HEAD

या

git show <commit-id>


-----

# 🚀 Topic Complete होने के बाद

git add .

git commit -m "docs(git): add git log documentation"

git push

-----

# 💡 Senior Engineer Tip (Golden Commands)

- ये 5 Commands लगभग हर DevOps Engineer रोज़ उपयोग करता है:

git log --oneline

git log --oneline --graph

git log --all --graph --oneline

git show HEAD

git log README.md

---

# 🧠 10 सेकंड का Interview Answer

अगर Interviewer पूछे:

"Git Log क्या है?"

तो बोलना:

git log का उपयोग Git Repository की Commit History देखने के लिए किया जाता है। इससे Commit ID, Author, Date और Commit Message देखे जा सकते हैं। Production में इसका उपयोग Bug Investigation, Audit, Code Review और Change Tracking के लिए किया जाता है।

---