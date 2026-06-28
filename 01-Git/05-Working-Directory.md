# Working Directory

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Working Directory क्या होती है?
- Git के Workflow में इसका स्थान कहाँ है?
- Working Directory और Staging Area में क्या अंतर है?
- File Modify होने पर Git क्या करता है?
- Real Industry Example

---

# Working Directory क्या है?

Working Directory वह Folder होता है जहाँ हम वास्तविक रूप से काम करते हैं।

यानी,

यहीं हम

✔ नई Files बनाते हैं

✔ Existing Files Edit करते हैं

✔ Files Delete करते हैं

✔ Project Develop करते हैं

सरल भाषा में,

> Working Directory = वह जगह जहाँ Developer रोज़ काम करता है।

---

# आसान उदाहरण

मान लो तुम्हारा Project यहाँ रखा है:

```

D:\Cloud-Engineering

```

यही तुम्हारी Working Directory है।

इसके अंदर मौजूद सभी Files पर तुम काम करते हो।

---

# Git Workflow

Git किसी भी File को सीधे Commit नहीं करता।

पहले File Working Directory में रहती है।

फिर Staging Area में जाती है।

फिर Commit बनता है।

Workflow

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

यही Git का सबसे महत्वपूर्ण Flow है।

---

# Working Directory में क्या-क्या हो सकता है?

Working Directory में File की तीन मुख्य स्थितियाँ होती हैं।

### 1. New File

Git ने File पहले कभी नहीं देखी।

Example

```

notes.md

```

Status

```

Untracked

```

---

### 2. Modified File

पहले से Git में थी।

अब Edit कर दी गई।

Status

```

Modified

```

---

### 3. Deleted File

File पहले थी।

अब Delete कर दी।

Status

```

Deleted

```

---

# Git Working Directory को कैसे पहचानता है?

Git लगातार Files को Monitor करता रहता है।

जब भी कोई बदलाव होता है,

Git उसे Track कर लेता है।

लेकिन...

जब तक हम

```

git add

```

नहीं चलाते,

तब तक बदलाव केवल Working Directory में रहते हैं।

---

# Practical

Current Status देखें

```bash
git status
```

नई File बनाइए

```bash
touch demo.txt
```

अब Status देखें

```bash
git status
```

Output

```

Untracked files:
demo.txt

```

अब File Edit करें

```bash
echo "Hello Git" > demo.txt
```

फिर देखें

```bash
git status
```

Git बताएगा कि File बदल चुकी है।

---

# Verification

Status देखने के लिए

```bash
git status
```

यदि Output में

```

modified

```

या

```

untracked

```

दिखाई देता है,

तो इसका मतलब बदलाव अभी Working Directory में हैं।

---

# Working Directory बनाम Staging Area

| Working Directory | Staging Area |
|-------------------|--------------|
| जहाँ काम करते हैं | जहाँ Commit की तैयारी होती है |
| File Edit होती है | File Commit के लिए Select होती है |
| Changes अभी Local हैं | Changes Commit होने वाले हैं |

---

# Real Industry Example

मान लो तुम Azure Infrastructure पर काम कर रहे हो।

तुमने

```

main.tf

```

में Virtual Network Add किया।

अभी यह केवल Working Directory में है।

Company के बाकी Engineers को यह बदलाव अभी दिखाई नहीं देगा।

जब तक

```

git add

git commit

git push

```

नहीं करोगे।

---

# Common Mistakes

❌ File Modify करके Commit करना भूल जाना।

❌ बिना Status देखे Commit करना।

❌ Working Directory में Temporary Files छोड़ देना।

❌ Sensitive Files Create करना।

---

# Best Practices

✔ हमेशा काम शुरू करने से पहले

```bash
git status
```

चलाओ।

✔ एक Feature पर काम करो।

✔ छोटे-छोटे Changes Commit करो।

✔ Unnecessary Files Remove करते रहो।

---

# 🏭 Production Note

Production Teams में Developers लगभग हर 10-15 मिनट में

```
git status
```

देखते हैं।

इससे उन्हें पता रहता है कि कौन-सी Files बदली हैं।

---

# Interview Questions

Q1. Working Directory क्या होती है?

Q2. Working Directory और Repository में क्या अंतर है?

Q3. Git किसी File को पहली बार कैसे पहचानता है?

Q4. Untracked File क्या होती है?

Q5. Modified File क्या होती है?

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

✔ Working Directory

✔ File States

✔ Git Workflow

✔ Untracked File

✔ Modified File

✔ Working Directory vs Staging Area

✔ Industry Example

अगले Chapter में हम Staging Area सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Git Repository

➡ Next: Staging Area