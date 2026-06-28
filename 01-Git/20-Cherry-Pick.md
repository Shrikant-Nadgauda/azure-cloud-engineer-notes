Beginners अक्सर इसे Skip कर देते हैं।

git cherry-pick

अगर Merge मतलब पूरी Branch लाना है,

तो Cherry-pick मतलब सिर्फ एक Commit उठाकर दूसरी Branch में लाना।

यही इसका सबसे बड़ा Use Case है।

📘 Topic 20 - Cherry-pick
# Cherry-pick

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Cherry-pick क्या है?
- Cherry-pick की आवश्यकता क्यों होती है?
- Cherry-pick कैसे काम करता है?
- Merge और Cherry-pick में अंतर
- Production में Cherry-pick कब उपयोग करते हैं?
- Real Industry Example

---

# Cherry-pick क्या है?

Cherry-pick का अर्थ है

> किसी Branch से केवल एक Specific Commit को उठाकर दूसरी Branch में Apply करना।

पूरी Branch Merge नहीं होती।

केवल चुना हुआ Commit आता है।

---

# आसान उदाहरण

मान लो

Main Branch

```
A

↓

B

↓

C
```

Feature Branch

```
A

↓

D

↓

E
```

अब

तुम्हें केवल

Commit D

Main Branch में चाहिए।

पूरी Feature Branch नहीं।

ऐसे समय

```
git cherry-pick <commit-id>
```

का उपयोग करेंगे।

---

# Cherry-pick Workflow

```
Main

A

↓

B

↓

C

Feature

A

↓

D

↓

E

↓

git cherry-pick D

↓

Main

A

↓

B

↓

C

↓

D
```

ध्यान दें

E Main में नहीं आया।

---

# Cherry-pick Command

सबसे पहले Commit ID देखें

```bash
git log --oneline
```

फिर

```bash
git cherry-pick <commit-id>
```

उदाहरण

```bash
git cherry-pick 7ad54bc
```

---

# कब उपयोग करें?

✔ Bug Fix

✔ Hotfix

✔ Production Patch

✔ किसी एक Feature को जल्दी Deploy करना

✔ केवल एक Commit दूसरी Branch में लाना

---

# Real Industry Example

Developer ने

Feature Branch में

10 Commits किए।

उनमें से

सिर्फ

1 Commit

Critical Bug Fix है।

Production Team पूरी Branch Merge नहीं करना चाहती।

ऐसे समय

```
git cherry-pick
```

का उपयोग किया जाता है।

---

# Merge vs Cherry-pick

| Merge | Cherry-pick |
|--------|-------------|
| पूरी Branch Merge करता है | केवल एक Commit लाता है |
| सभी Commits आते हैं | केवल चुना हुआ Commit आता है |
| Branch History जुड़ती है | केवल Commit Copy होता है |
| Feature Complete होने पर | Specific Fix के लिए |

---

# Cherry-pick Conflict

अगर दोनों Branch में

एक ही File

अलग-अलग तरीके से बदली गई हो,

तो Cherry-pick करते समय Conflict आ सकता है।

Conflict Resolve करने के बाद

```bash
git cherry-pick --continue
```

चलाते हैं।

अगर Cancel करना हो

```bash
git cherry-pick --abort
```

---

# Common Mistakes

❌ गलत Commit Cherry-pick करना।

❌ Commit ID Verify नहीं करना।

❌ Conflict Resolve किए बिना Continue करना।

---

# Best Practices

✔ पहले

```bash
git log --oneline
```

देखें।

✔ Commit Message पढ़ें।

✔ केवल Tested Commit Cherry-pick करें।

✔ Production में सोच-समझकर उपयोग करें।

---

# 🏭 Production Note

Enterprise Projects में

Release Branch

Main Branch

Hotfix Branch

के बीच

Specific Bug Fix लाने के लिए

Cherry-pick का बहुत उपयोग होता है।

---

# Interview Questions

Q1. Cherry-pick क्या है?

Q2. Merge और Cherry-pick में क्या अंतर है?

Q3. Cherry-pick कब उपयोग किया जाता है?

Q4. Cherry-pick Conflict कैसे Resolve करेंगे?

Q5. Cherry-pick के बाद कौन सा Commit आता है?

---

# 🧠 Quick Revision

```
Feature Branch

↓

Specific Commit

↓

Cherry-pick

↓

Main Branch
```

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Cherry-pick

✔ Specific Commit Copy

✔ Merge vs Cherry-pick

✔ Conflict Handling

✔ Production Workflow

अगले Chapter में हम Git Ignore सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Reset

➡ Next: Git Ignore

-----


# 🔥  Important Note Cherry-pick Commit को Move नहीं करता

Cherry-pick किसी Commit को उसकी Original Branch से हटाता नहीं है।

यह उसी Commit की एक नई Copy दूसरी Branch पर बना देता है।

इसलिए Original Branch और Target Branch दोनों में वह Change मौजूद रहेगा।

----

# 🔥 Real Production Scenario Enterprise Hotfix Scenario

मान लो

Feature Branch में 15 Commits हैं।

```
Feature Branch

↓

Commit 1

↓

Commit 2

↓

Commit 3 (Critical Bug Fix)

↓

Commit 4

↓

Commit 5
```

Production में केवल Bug Fix चाहिए।

पूरी Feature Branch Merge नहीं करनी।

ऐसे समय

```
git checkout main

git cherry-pick <Commit-3-ID>
```

अब केवल वही Bug Fix Main Branch में आ जाएगा।

बाकी Development Commits Feature Branch में ही रहेंगे।

यही तरीका Enterprise Projects में Hotfix Deploy करने के लिए अक्सर उपयोग किया जाता है।

----

# 💻 Practical

Commit History देखें

git log --oneline

मान लो Output

9ac41ef Add Login Feature

7bd124f Fix Azure NSG Rule

3cae112 Initial Commit

अब केवल Bug Fix Commit दूसरी Branch में लाना है

git cherry-pick 7bd124f

अगर Conflict आए

git status

Conflict Resolve करें

फिर

git add .

git cherry-pick --continue

अगर Cherry-pick Cancel करना हो

git cherry-pick --abort

History Verify करें

git log --oneline

----

# 🚀 Topic Complete होने के बाद

git add .

git commit -m "docs(git): add cherry-pick documentation"

git push

----

# 💡 Senior Engineer Tip (Golden Memory Trick)

- इसे हमेशा याद रखना:

Merge
=
पूरी Branch
Cherry-pick
=
सिर्फ एक Commit

और यह Diagram हमेशा दिमाग में रखना:

Feature Branch

A
│
B
│
C (Bug Fix)  ✅
│
D
│
E

          │
          │ git cherry-pick C
          ▼

Main Branch

A
│
M1
│
M2
│
C ✅

----

# 🧠 10 सेकंड का Interview Answer

अगर Interviewer पूछे:

"Cherry-pick क्या है?"

तो सीधे बोलना:

Git Cherry-pick का उपयोग किसी दूसरी Branch से केवल एक Specific Commit को Current Branch में Apply करने के लिए किया 

----