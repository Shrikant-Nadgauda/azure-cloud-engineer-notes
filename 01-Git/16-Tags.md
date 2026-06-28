# 📘 Topic 16 - Tags
# Tags

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Tag क्या होता है?
- Tag की आवश्यकता क्यों होती है?
- Lightweight Tag
- Annotated Tag
- Tag बनाना
- Tag Delete करना
- GitHub पर Tag Push करना
- Production Release Workflow

---

# Tag क्या होता है?

Tag एक विशेष Label होता है

जो किसी विशेष Commit को स्थायी रूप से पहचान देता है।

उदाहरण

```
v1.0.0

↓

Commit A34F21
```

अब चाहे बाद में कितने भी Commit हो जाएं,

Tag हमेशा उसी Commit पर रहेगा।

---

# आसान उदाहरण

मान लो

Project Complete हुआ।

अब Company ने पहला Stable Version Release किया।

उस Commit पर

```
v1.0.0
```

Tag लगा दिया।

अब भविष्य में कोई भी Engineer

उसी Version पर वापस जा सकता है।

---

# Tag क्यों उपयोग करते हैं?

✔ Stable Release

✔ Production Version

✔ Rollback

✔ Software Versioning

✔ CI/CD Deployment

✔ GitHub Releases

---

# Tag Workflow

```
Commit

↓

Tag

↓

Push Tag

↓

GitHub Release
```

---

# सभी Tags देखें

```bash
git tag
```

---

# Lightweight Tag

```bash
git tag v1.0.0
```

यह केवल एक नाम (Label) बनाता है।

---

# Annotated Tag

Production में यही उपयोग होता है।

```bash
git tag -a v1.0.0 -m "First Stable Release"
```

इसमें

✔ Author

✔ Date

✔ Message

Store होती है।

---

# Tag Information देखें

```bash
git show v1.0.0
```

---

# Tag Push करें

केवल Local Tag बनाना पर्याप्त नहीं है।

GitHub पर भेजना होगा।

```bash
git push origin v1.0.0
```

---

# सभी Tags Push करें

```bash
git push origin --tags
```

---

# Tag Delete

Local

```bash
git tag -d v1.0.0
```

Remote

```bash
git push origin --delete v1.0.0
```

---

# Tag Checkout

```bash
git checkout v1.0.0
```

अब Project उसी Version पर खुल जाएगा।

---

# Real Industry Example

Version History

```
v1.0.0

↓

Initial Release

↓

v1.1.0

↓

Bug Fix

↓

v2.0.0

↓

Major Features
```

---

# Semantic Versioning

Production में सामान्यतः

```
MAJOR.MINOR.PATCH
```

उदाहरण

```
1.0.0

1.1.0

1.1.1

2.0.0
```

---

# Version Meaning

```
1.0.0

↓

First Stable Release

1.1.0

↓

New Feature Added

1.1.1

↓

Bug Fix

2.0.0

↓

Breaking Changes
```

---

# Common Mistakes

❌ Tag बनाकर Push नहीं करना।

❌ हर Commit पर Tag लगा देना।

❌ Wrong Version Number देना।

❌ Production Release बिना Tag के करना।

---

# Best Practices

✔ केवल Stable Commits पर Tag लगाएं।

✔ Annotated Tags उपयोग करें।

✔ Semantic Versioning Follow करें।

✔ GitHub Release के साथ Tag Publish करें।

---

# 🏭 Production Note

Enterprise Projects में

Deployment Pipeline

अक्सर

```
Tag

↓

Build

↓

Test

↓

Deploy
```

के आधार पर Trigger होती है।

इसलिए Tags Production Automation का महत्वपूर्ण भाग हैं।

---

# Interview Questions

Q1. Git Tag क्या है?

Q2. Lightweight और Annotated Tag में अंतर?

Q3. Tag को GitHub पर कैसे Push करते हैं?

Q4. Semantic Versioning क्या है?

Q5. Production में Tags क्यों उपयोग किए जाते हैं?

---

# 🧠 Quick Revision

```
Commit

↓

Tag

↓

Push

↓

GitHub Release
```

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Tags

✔ Annotated Tag

✔ Lightweight Tag

✔ Push Tag

✔ Semantic Versioning

✔ Production Release

अगले Chapter में हम GitHub Releases सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Fetch

➡ Next: Releases

--- 



# 🔥 Important Note Branch और Tag में अंतर

Branch एक Moving Pointer है।

जैसे-जैसे नए Commit होते हैं,
Branch आगे बढ़ती रहती है।

लेकिन

Tag एक Fixed Pointer है।

एक बार जिस Commit पर Tag लगा दिया,

वह हमेशा उसी Commit पर रहेगा।

इसी कारण Release के लिए Tag उपयोग किया जाता है।

---

# 🔥 Real Production Scenario / Enterprise Release Workflow

Developer

↓

Feature Complete

↓

Testing

↓

Code Review

↓

Merge into Main

↓

Create Tag

v1.0.0

↓

Push Tag

↓

GitHub Release

↓

CI/CD Deployment

इस Workflow का उपयोग अधिकांश Enterprise Projects में किया जाता है।

---

# 💻 Practical

- सभी Tags देखें

git tag

- Lightweight Tag बनाएं

git tag v1.0.0

- Annotated Tag बनाएं (Recommended)

git tag -a v1.0.0 -m "First stable release"

- Tag की जानकारी देखें

git show v1.0.0

- GitHub पर Tag Push करें

git push origin v1.0.0

- सभी Tags Push करें

git push origin --tags

- Local Tag Delete करें

git tag -d v1.0.0

- Remote Tag Delete करें

git push origin --delete v1.0.0

---

# 🚀 Topic Complete होने के बाद

- git add .

- git commit -m "docs(git): add tags documentation"

- git push

---

# 💡 Senior Engineer Tip

एक Concept हमेशा याद रखना:

Commit = Development का Record

Branch = Development की Line

Tag = Release का Snapshot

Visualize ऐसे करो:

A──B──C──D──E──F
         │
       v1.0.0

Branch (main) आगे बढ़ती रहेगी

A──B──C──D──E──F──G──H
         │
       v1.0.0

Tag हमेशा Commit `C` पर ही रहेगा।

----