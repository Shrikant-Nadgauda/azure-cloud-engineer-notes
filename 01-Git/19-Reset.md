अगर git revert Safe Undo है,

तो git reset Time Machine है।

लेकिन ⚠️ गलत इस्तेमाल किया तो अपना काम भी उड़ा सकते हो।

इसलिए इस Topic को धीरे-धीरे समझेंगे।

# 📘 Topic 19 - Reset
# Reset

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Reset क्या होता है?
- Reset की आवश्यकता क्यों होती है?
- Soft Reset
- Mixed Reset
- Hard Reset
- Revert और Reset में अंतर
- Production में Reset कब उपयोग करते हैं?
- Real Industry Example

---

# Reset क्या होता है?

Reset का अर्थ है

> Git Repository को किसी पुराने Commit पर वापस ले जाना।

Reset करने पर

Git Branch Pointer को पीछे ले जाता है।

यही कारण है कि Reset History को बदल सकता है।

---

# आसान उदाहरण

मान लो History

```
A

↓

B

↓

C

↓

D
```

अब

```
git reset B
```

कर दिया।

तो Branch वापस

```
B
```

पर आ जाएगी।

आगे के Commits

```
C

D
```

Branch History से हट जाएंगे।

---

# Reset Workflow

```
Commit A

↓

Commit B

↓

Commit C

↓

Commit D

↓

git reset B

↓

Current Branch

↓

Commit B
```

---

# Reset के प्रकार

Git में Reset के तीन मुख्य प्रकार हैं।

1.

Soft Reset

2.

Mixed Reset

3.

Hard Reset

---

# 1. Soft Reset

Command

```bash
git reset --soft HEAD~1
```

यह

✔ Commit हटा देता है।

✔ लेकिन Staging Area सुरक्षित रहती है।

✔ Files भी सुरक्षित रहती हैं।

---

स्थिति

```
Commit हट गया

↓

Files Stage में हैं

↓

Changes सुरक्षित
```

---

# कब उपयोग करें?

अगर Commit Message गलत हो।

अगर Commit दोबारा बनाना हो।

---

# 2. Mixed Reset

(Default)

```bash
git reset HEAD~1
```

या

```bash
git reset --mixed HEAD~1
```

यह

✔ Commit हटाता है।

✔ Staging हटाता है।

✔ Files सुरक्षित रहती हैं।

यही Git का Default Reset है।

---

स्थिति

```
Commit हट गया

↓

Stage खाली

↓

Files Working Directory में
```

---

# कब उपयोग करें?

अगर Files दोबारा Stage करनी हों।

---

# 3. Hard Reset

सबसे Dangerous

```bash
git reset --hard HEAD~1
```

यह

✔ Commit हटाता है।

✔ Stage हटाता है।

✔ Files भी हटा देता है।

---

स्थिति

```
Commit हट गया

↓

Stage हट गया

↓

Files भी हट गईं
```

---

# Hard Reset कब उपयोग करें?

✔ Local Practice

✔ Temporary Changes हटाने के लिए

✔ कभी भी Production Main Branch पर नहीं।

---

# HEAD क्या है?

HEAD हमेशा Current Commit की ओर Point करता है।

```
A

↓

B

↓

C ← HEAD
```

अगर

```bash
git reset HEAD~1
```

चलाया,

तो

HEAD

```
B
```

पर आ जाएगा।

---

# HEAD~1

Current Commit से

1 Commit पीछे

HEAD~2

2 Commit पीछे

HEAD~3

3 Commit पीछे

---

# Revert vs Reset

| Revert | Reset |
|---------|--------|
| नया Commit बनाता है | Branch पीछे ले जाता है |
| History सुरक्षित रहती है | History बदल सकती है |
| Production के लिए Best | Local Development के लिए Best |
| Safe | Risky |

---

# Real Industry Example

Developer ने

5 Commits किए।

अभी Push नहीं किया।

पता चला पूरा Code गलत है।

ऐसे समय

```bash
git reset --hard HEAD~5
```

से Local History साफ की जा सकती है।

लेकिन अगर वही Commits पहले से GitHub पर Push हो चुके हों,

तो Reset की जगह

Revert उपयोग करना चाहिए।

---

# Common Mistakes

❌ Hard Reset के बाद Files खो देना।

❌ Push किए हुए Commits पर Reset करना।

❌ Reset और Revert को Confuse करना।

❌ Main Branch पर Hard Reset करना।

---

# Best Practices

✔ पहले

```bash
git status
```

देखें।

✔ पहले

```bash
git log --oneline
```

देखें।

✔ Production में Revert Prefer करें।

✔ Hard Reset से पहले Backup रखें।

---

# 🏭 Production Note

Enterprise Projects में

Developers

Local Branch पर Reset करते हैं।

लेकिन Shared Branch

Main

Master

Release

पर लगभग हमेशा

Revert उपयोग किया जाता है।

---

# Interview Questions

Q1. Git Reset क्या है?

Q2. Soft Reset क्या करता है?

Q3. Mixed Reset क्या करता है?

Q4. Hard Reset क्यों Dangerous है?

Q5. Revert और Reset में क्या अंतर है?

---

# 🧠 Quick Revision

```
Soft

↓

Commit हटे

↓

Files Safe

Mixed

↓

Commit हटे

↓

Stage हटे

↓

Files Safe

Hard

↓

Commit हटे

↓

Stage हटे

↓

Files हटें
```

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Reset

✔ Soft Reset

✔ Mixed Reset

✔ Hard Reset

✔ HEAD

✔ Revert vs Reset

अगले Chapter में हम Cherry-pick सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Revert

➡ Next: Cherry-pick

----
 
# 🔥  Important Note- Hard Reset से पहले सोचें

Hard Reset केवल Commit नहीं हटाता,

बल्कि Working Directory की Files भी हटा सकता है।

अगर Changes कहीं Save नहीं हैं,

तो वे हमेशा के लिए खो सकते हैं।

इसलिए Hard Reset से पहले

- git status

- git log --oneline

- Backup

जरूर देखें।

----

# 🔥  Real Production Scenario Production में Reset कब नहीं करना चाहिए?

मान लो

Developer ने

Main Branch पर

5 Commits Push कर दिए।

बाद में पता चला कि उनमें Bug है।

ऐसे समय

```
git reset --hard
```

नहीं करेंगे।

क्योंकि इससे Shared History बदल जाएगी।

सही तरीका

```
git revert
```

है।

Reset केवल Local Branch पर करें,

Shared Branch पर नहीं।

----

# 💻 Practical

History देखें

git log --oneline

Soft Reset

git reset --soft HEAD~1

Mixed Reset

git reset HEAD~1

Hard Reset

git reset --hard HEAD~1

Status देखें

git status

History Verify करें

git log --oneline

---

# 🚀 Topic Complete होने के बाद

git add .

git commit -m "docs(git): add reset documentation"

git push

----

# 💡 Senior Engineer Tip (Golden Memory Trick)

- इसे हमेशा याद रखना:

git reset --soft

👉 Commit हटाओ, Changes बचाओ

git reset --mixed

👉 Commit + Stage हटाओ, Files बचाओ

git reset --hard

👉 सब हटाओ (Commit + Stage + Files)

----

# 🧠 10 सेकंड का Interview Answer

अगर Interviewer पूछे:

"Soft, Mixed और Hard Reset में क्या अंतर है?"

तो सीधे यह बोलना:

Soft  → Commit हटाता है, Files और Stage सुरक्षित रहती हैं.

Mixed → Commit और Stage हटाता है, Files सुरक्षित रहती हैं.

Hard  → Commit, Stage और Files तीनों हटा देता है.

---