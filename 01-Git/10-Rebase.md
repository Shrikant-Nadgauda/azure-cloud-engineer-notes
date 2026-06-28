# Rebase

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Rebase क्या है?
- Merge और Rebase में क्या अंतर है?
- Rebase की आवश्यकता क्यों होती है?
- Rebase कैसे करते हैं?
- Interactive Rebase क्या है?
- Real Industry Example

---

# Rebase क्या है?

Rebase का अर्थ है

> एक Branch के Commits को दूसरी Branch के Latest Commit के ऊपर दोबारा लगाना।

सरल भाषा में,

> Rebase = अपनी Branch को Latest History पर Shift करना।

इससे Git History साफ (Linear) दिखाई देती है।

---

# आसान उदाहरण

मान लो Main Branch पर नए Changes आ चुके हैं।

```
main

A ---- B ---- C
```

तुमने पहले ही Branch बना ली थी।

```
feature-login

A ---- B ---- D
```

अब Main आगे बढ़ गया है।

तुम चाहते हो कि तुम्हारी Branch भी Latest Main पर आ जाए।

तब Rebase किया जाता है।

---

# Rebase के बाद

```
main

A ---- B ---- C

               \

feature-login

                D'
```

ध्यान दो

D वही Commit है,

लेकिन Git उसे नए Base पर दोबारा बनाता है।

इसलिए उसे D' (New Commit) कहा जाता है।

---

# Rebase क्यों करते हैं?

यदि Team Main Branch पर लगातार काम कर रही है,

तो तुम्हारी Branch पुरानी हो जाती है।

Rebase करके

✔ Latest Code मिल जाता है।

✔ Merge Conflicts जल्दी पकड़ में आते हैं।

✔ History साफ रहती है।

---

# Merge vs Rebase

## Merge

```
A ---- B ---- C

      \

       D

        \

      Merge Commit
```

✔ Original History सुरक्षित रहती है।

✔ Merge Commit बनता है।

---

## Rebase

```
A ---- B ---- C ---- D'
```

✔ कोई Merge Commit नहीं।

✔ History बिल्कुल सीधी (Linear) रहती है।

---

# Rebase कैसे करें?

Feature Branch पर जाओ।

```bash
git switch feature-login
```

Latest Main लो।

```bash
git rebase main
```

Git तुम्हारे Commits को Main के ऊपर लगा देगा।

---

# Verification

History देखें।

```bash
git log --oneline --graph
```

Rebase के बाद Graph सीधा दिखाई देगा।

---

# Interactive Rebase

अगर कई Commits को Edit करना हो,

तो Interactive Rebase उपयोग करते हैं।

```bash
git rebase -i HEAD~3
```

इससे

✔ Commit Rename

✔ Commit Delete

✔ Commit Combine (Squash)

✔ Commit Reorder

किए जा सकते हैं।

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

Developer तीन दिन तक काम करता रहा।

इस दौरान Main Branch में

NSG

Bastion

Firewall

के Changes आ गए।

अब Developer

```bash
git rebase main
```

करता है।

अब उसकी Branch Latest Production Code पर आ जाती है।

---

# Common Mistakes

❌ Shared Branch पर Rebase करना।

❌ Rebase के बाद Force Push करना भूल जाना।

❌ Rebase के दौरान Conflicts Ignore करना।

---

# Best Practices

✔ Rebase केवल अपनी Feature Branch पर करें।

✔ Main Branch पर Rebase न करें।

✔ Rebase से पहले

```bash
git status
```

साफ होना चाहिए।

✔ Rebase के बाद History Verify करें।

---

# 🏭 Production Note

Enterprise Projects में Developers अक्सर

```bash
git fetch
git rebase origin/main
```

चलाते हैं,

ताकि उनकी Branch हमेशा Latest रहे।

GitHub और Azure DevOps में Pull Request भेजने से पहले Rebase करना एक अच्छी Practice मानी जाती है।

---

# Merge vs Rebase (Quick Comparison)

| Merge | Rebase |
|--------|---------|
| Merge Commit बनता है | Merge Commit नहीं बनता |
| History Branches सहित रहती है | History Linear रहती है |
| Beginners के लिए आसान | थोड़ा Advanced |
| Shared Branch के लिए सुरक्षित | Feature Branch के लिए बेहतर |

---

# Interview Questions

Q1. Rebase क्या है?

Q2. Merge और Rebase में क्या अंतर है?

Q3. Interactive Rebase क्या है?

Q4. Rebase के बाद Force Push क्यों करना पड़ सकता है?

Q5. Production में Rebase कब किया जाता है?

---

# 🧠 Quick Revision

```
Feature Branch

↓

Main Updated

↓

git rebase main

↓

Latest Code

↓

Clean History
```

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Rebase

✔ Merge vs Rebase

✔ Interactive Rebase

✔ Linear History

✔ Production Workflow

अगले Chapter में हम Remote Repository सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Merge

➡ Next: Remote

---

# 10.1 क्या Rebase Dangerous है?

हाँ, अगर गलत जगह किया जाए।

Rebase Commit History को Rewrite करता है।

इसलिए Production में कभी भी Shared Branch (जैसे main) पर Rebase नहीं किया जाता।

Rebase केवल अपनी Feature Branch पर करें।

अगर Rebase के दौरान कोई गलती हो जाए, तो Git उसे भी Recover करने के तरीके देता है।

आगे आने वाले Chapters में हम सीखेंगे:

- Rebase Abort
- Rebase Continue
- Reflog
- Reset
- Force Push

इसलिए अभी केवल Concept समझें। Recovery Techniques बाद में विस्तार से सीखेंगे।

---

# 💻 Practical (अभी मत घबराना 😄)

अभी सिर्फ Commands समझो। अगले Labs में इन्हें Practical करेंगे।

- Feature Branch पर जाओ
git switch feature-login

- Main के Latest Changes लाओ
git fetch origin

- Main पर Rebase करो
git rebase origin/main

- History देखो
git log --oneline --graph --all

---

# 🚀 Topic Complete होने के बाद
- git add .

- git commit -m "docs(git): add rebase documentation"

- git push

---

# 💡 Senior Engineer Tip

** एक Rule हमेशा याद रखना: **

Merge जोड़ता है (Joins History).
Rebase लिखता है (Rewrites History).

यही एक लाइन Interview में बोल दोगे, तो सामने वाले को समझ आ जाएगा कि तुम्हें सिर्फ Commands नहीं, Git का Concept भी समझ में आता है। 🚀

---