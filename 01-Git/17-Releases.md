📘 Topic 17 - Releases
# Releases

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Release क्या होता है?
- Release की आवश्यकता क्यों होती है?
- Release और Tag में अंतर
- GitHub Release कैसे बनाते हैं?
- Release Notes क्या होती हैं?
- Production Release Workflow

---

# Release क्या होता है?

Release किसी Project के Stable Version को Public या Team के लिए Publish करना होता है।

GitHub में Release हमेशा किसी Tag के आधार पर बनाया जाता है।

उदाहरण

```
v1.0.0

↓

Git Tag

↓

GitHub Release
```

---

# आसान उदाहरण

मान लो Project पूरा हो गया।

तुमने

```
v1.0.0
```

Tag बनाया।

अब GitHub पर उसी Tag से

Release Publish कर दी।

अब सभी Users उसी Stable Version को Download कर सकते हैं।

---

# Release क्यों उपयोग करते हैं?

✔ Stable Version Publish करना

✔ Software Distribution

✔ Release Notes देना

✔ Downloadable Files उपलब्ध कराना

✔ Version History Maintain करना

✔ CI/CD Deployment Trigger करना

---

# Tag और Release में अंतर

| Tag | Release |
|------|----------|
| Git Feature | GitHub Feature |
| केवल Commit Mark करता है | Stable Version Publish करता है |
| Message हो सकता है | Detailed Release Notes होती हैं |
| Git Repository का भाग | GitHub Platform का भाग |
| Version Marking | Software Distribution |

---

# Release Workflow

```
Code Complete

↓

Testing

↓

Merge

↓

Tag

↓

GitHub Release

↓

Deployment
```

---

# GitHub Release कैसे बनाएं?

Step 1

Repository खोलें।

↓

Step 2

Releases पर जाएं।

↓

Step 3

New Release

↓

Step 4

Existing Tag चुनें

या

New Tag बनाएं।

↓

Step 5

Release Title लिखें।

↓

Step 6

Release Notes लिखें।

↓

Step 7

Publish Release

---

# Release Notes क्या होती हैं?

Release Notes में लिखा जाता है

✔ New Features

✔ Bug Fixes

✔ Improvements

✔ Known Issues

✔ Upgrade Instructions

---

# Example Release Notes

```
Version

v1.1.0

New Features

- Azure Bastion Support

- Terraform Modules

- NSG Automation

Bug Fixes

- Storage Issue Fixed

- VNet Validation Improved

Known Issues

- Monitoring Module Pending
```

---

# Release Assets

GitHub Release के साथ

ZIP

Source Code

Binary Files

Scripts

Documents

भी Attach किए जा सकते हैं।

---

# Real Industry Example

Developer

↓

Feature Complete

↓

Testing

↓

Code Review

↓

Merge

↓

Tag

v2.0.0

↓

GitHub Release

↓

Production Deployment

---

# Common Mistakes

❌ बिना Tag के Release बनाना।

❌ Release Notes नहीं लिखना।

❌ Development Version को Stable Release बना देना।

❌ Version Number गलत रखना।

---

# Best Practices

✔ Semantic Versioning Follow करें।

✔ Annotated Tag उपयोग करें।

✔ Detailed Release Notes लिखें।

✔ Stable Code पर ही Release बनाएं।

✔ Release Publish करने से पहले Testing पूरी करें।

---

# 🏭 Production Note

Enterprise Projects में Release Publish होने के बाद

CI/CD Pipeline

Automatic

Build

↓

Test

↓

Deploy

भी कर सकती है।

कई Organizations Production Deployment को Tag या Release Event से Trigger करती हैं।

---

# Interview Questions

Q1. GitHub Release क्या है?

Q2. Tag और Release में क्या अंतर है?

Q3. Release Notes क्या होती हैं?

Q4. Release Assets क्या हैं?

Q5. Production में Release क्यों बनाया जाता है?

---

# 🧠 Quick Revision

```
Commit

↓

Tag

↓

GitHub Release

↓

Deployment
```

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ GitHub Release

✔ Tag vs Release

✔ Release Notes

✔ Release Assets

✔ Production Workflow

अगले Chapter में हम Revert सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Tags

➡ Next: Revert

------

# 🔥  Important Note / Tag और Release का संबंध

हर Release के पीछे एक Tag होता है।

लेकिन

हर Tag के लिए Release बनाना आवश्यक नहीं है।

उदाहरण

v0.9.0

↓

Testing Tag

(No Release)

v1.0.0

↓

Stable Tag

↓

GitHub Release

----

# 💻 Practical (GitHub)

- 1. Tag Push करें
git push origin v1.0.0

- 2. GitHub Repository खोलें
Releases

↓

New Release

- 3. Tag चुनें
v1.0.0

- 4. Release Title
Azure Cloud Engineering v1.0.0

- 5. Release Notes

Initial Stable Release

Features

- Git Notes

- GitHub Documentation

- Linux Roadmap

- Azure Roadmap

Bug Fixes

- Initial Structure Completed
6. Publish Release

अब GitHub पर पहला Official Release बन जाएगा।

----

# 🔥 Real Production Scenario / Enterprise Release Process

Developer

↓

Feature Branch

↓

Pull Request

↓

Code Review

↓

Testing

↓

Merge into Main

↓

Create Tag

v2.1.0

↓

GitHub Release

↓

CI/CD Pipeline

↓

Production Deployment

यही Workflow अधिकांश Enterprise Organizations में Follow किया जाता है।

----

# 🚀 Topic Complete होने के बाद

git add .

git commit -m "docs(git): add releases documentation"

git push

---

# 💡 Senior Engineer Tip (Golden Flow)

- इस पूरे Flow को हमेशा याद रखना:

Developer
      │
      ▼
git add
      │
      ▼
git commit
      │
      ▼
git push
      │
      ▼
GitHub Repository
      │
      ▼
Create Tag
      │
      ▼
Create Release
      │
      ▼
CI/CD Pipeline
      │
      ▼
Production

---