# Merge

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Merge क्या होता है?
- Merge की आवश्यकता क्यों होती है?
- Branches को Merge कैसे करते हैं?
- Fast Forward Merge क्या है?
- Three-Way Merge क्या है?
- Real Industry Example

---

# Merge क्या है?

Merge का अर्थ है

दो अलग-अलग Branches के Changes को एक Branch में जोड़ना।

सरल भाषा में,

> Merge = दो Branches का Code एक साथ मिलाना।

---

# आसान उदाहरण

मान लो Project में दो Developers काम कर रहे हैं।

Developer A

```
feature-login
```

Developer B

```
feature-payment
```

दोनों ने अपना काम पूरा कर लिया।

अब दोनों Features को Main Project में जोड़ना है।

यही Merge कहलाता है।

---

# Git Merge Workflow

```
            feature-login
                  │
                  │
main ─────────────┼────────────

                  │

          git merge

                  │

main ─────────────────────────
```

---

# Merge की आवश्यकता क्यों होती है?

अगर Merge नहीं होगा,

तो हर Branch अलग-अलग रहेगी।

Project कभी Complete नहीं होगा।

Merge सभी Features को एक Project में जोड़ देता है।

---

# Merge कैसे करते हैं?

सबसे पहले Main Branch पर जाएँ

```bash
git switch main
```

अब Feature Branch Merge करें

```bash
git merge feature-login
```

Git दोनों Branches के Changes को जोड़ देगा।

---

# Practical Example

Current Branch

```
main
```

नई Branch

```
feature-login
```

Feature Complete

अब वापस

```bash
git switch main
```

Merge

```bash
git merge feature-login
```

अब Login Feature Main Branch में आ गया।

---

# Verification

History देखें

```bash
git log --oneline --graph
```

या

```bash
git branch
```

---

# Fast Forward Merge

यदि Main Branch में कोई नया Commit नहीं हुआ,

तो Git सीधे Branch को आगे बढ़ा देता है।

```
main

A

↓

feature

A ---- B ---- C

↓

Merge

↓

main

A ---- B ---- C
```

कोई Merge Commit नहीं बनता।

---

# Three-Way Merge

यदि दोनों Branches में अलग-अलग Commits हुए हैं,

तो Git Merge Commit बनाता है।

```
           feature

             B

            /

A ----------

            \

             C

           main

↓

Merge

↓

A ----- B

 \     /

  Merge

    |

    C
```

---

# Real Industry Example

Azure Infrastructure Project

Main Branch

```
Production
```

Developer 1

```
feature-vnet
```

Developer 2

```
feature-bastion
```

Developer 3

```
feature-firewall
```

सभी Engineers अपना Feature Complete करते हैं।

Code Review होती है।

Testing होती है।

फिर Main Branch में Merge किया जाता है।

---

# Common Mistakes

❌ बिना Pull किए Merge करना।

❌ Main Branch पर Direct Development करना।

❌ Merge करने से पहले Testing न करना।

❌ Merge Conflict Ignore करना।

---

# Best Practices

✔ Merge से पहले

```bash
git pull
```

करो।

✔ Code Review के बाद ही Merge करो।

✔ Feature Branch Delete करने से पहले Verify करो।

✔ छोटे Features जल्दी Merge करो।

---

# 🏭 Production Note

Enterprise Projects में Developers सीधे

```bash
git merge
```

कम ही करते हैं।

अधिकतर Merge

✔ Pull Request

✔ Merge Request

✔ Azure DevOps PR

✔ GitHub PR

के माध्यम से किया जाता है।

Code Review के बाद ही Merge होता है।

---

# Interview Questions

Q1. Merge क्या है?

Q2. Fast Forward Merge क्या है?

Q3. Three-Way Merge क्या है?

Q4. Merge Commit क्या होता है?

Q5. Production में Merge कैसे किया जाता है?

---

# 🧠 Quick Revision

```
Create Branch

↓

Development

↓

Commit

↓

Switch Main

↓

Merge

↓

Main Updated
```

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Merge

✔ Fast Forward Merge

✔ Three-Way Merge

✔ git merge

✔ Production Workflow

✔ Industry Example

अगले Chapter में हम Rebase सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Branches

➡ Next: Rebase

---

# 💻 Practical (अभी करके देखो)

Step 1: नई Branch बनाओ

git switch -c feature/demo

Step 2: कोई File Edit करो और Commit करो

echo "Merge Demo" >> demo.txt

git add .

git commit -m "feat: add merge demo"

Step 3: Main Branch पर वापस जाओ

git switch main

Step 4: Branch Merge करो

git merge feature/demo

Step 5: History Graph देखो

git log --oneline --graph --all

यहीं पहली बार तुम्हें Git का Branch Graph दिखाई देगा। आगे Rebase पढ़ते समय यही Graph बहुत काम आएगा।

---

# 🚀 Topic Complete होने के बाद

- git add .

- git commit -m "docs(git): add merge documentation"

- git push

---
# 💡 Engineer Tip

Production में Merge सीधे main पर नहीं किया जाता।

Real Workflow कुछ ऐसा होता है:

main
   │
   ├── feature/vnet
   ├── feature/nsg
   ├── feature/bastion
        │
        ▼
   Pull Request (Code Review)
        │
        ▼
      Merge
        │
        ▼
      main

यही Workflow GitHub, Azure DevOps, GitLab और लगभग हर Enterprise Organization में Follow किया जाता है।

---

# 9.1 क्या Merge करने से Main Branch खराब हो सकती है?

हाँ।

अगर गलत Branch Merge कर दी जाए या गलत Code Merge हो जाए, तो Main Branch प्रभावित हो सकती है।

लेकिन Git हमें ऐसी स्थिति से बाहर आने के लिए कई विकल्प देता है।

आगे आने वाले Chapters में हम सीखेंगे:

- Revert
- Reset
- Reflog
- Cherry-Pick

इनकी मदद से हम गलत Merge, गलत Commit या गलती से हुए Changes को सुरक्षित तरीके से Recover कर सकते हैं।

**इसलिए अभी केवल Merge की प्रक्रिया समझें। Recovery Techniques हम आगे सीखेंगे।**