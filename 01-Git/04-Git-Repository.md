# Git Repository

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Git Repository क्या होती है?
- Repository की आवश्यकता क्यों होती है?
- Local और Remote Repository
- Repository कैसे बनाई जाती है?
- Existing Repository कैसे Clone करते हैं?
- Real Industry Example

---

# Git Repository क्या है?

Git Repository (Repo) वह स्थान है जहाँ Project का पूरा Source Code और उसकी Version History सुरक्षित रहती है।

सरल भाषा में:

> Git Repository = Project का घर (Home)

यहीं Project की सभी Files, Commits, Branches और History रहती है।

---

# Repository की आवश्यकता क्यों होती है?

अगर Repository नहीं होगी,

तो Git यह Track नहीं कर पाएगा कि

✔ कौन-सी File बदली

✔ कब बदली

✔ किसने बदली

✔ क्यों बदली

Repository Git को Project Manage करने की जगह देती है।

---

# Repository में क्या-क्या होता है?

एक Git Repository में सामान्यतः:

✔ Source Code

✔ Commit History

✔ Branches

✔ Tags

✔ Configuration Files

✔ Hidden `.git` Folder

---

# Repository के प्रकार

## 1. Local Repository

यह आपकी Local Machine पर होती है।

यहीं Developer अपना Code लिखता और Test करता है।

उदाहरण:

```
D:\Cloud-Engineering
```

---

## 2. Remote Repository

यह GitHub, Azure DevOps या GitLab जैसे Server पर होती है।

यहीं पूरी Team अपना Code Share करती है।

उदाहरण:

```
https://github.com/username/project.git
```

---

# Git Repository कैसे बनती है?

नई Repository बनाने के लिए:

```bash
git init
```

यह Command Current Folder को Git Repository में बदल देती है।

---

# Existing Repository कैसे प्राप्त करें?

अगर Repository पहले से GitHub पर है:

```bash
git clone <repository-url>
```

Example

```bash
git clone https://github.com/user/project.git
```

---

# Repository बनने के बाद क्या होता है?

`git init` चलाने के बाद एक Hidden Folder बनता है।

```
.git
```

इसी Folder में Git अपनी पूरी History Store करता है।

यदि यह Folder Delete हो जाए,

तो Project Files रहेंगी,

लेकिन Git History समाप्त हो जाएगी।

---

# Real Industry Example

मान लो Company में Azure Infrastructure का Project चल रहा है।

Repository में मौजूद हो सकता है:

- Terraform Code
- Azure DevOps Pipelines
- Documentation
- PowerShell Scripts
- Bash Scripts
- Architecture Diagrams

पूरी Team इसी एक Repository पर मिलकर काम करती है।

---

# Practical

नई Repository बनाइए:

```bash
mkdir Git-Lab
```

```bash
cd Git-Lab
```

```bash
git init
```

Repository Verify करें:

```bash
git status
```

Hidden Files देखें:

Git Bash

```bash
ls -la
```

PowerShell

```powershell
Get-ChildItem -Force
```

---

# Verification

अगर `.git` Folder दिखाई देता है,

तो Repository Successfully बन चुकी है।

`git status` में दिखाई देगा:

```
On branch main
```

या

```
On branch master
```

---

# Best Practices

✔ प्रत्येक Project के लिए अलग Repository रखें।

✔ Repository का नाम Meaningful रखें।

✔ Repository में README.md अवश्य रखें।

✔ Sensitive Data Commit न करें।

✔ Project Structure पहले से तय करें।

---

# Common Mistakes

❌ एक ही Repository में कई अलग-अलग Projects रखना।

❌ `.git` Folder Delete कर देना।

❌ Repository बिना README के बनाना।

❌ Secret Keys Commit करना।

---

# 💡 Engineer Tip

Repository शुरू करने के पहले 10 मिनट Planning में लगाओ।

बाद में Structure बदलना मुश्किल हो सकता है।

---

# 🏭 Production Note

Enterprise Projects में Repository पहले से Standard Structure के साथ बनाई जाती है।

उदाहरण:

```
README.md
docs/
terraform/
scripts/
pipelines/
images/
```

इससे सभी Engineers एक जैसी Structure Follow करते हैं।

---

# Interview Questions

Q1. Git Repository क्या होती है?

Q2. Local और Remote Repository में क्या अंतर है?

Q3. `git init` क्या करता है?

Q4. `.git` Folder का क्या कार्य है?

Q5. `git init` और `git clone` में क्या अंतर है?

---

# 🧠 Quick Revision

Repository = Project का घर

git init = नई Repository बनाना

git clone = Existing Repository डाउनलोड करना

.git = Git की पूरी History

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Git Repository

✔ Local Repository

✔ Remote Repository

✔ git init

✔ git clone

✔ .git Folder

✔ Real Industry Example

अगले Chapter में हम Working Directory सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Git Configuration

➡ Next: Working Directory