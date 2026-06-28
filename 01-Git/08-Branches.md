# Branches

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Git Branch क्या होती है?
- Branch की आवश्यकता क्यों होती है?
- Main Branch और Feature Branch
- नई Branch कैसे बनाते हैं?
- Branch बदलना (Switch)
- Real Industry Example

---

# Branch क्या होती है?

Branch Git में Development की एक अलग Line होती है।

सरल भाषा में,

> Branch = Project की एक अलग Working Copy जहाँ हम सुरक्षित तरीके से नए Changes कर सकते हैं।

इससे Main Project प्रभावित नहीं होता।

---

# आसान उदाहरण

मान लो Company की Website Live चल रही है।

अब तुम्हें Login Page में नया Feature जोड़ना है।

अगर तुम सीधे Main Branch पर काम करोगे,

तो गलती होने पर पूरी Website प्रभावित हो सकती है।

इसलिए नई Branch बनाई जाती है।

```
main
   │
   ├─────────────── Production

feature-login
   │
   ├─────────────── नया Feature
```

काम पूरा होने के बाद ही Feature Main में Merge किया जाता है।

---

# Branch की आवश्यकता क्यों होती है?

अगर Branch नहीं होगी,

तो पूरी Team एक ही Code पर काम करेगी।

इससे

❌ Code Conflict

❌ Bugs

❌ Production Failure

हो सकते हैं।

Branch Developers को सुरक्षित वातावरण देती है।

---

# Git Branch Workflow

```
main

│

├──────── feature-login

│

├──────── feature-payment

│

├──────── feature-dashboard

│

└──────── hotfix
```

हर Developer अपनी Branch पर काम करता है।

---

# Current Branch देखें

```bash
git branch
```

Output

```
* main
```

`*` वर्तमान Branch को दिखाता है।

---

# नई Branch बनाना

```bash
git branch feature-login
```

अब Branch बन गई,

लेकिन अभी तुम उसी Branch पर नहीं गए हो।

---

# Branch बदलना

```bash
git switch feature-login
```

या

```bash
git checkout feature-login
```

अब तुम नई Branch पर काम कर रहे हो।

---

# Branch बनाकर उसी पर जाना

```bash
git switch -c feature-login
```

या

```bash
git checkout -b feature-login
```

यह सबसे ज्यादा उपयोग होने वाला तरीका है।

---

# सभी Branch देखें

```bash
git branch
```

Output

```
* feature-login

main
```

---

# Practical

Current Branch

```bash
git branch
```

नई Branch

```bash
git switch -c feature-login
```

Verify

```bash
git branch
```

Main पर वापस

```bash
git switch main
```

---

# Verification

Current Branch

```bash
git branch
```

या

```bash
git status
```

Output

```
On branch feature-login
```

---

# Real Industry Example

Azure Project

```
main
```

Production Infrastructure

```
feature-vnet
```

Azure VNet Development

```
feature-bastion
```

Azure Bastion Development

```
feature-firewall
```

Azure Firewall Configuration

सभी Engineers अलग-अलग Branch पर काम करते हैं।

काम पूरा होने के बाद Code Review होती है।

फिर Merge किया जाता है।

---

# Common Mistakes

❌ सीधे Main Branch पर Development करना।

❌ Branch Delete करना बिना Merge किए।

❌ Branch का Meaningless Name रखना।

```
test
```

```
new
```

```
abc
```

---

# Best Practices

✔ हर Feature के लिए नई Branch बनाओ।

✔ Main Branch हमेशा Stable रखो।

✔ Meaningful Branch Name रखो।

Examples

```
feature-login
```

```
feature-vnet
```

```
bugfix-firewall
```

```
hotfix-authentication
```

---

# 🏭 Production Note

Enterprise Projects में Branch Naming Standard Follow किया जाता है।

```
feature/
```

```
bugfix/
```

```
hotfix/
```

```
release/
```

Example

```
feature/azure-vnet
```

```
bugfix/nsg-rule
```

```
hotfix/login-api
```

इससे पूरी Team आसानी से समझ जाती है कि Branch किस Purpose के लिए है।

---

# Interview Questions

Q1. Git Branch क्या है?

Q2. Branch की आवश्यकता क्यों होती है?

Q3. Main Branch और Feature Branch में क्या अंतर है?

Q4. Branch Create और Switch कैसे करते हैं?

Q5. Production में Developers Main Branch पर सीधे काम क्यों नहीं करते?

---

# 🧠 Quick Revision

```
main

↓

git switch -c feature-login

↓

नई Branch

↓

Development

↓

Commit

↓

Merge

↓

main
```

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Git Branch

✔ Feature Branch

✔ Main Branch

✔ git branch

✔ git switch

✔ Branch Naming

✔ Production Workflow

अगले Chapter में हम Merge सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Commit

➡ Next: Merge

---

# 💻 Practical (अभी करके देखो)
git branch

git switch -c feature/git-notes

git branch

git status

git switch main

# 🚀 Topic Complete होने के बाद

git add .

git commit -m "docs(git): add branches documentation"

git push

---

#💡 Engineer Tip

एक छोटी-सी बात जो Beginners अक्सर Miss कर देते हैं:

Branch बनाना (git branch) और Branch पर जाना (git switch) दो अलग-अलग काम हैं।

git branch feature/login

➡️ सिर्फ Branch बनाता है।

git switch feature/login

➡️ उस Branch पर ले जाता है।

इसलिए Production में ज़्यादातर Engineers सीधे यह Command चलाते हैं:

git switch -c feature/login

एक ही Command में Branch भी बन गई और Switch भी हो गया।

---