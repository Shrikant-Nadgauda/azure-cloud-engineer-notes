यहीं से असली Git शुरू होता है।

Production में सबसे ज़्यादा डर कब लगता है?

"गलत Commit हो गया 😨"

यहीं पर git revert काम आता है।

⚠️ याद रखना:

Revert = Safe Undo

यानी History को बिना तोड़े गलती को वापस लेना।

# 📘 Topic 18 - Revert

# Revert

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Revert क्या होता है?
- Revert की आवश्यकता क्यों होती है?
- Revert कैसे काम करता है?
- Revert और Reset में अंतर
- Production में Revert कब उपयोग करते हैं?
- Real Industry Example

---

# Revert क्या होता है?

Revert का अर्थ है

> किसी पुराने Commit के Effect को Cancel करना, लेकिन Git History को सुरक्षित रखना।

यानी

गलत Commit Delete नहीं होता,

बल्कि Git एक नया Commit बनाता है जो उस गलती को Undo कर देता है।

---

# आसान उदाहरण

मान लो

तुमने एक Commit किया

```
Add Login Feature
```

बाद में पता चला कि Login Feature में Bug है।

ऐसे में

```bash
git revert <commit-id>
```

चलाने पर

Git एक नया Commit बनाएगा

```
Revert "Add Login Feature"
```

अब Bug हट जाएगा,

लेकिन History सुरक्षित रहेगी।

---

# Revert Workflow

```
Commit A

↓

Commit B

↓

Commit C (Bug)

↓

git revert C

↓

Commit D (Revert Commit)
```

ध्यान दें

Commit C अभी भी History में रहेगा।

Commit D उसका Effect Cancel करेगा।

---

# Revert Command

सबसे पहले Commit History देखें

```bash
git log --oneline
```

फिर

```bash
git revert <commit-id>
```

उदाहरण

```bash
git revert a4d9f21
```

---

# Revert के बाद

History

```
A

↓

B

↓

C

↓

D (Revert)
```

कोई Commit Delete नहीं हुआ।

---

# Real Industry Example

Developer ने

Production में

गलत Firewall Rule Deploy कर दिया।

Application Down हो गई।

ऐसे समय

Reset नहीं करेंगे।

बल्कि

```
git revert
```

करेंगे,

ताकि History सुरक्षित रहे।

---

# Revert कब उपयोग करें?

✔ Production Branch

✔ Shared Repository

✔ Main Branch

✔ Release Branch

✔ Team Projects

---

# Common Mistakes

❌ Revert और Reset को एक जैसा समझना।

❌ Wrong Commit Revert करना।

❌ Revert के बाद Push करना भूल जाना।

---

# Best Practices

✔ पहले Commit ID Verify करें।

```bash
git log --oneline
```

✔ Main Branch में Revert Prefer करें।

✔ Revert Commit का Message न बदलें।

✔ Team को Inform करें।

---

# Revert vs Reset

| Revert | Reset |
|---------|--------|
| Safe | Risky |
| History रहती है | History बदल सकती है |
| नया Commit बनता है | Commit हट सकते हैं |
| Production में उपयोग | Local Development में उपयोग |

---

# 🏭 Production Note

Enterprise Projects में

अगर कोई गलत Commit Main Branch में Merge हो जाए,

तो लगभग हमेशा

```
git revert
```

का उपयोग किया जाता है।

क्योंकि इससे History सुरक्षित रहती है।

---

# Interview Questions

Q1. Git Revert क्या है?

Q2. Revert नया Commit क्यों बनाता है?

Q3. Revert और Reset में क्या अंतर है?

Q4. Production में Revert क्यों उपयोग किया जाता है?

Q5. Revert करने से History बदलती है?

---

# 🧠 Quick Revision

```
Wrong Commit

↓

git revert

↓

New Undo Commit

↓

History Safe
```

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Revert

✔ Undo Changes

✔ Safe Recovery

✔ Revert vs Reset

✔ Production Workflow

अगले Chapter में हम Reset सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Releases

➡ Next: Reset

----

# 🔥 Important Note / Revert Commit Delete नहीं करता

Revert कभी भी पुराने Commit को Delete नहीं करता।

यह केवल एक नया Commit बनाता है जो पुराने Commit के Effect को Cancel कर देता है।

इसी कारण Revert को Safe Operation माना जाता है।

----

# 🔥 Real Production Scenario / Production Bug Recovery

मान लो

Developer ने Main Branch में गलत Code Merge कर दिया।

```
Commit A

↓

Commit B

↓

Commit C (Bug)
```

अब पूरी Application Error देने लगी।

ऐसे समय

```
git revert C
```

चलाया जाता है।

नई History

```
Commit A

↓

Commit B

↓

Commit C

↓

Commit D (Revert)
```

अब Bug हट गया,

लेकिन सभी Commits सुरक्षित रहे।

यही Enterprise Projects में सबसे सामान्य Recovery Method है।

----

# 💻 Practical

- Commit History देखें

git log --oneline

- मान लो Output

f45d321 Add Login

b214a11 Update README

9c341ab Initial Commit

- अब पहला Commit Undo करना है

git revert f45d321

History देखें

git log --oneline

- अब नया Commit दिखाई देगा

8d12c56 Revert "Add Login"

f45d321 Add Login

b214a11 Update README

9c341ab Initial Commit

GitHub पर भेजें

git push

-----

# 🚀 Topic Complete होने के बाद

git add .

git commit -m "docs(git): add revert documentation"

git push

----

# 💡 Senior Engineer Tip

- यह Rule हमेशा याद रखना:

Development में गलती?

→ Reset

Production में गलती?

→ Revert

- और यह Diagram कभी मत भूलना:

Original History

A ── B ── C (Bug)

↓

git revert C

↓

New History

A ── B ── C ── D (Undo)

C अभी भी History में है।

D केवल C के Effect को Cancel करता है।

----