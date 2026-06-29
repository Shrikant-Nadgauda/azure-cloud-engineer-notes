git status हमें बताता है कि कौन-सी File बदली है।

लेकिन

git diff बताता है कि उस File के अंदर क्या-क्या बदला है।

यही सबसे बड़ा अंतर है।

📘 Topic 24 - Git Diff
# Git Diff

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Git Diff क्या है?
- Git Diff की आवश्यकता क्यों होती है?
- Working Directory और Staging Area का Difference
- Commit के बीच Difference कैसे देखें?
- Branch के बीच Difference कैसे देखें?
- Production में Git Diff का उपयोग

---

# Git Diff क्या है?

Git Diff एक Command है

जिसका उपयोग दो Versions के बीच का Difference देखने के लिए किया जाता है।

यह बताती है

✔ कौन-सी Line बदली

✔ कौन-सी Line हटाई

✔ कौन-सी Line जोड़ी

---

# आसान उदाहरण

मान लो

README.md

पहले

```
Azure Notes
```

अब

```
Azure Cloud Notes
```

अगर

```bash
git diff
```

चलाओगे

तो Git दोनों Versions का अंतर दिखाएगा।

---

# Basic Command

```bash
git diff
```

यह

Working Directory

और

Staging Area

के बीच का Difference दिखाता है।

---

# Stage किए हुए Changes

```bash
git diff --staged
```

या

```bash
git diff --cached
```

यह दिखाता है

कि अगली Commit में क्या-क्या जाएगा।

---

# दो Commits का Difference

```bash
git diff <commit1> <commit2>
```

उदाहरण

```bash
git diff a12345 b67890
```

---

# दो Branch का Difference

```bash
git diff main feature-login
```

अब Git दोनों Branch के बीच का Difference दिखाएगा।

---

# किसी Specific File का Difference

```bash
git diff README.md
```

---

# Git Diff कैसे पढ़ें?

Example

```diff
-Azure Notes

+Azure Cloud Notes
```

Meaning

```
- = हटाई गई Line

+ = नई जोड़ी गई Line
```

---

# Git Diff Workflow

```
File Edit

↓

git diff

↓

Review Changes

↓

git add

↓

git diff --staged

↓

git commit
```

---

# Real Industry Example

Developer ने

100 Lines का Code बदला।

Commit करने से पहले

```
git diff
```

चलाया।

उसे पता चला

कि गलती से

Password

भी File में Save हो गया है।

अब वह उसे Remove करके

सही Commit करता है।

---

# Common Mistakes

❌ Diff देखे बिना Commit करना।

❌ Secret Information Commit कर देना।

❌ Wrong File Stage कर देना।

❌ Diff और Log को Confuse करना।

---

# Best Practices

✔ Commit से पहले

```bash
git diff
```

देखें।

✔ Stage के बाद

```bash
git diff --staged
```

देखें।

✔ Pull Request से पहले Difference Review करें।

---

# Git Status vs Git Diff

| Git Status | Git Diff |
|------------|----------|
| कौन-सी File बदली | File के अंदर क्या बदला |
| Summary दिखाता है | Actual Changes दिखाता है |
| Fast Overview | Detailed Review |

---

# 🏭 Production Note

Enterprise Projects में

Code Review

Pull Request

Bug Investigation

Merge Approval

सबमें

```
git diff
```

का उपयोग किया जाता है।

Code Review की शुरुआत अक्सर Diff से होती है।

---

# Interview Questions

Q1. Git Diff क्या है?

Q2. git diff और git status में क्या अंतर है?

Q3. git diff --staged क्या करता है?

Q4. दो Branch का Difference कैसे देखेंगे?

Q5. Production में Git Diff क्यों महत्वपूर्ण है?

---

# 🧠 Quick Revision

```
File Change

↓

git diff

↓

Review

↓

git add

↓

git diff --staged

↓

Commit
```

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Git Diff

✔ Working Directory Difference

✔ Staged Difference

✔ Branch Difference

✔ Commit Difference

✔ Production Workflow

अगले Chapter में हम Merge Conflict सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Git Status

➡ Next: Merge Conflict


# 🔥 24.1 Important Note / Git Diff कोई बदलाव नहीं करता

Git Diff केवल Files के बीच का Difference दिखाता है।

यह Repository, Commit या Files में कोई बदलाव नहीं करता।

इसी कारण यह पूरी तरह Safe Command है।

# 🔥 24.2 Real Production Scenario Production Code Review

मान लो

तुमने

Terraform Project में

20 Files Modify की हैं।

Commit करने से पहले

```bash
git diff
```

चलाया।

तुम्हें पता चला कि

```
terraform.tfvars
```

में Test Password भी Save हो गया है।

अगर बिना Review किए Commit करते,

तो Sensitive Information GitHub पर चली जाती।

इसीलिए Enterprise Teams में Commit से पहले `git diff` देखना एक Standard Practice है।

---

# 💻 Practical

# Current Changes देखें

git diff

- Stage करें

git add README.md

- Staged Changes देखें

git diff --staged

- दो Commits Compare करें

git diff HEAD~1 HEAD

- दो Branch Compare करें

git diff main feature-login

- Specific File Compare करें

git diff README.md

---

# 🚀 Topic Complete होने के बाद

git add .

git commit -m "docs(git): add git diff documentation"

git push

# 💡 Senior Engineer Tip (Golden Rule)

- इन चार Commands का Flow हमेशा याद रखना:

git status
      │
      ▼
कौन-सी File बदली?

      │
      ▼
git diff
      │
      ▼
क्या बदला?

      │
      ▼
git add
      │
      ▼
git diff --staged
      │
      ▼
क्या Commit होने वाला है?

      │
      ▼
git commit

# 🧠 10 सेकंड का Interview Answer

अगर Interviewer पूछे:

"git diff का उपयोग क्या है?"

तो सीधे बोलना:

git diff का उपयोग दो Versions के बीच का अंतर देखने के लिए किया जाता है। इससे पता चलता है कि कौन-सी Lines जोड़ी गई हैं, हटाई गई हैं या बदली गई हैं। इसका उपयोग Commit से पहले Code Review, Pull Request Review और Bug Investigation में किया जाता है।

----