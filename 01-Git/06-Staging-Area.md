# Staging Area

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Staging Area क्या होती है?
- Git में इसकी आवश्यकता क्यों है?
- git add वास्तव में क्या करता है?
- Working Directory और Staging Area में क्या अंतर है?
- Real Industry Example

---

# Staging Area क्या है?

Staging Area Git का एक Temporary Area होता है।

यहीं हम तय करते हैं कि

Project की कौन-कौन सी Files अगले Commit में शामिल होंगी।

सरल भाषा में,

> Staging Area = Commit की तैयारी करने वाली जगह।

---

# आसान उदाहरण

मान लो तुमने 10 Files Edit की हैं।

लेकिन अभी केवल 2 Files ही Commit करनी हैं।

Git तुम्हें यह सुविधा देता है।

यही काम Staging Area करती है।

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

ध्यान दो,

Working Directory और Commit के बीच में हमेशा Staging Area आती है।

---

# git add वास्तव में क्या करता है?

बहुत लोग सोचते हैं

```
git add
```

मतलब File Save हो गई।

❌ ऐसा नहीं है।

असल में

```
git add
```

Git को बताता है

> "अगले Commit में यह File शामिल करना।"

बस।

Commit अभी नहीं हुआ है।

---

# Practical Example

मान लो Project में ये Files हैं

```
main.tf
variables.tf
README.md
```

तुमने तीनों बदल दीं।

लेकिन अभी केवल

```
README.md
```

Commit करनी है।

तो

```bash
git add README.md
```

अब केवल यही File Stage होगी।

बाकी दो Files Working Directory में ही रहेंगी।

---

# Practical

Current Status

```bash
git status
```

नई File बनाओ

```bash
touch demo.txt
```

Status

```bash
git status
```

अब Stage करो

```bash
git add demo.txt
```

फिर Status

```bash
git status
```

Output

```
Changes to be committed
```

यानी File अब Staging Area में आ चुकी है।

---

# Multiple Files Stage करना

सभी Files

```bash
git add .
```

सिर्फ एक File

```bash
git add README.md
```

दो Files

```bash
git add main.tf variables.tf
```

---

# Verification

Status Check

```bash
git status
```

अगर दिखाई दे

```
Changes to be committed
```

तो File Successfully Stage हो चुकी है।

---

# Working Directory vs Staging Area

| Working Directory | Staging Area |
|-------------------|--------------|
| यहाँ File Edit होती है | यहाँ Commit के लिए Select होती है |
| Changes अभी Local हैं | Changes Commit होने वाले हैं |
| git add से पहले | git add के बाद |

---

# Real Industry Example

मान लो Azure Infrastructure Project में तुमने

```
main.tf
```

और

```
README.md
```

दोनों बदल दिए।

लेकिन

README अभी Complete नहीं है।

केवल

```
main.tf
```

Deploy करनी है।

तुम करोगे

```bash
git add main.tf
```

अब केवल Infrastructure वाला Code Commit होगा।

README अगले Commit में जाएगी।

यही Professional Workflow है।

---

# Common Mistakes

❌ हमेशा `git add .` चला देना।

❌ बिना `git status` देखे Commit करना।

❌ गलती से Secret Files Stage कर देना।

❌ Temporary Files Stage करना।

---

# Best Practices

✔ Commit करने से पहले हमेशा

```bash
git status
```

देखो।

✔ जितनी जरूरत हो उतनी ही Files Stage करो।

✔ छोटे और Logical Commits बनाओ।

✔ Stage करने के बाद दोबारा Status Verify करो।

---

# 🏭 Production Note

Production Teams में Developers अक्सर

```bash
git add README.md
```

या

```bash
git add main.tf
```

जैसी Specific Files Stage करते हैं।

Blindly

```bash
git add .
```

हर बार Use नहीं किया जाता।

---

# Interview Questions

Q1. Staging Area क्या है?

Q2. git add क्या करता है?

Q3. Working Directory और Staging Area में क्या अंतर है?

Q4. क्या git add Commit करता है?

Q5. केवल एक File Stage कैसे करेंगे?

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

✔ Staging Area

✔ git add

✔ File Selection

✔ Git Workflow

✔ Verification

✔ Production Workflow

✔ Industry Example

अगले Chapter में हम Commit सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Working Directory

➡ Next: Commit

💻 Practical (अभी करके देखो)

अपने Repository में ये Commands चलाओ:

touch staging-demo.txt
git status
git add staging-demo.txt
git status

git status के Output को ध्यान से पढ़ना। पहले Untracked files दिखेगा, फिर Changes to be committed। यहीं पहली बार तुम्हें Staging Area का असली फर्क दिखाई देगा।

