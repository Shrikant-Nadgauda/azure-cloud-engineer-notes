# Pull

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Pull क्या होता है?
- Pull की आवश्यकता क्यों होती है?
- Pull कैसे करते हैं?
- Pull के दौरान क्या होता है?
- Pull कब करना चाहिए?
- Real Industry Example

---

# Pull क्या होता है?

Pull का अर्थ है

> Remote Repository (GitHub/Azure DevOps) से Latest Changes को Local Repository में लाना।

सरल भाषा में,

> Pull = GitHub से अपने Computer पर Latest Code लाना।

---

# आसान उदाहरण

मान लो Team में 5 Developers काम कर रहे हैं।

Developer A ने

```
Login Feature
```

Push कर दिया।

Developer B ने

```
Dashboard Feature
```

Push कर दिया।

अब तुम्हारे Laptop में पुराना Code है।

Latest Code लाने के लिए

```bash
git pull
```

चलाना होगा।

---

# Pull Workflow

```
GitHub Repository

↓

git pull

↓

Local Repository

↓

Working Directory
```

---

# Pull के अंदर क्या होता है?

बहुत Important Concept

जब हम

```bash
git pull
```

चलाते हैं,

तो Git वास्तव में दो Commands चलाता है।

```
git fetch
```

+

```
git merge
```

यानी

पहले Latest Changes Download होते हैं।

फिर Local Branch में Merge होते हैं।

---

# Basic Pull

```bash
git pull
```

यदि Upstream पहले से Set है,

तो यही Command पर्याप्त है।

---

# Specific Branch Pull

```bash
git pull origin main
```

इसका अर्थ है

```
origin/main
```

से Latest Changes लाकर

Current Branch में Merge करना।

---

# Verification

```bash
git status
```

Output

```
Your branch is up to date with origin/main.
```

---

# Real Industry Example

Morning

↓

Laptop Start

↓

Open Project

↓

```bash
git pull
```

↓

Latest Team Code

↓

Development Start

---

# Pull कब करना चाहिए?

✔ Development शुरू करने से पहले।

✔ Push करने से पहले।

✔ Pull Request Review से पहले।

✔ लंबे समय बाद Project खोलने पर।

---

# Common Mistakes

❌ बिना Pull किए Push करना।

❌ Local Changes Save किए बिना Pull करना।

❌ Wrong Branch पर Pull करना।

❌ Merge Conflict को Ignore करना।

---

# Best Practices

✔ Pull से पहले

```bash
git status
```

देखें।

✔ अपनी Current Branch Verify करें।

```bash
git branch
```

✔ छोटे-छोटे Interval में Pull करें।

✔ बड़े Feature शुरू करने से पहले Latest Code लें।

---

# 🏭 Production Note

Enterprise Projects में Developers

हर सुबह

```bash
git pull
```

चलाते हैं।

इससे सभी Team Members Latest Code पर काम करते हैं।

---

# Interview Questions

Q1. Git Pull क्या है?

Q2. Git Pull के अंदर कौन-सी दो Commands चलती हैं?

Q3. Pull और Fetch में क्या अंतर है?

Q4. Pull कब करना चाहिए?

Q5. Pull के दौरान Merge Conflict क्यों आ सकता है?

---

# 🧠 Quick Revision

```
GitHub

↓

git pull

↓

Latest Code

↓

Local Repository
```

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Pull

✔ Pull Workflow

✔ Pull = Fetch + Merge

✔ Production Workflow

✔ Best Practices

अगले Chapter में हम Fetch सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Push

➡ Next: Fetch

---


# 🔥 Important Note Pull हमेशा Safe नहीं होता

बहुत से Beginners सोचते हैं कि

```
git pull
```

हमेशा Safe है।

ऐसा नहीं है।

अगर Local Repository में Uncommitted Changes हैं,

तो Pull के दौरान Merge Conflict आ सकता है।

इसलिए Pull करने से पहले हमेशा

```bash

git status
```

चलाकर Working Tree Verify करें।

# 🔥 Real Production Scenario Daily Development Workflow

Production Environment में Developers अक्सर यह Workflow Follow करते हैं।

```
Office Start

↓

git pull

↓

Latest Code

↓

Development

↓

git add .

↓

git commit

↓

git push

↓

Pull Request
```

यह सबसे सामान्य Industry Workflow है।

---

# 🚀 Topic Complete होने के बाद

- git add .

- git commit -m "docs(git): add pull documentation"

- git push


# 💡 Senior Engineer Tip

आज एक बहुत महत्वपूर्ण Concept याद रखो:

git push

➡️ Local → GitHub

git pull

➡️ GitHub → Local

यानी:

git push  = Upload

git pull  = Download + Merge

----