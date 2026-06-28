# Push

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Push क्या होता है?
- Push की आवश्यकता क्यों होती है?
- Push कैसे करते हैं?
- First Push क्या होता है?
- Upstream Branch क्या होती है?
- Force Push क्या है?
- Real Industry Example

---

# Push क्या होता है?

Push का अर्थ है

> Local Repository के Commits को Remote Repository पर भेजना।

जब तक Push नहीं करते,

तब तक तुम्हारे Commits केवल तुम्हारे Computer में रहते हैं।

---

# आसान उदाहरण

तुमने Laptop पर

✔ File बनाई

✔ Commit किया

लेकिन GitHub खोला...

कुछ भी दिखाई नहीं दिया।

क्यों?

क्योंकि अभी तक

```
git push
```

नहीं किया।

---

# Git Push Workflow

```
Working Directory

↓

Staging Area

↓

Commit

↓

git push

↓

GitHub Repository
```

---

# Basic Push

```bash
git push
```

अगर Upstream पहले से सेट है,

तो यही Command पर्याप्त है।

---

# First Push

अगर पहली बार Branch Push कर रहे हो,

तो

```bash
git push -u origin main
```

यहाँ

```
-u
```

का अर्थ है

Upstream Branch Set करना।

इसके बाद केवल

```bash
git push
```

चलाना होगा।

---

# Upstream क्या होता है?

Git को पता होना चाहिए कि

Local Branch

```
main
```

का संबंध

किस Remote Branch से है।

उदाहरण

```
main

↓

origin/main
```

यह Mapping Upstream कहलाती है।

---

# Verification

देखें कि Branch Track हो रही है या नहीं।

```bash
git branch -vv
```

Output

```
main

origin/main
```

---

# Multiple Branch Push

Feature Branch

```bash
git push -u origin feature-login
```

अब यह Branch GitHub पर भी दिखाई देगी।

---

# Force Push

```bash
git push --force
```

या

```bash
git push -f
```

यह Remote History को बदल सकता है।

⚠ इसका उपयोग बहुत सावधानी से करें।

---

# Real Industry Example

Developer

↓

Feature Complete

↓

Commit

↓

Push

↓

GitHub

↓

Pull Request

↓

Code Review

↓

Merge

↓

Deployment

---

# Common Mistakes

❌ Commit किए बिना Push करना।

❌ Wrong Branch Push करना।

❌ Main Branch पर सीधे Push करना।

❌ Force Push का गलत उपयोग करना।

---

# Best Practices

✔ Push से पहले

```bash
git status
```

देखें।

✔ Branch Verify करें।

```bash
git branch
```

✔ Latest Changes लें।

```bash
git pull
```

✔ Force Push से बचें।

---

# 🏭 Production Note

Enterprise Projects में Developers

सीधे Main Branch पर Push नहीं करते।

Workflow

Feature Branch

↓

Push

↓

Pull Request

↓

Code Review

↓

Merge

↓

Deployment

---

# Interview Questions

Q1. Git Push क्या है?

Q2. First Push में -u क्यों उपयोग करते हैं?

Q3. Upstream Branch क्या होती है?

Q4. Force Push कब उपयोग करना चाहिए?

Q5. Production में Main Branch पर Direct Push क्यों नहीं करते?

---

# 🧠 Quick Revision

```
File

↓

Commit

↓

git push

↓

GitHub
```

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Push

✔ First Push

✔ Upstream

✔ Force Push

✔ Production Workflow

अगले Chapter में हम Pull सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Clone

➡ Next: Pull

---

# 🔥 Push और Commit में अंतर

बहुत से Beginners सोचते हैं कि Commit करते ही Code GitHub पर पहुँच जाता है।

ऐसा नहीं है।

```
Commit
```

Code केवल Local Repository में सेव करता है।

```
Push
```

उसी Commit को Remote Repository (GitHub) पर भेजता है।

याद रखें:

Commit = Local Save

Push = GitHub पर Upload


---

# 🔥 एक Real Scenario अगर Push न करें तो क्या होगा?


मान लो तुमने पूरे दिन 25 Commit किए।

लेकिन Push नहीं किया।

अब Laptop Crash हो गया।

तो क्या होगा?

अगर Repository केवल Local थी,

तो सारे नए Commits खो सकते हैं।

अगर समय-समय पर Push करते रहते,

तो सभी Commits GitHub पर सुरक्षित रहते।

इसीलिए Production में Engineers नियमित रूप से Push करते हैं।

---

# 💻 Practical (तुम्हारे Current Repository पर)

- Status देखो

git status

- ** Commit करो

git add .


git commit -m "docs(git): update push notes"

- GitHub पर भेजो

git push

- अगर नई Branch है

git push -u origin feature/git-notes

- Verify

git branch -vv

---

# 🚀 Topic Complete होने के बाद

git add .

git commit -m "docs(git): add push documentation"

git push

----

# 💡 Senior Engineer Tip

एक बात हमेशा याद रखना:

git add     → Changes तैयार करता है

git commit  → Changes Local Git में सेव करता है

git push    → Changes GitHub पर भेजता है

- यही Git का Golden Flow है:

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
GitHub Repository

# 🔥 अगला Topic 14-Pull.md होगा।
---

