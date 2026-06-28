# Fetch

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Fetch क्या होता है?
- Fetch की आवश्यकता क्यों होती है?
- Fetch कैसे काम करता है?
- Fetch और Pull में अंतर
- Production में Fetch कब उपयोग करते हैं?
- Real Industry Example

---

# Fetch क्या होता है?

Fetch का अर्थ है

> Remote Repository (GitHub/Azure DevOps) से Latest Changes Download करना, लेकिन उन्हें Local Branch में Merge **नहीं** करना।

सरल भाषा में,

> Fetch = Latest Updates देखो, लेकिन अभी Project को मत बदलो।

---

# आसान उदाहरण

मान लो Team में 10 Developers काम कर रहे हैं।

किसी ने नए Commits Push किए।

तुम जानना चाहते हो कि क्या-क्या बदला है,

लेकिन अभी अपना Code बदलना नहीं चाहते।

ऐसे समय पर

```bash
git fetch
```

चलाया जाता है।

---

# Fetch Workflow

```
GitHub Repository

↓

git fetch

↓

Local Git Database

↓

(Working Directory में कोई बदलाव नहीं)
```

---

# Fetch के बाद क्या होता है?

Fetch केवल

```
origin/main
```

को Update करता है।

तुम्हारी Current Branch वैसे की वैसे रहती है।

इसलिए Fetch पूरी तरह Safe Operation माना जाता है।

---

# Basic Fetch

```bash
git fetch
```

---

# Specific Remote

```bash
git fetch origin
```

---

# सभी Branches Fetch करना

```bash
git fetch --all
```

---

# Fetch के बाद Changes देखना

```bash
git log HEAD..origin/main --oneline
```

या

```bash
git diff main origin/main
```

अब तुम्हें पता चल जाएगा कि Remote पर क्या नया आया है।

---

# Fetch और Pull में अंतर

| Git Fetch | Git Pull |
|-----------|----------|
| केवल Download करता है | Download + Merge करता है |
| Working Directory नहीं बदलती | Working Directory बदल सकती है |
| Safe Operation | Merge Conflict आ सकता है |
| Review के लिए अच्छा | सीधे Latest Code लेने के लिए |

---

# Real Industry Example

Developer सुबह Office आया।

सबसे पहले

```bash
git fetch
```

चलाया।

देखा कि Team ने 15 Commits किए हैं।

पहले उन Commits को Review किया।

फिर

```bash
git pull
```

किया।

यही Production Workflow है।

---

# Fetch कब करना चाहिए?

✔ Team के Latest Changes देखने हों।

✔ Merge करने से पहले Review करना हो।

✔ Remote Branches Check करनी हों।

✔ CI/CD Pipeline Trigger होने से पहले Code Compare करना हो।

---

# Common Mistakes

❌ Fetch करने के बाद सोचना कि Local Code Update हो गया।

❌ Fetch और Pull को एक जैसा समझना।

❌ Fetch के बाद Review किए बिना Merge करना।

---

# Best Practices

✔ पहले Fetch करें।

✔ Changes Review करें।

✔ फिर Pull करें।

✔ बड़े Project में सीधे Pull करने से बचें।

---

# 🏭 Production Note

Enterprise Projects में Senior Engineers अक्सर

```bash
git fetch
```

पहले चलाते हैं।

उसके बाद

```bash
git diff
```

या

```bash
git log
```

से Changes Review करते हैं।

फिर ही

```bash
git pull
```

करते हैं।

---

# Interview Questions

Q1. Git Fetch क्या है?

Q2. Git Fetch और Git Pull में क्या अंतर है?

Q3. Fetch के बाद Working Directory बदलती है?

Q4. Fetch को Safe Operation क्यों कहते हैं?

Q5. Production में Fetch पहले क्यों करते हैं?

---

# 🧠 Quick Revision

```
GitHub

↓

git fetch

↓

Latest Commits Download

↓

No Merge

↓

No Changes in Working Directory
```

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Fetch

✔ Fetch Workflow

✔ Fetch vs Pull

✔ Safe Operation

✔ Production Workflow

अगले Chapter में हम Tags सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Pull

➡ Next: Tags

---

 
# 🔥Important Note Fetch के बाद Project क्यों नहीं बदलता?

Fetch केवल Remote Repository की जानकारी Local Git Database में Update करता है।

यह तुम्हारी Working Directory या Current Branch को नहीं बदलता।

इसी कारण Fetch को Safe Operation माना जाता है।

अगर Latest Code अपने Project में लाना है,

तो उसके बाद

git pull

या

git merge origin/main

करना होगा।

# 🔥 Real Production Scenario Enterprise Workflow

Morning

↓

git fetch

↓

Review Remote Changes

↓

git diff

↓

Code Review

↓

git pull

↓

Development Start

यह Workflow बड़े Enterprise Projects में सामान्य है क्योंकि इससे बिना सोचे-समझे Merge करने से बचा जा सकता है।
---

# 🚀 Topic Complete होने के बाद

- git add .

- git commit -m "docs(git): add fetch documentation"

- git push

# 💡 Senior Engineer Tip (Golden Rule)

यह Diagram हमेशा याद रखना:

                 GitHub
                    │
        ┌───────────┴───────────┐
        │                       │
    git fetch              git pull
        │                       │
Download Only         Download + Merge
        │                       │
No Project Change     Working Directory Update

और अब Git के तीन सबसे महत्वपूर्ण Commands एक साथ:

git push   → Local → GitHub

git fetch  → GitHub → Local Database (No Merge)

git pull   → GitHub → Local + Merge
------