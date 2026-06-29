# Lab 05 - Commit

## 🎯 Objective

इस Lab में आप Git Commit बनाना, Meaningful Commit Messages लिखना और Commit History Verify करना सीखेंगे।

---

# 📋 Prerequisites

- Git Repository पहले से Initialize होनी चाहिए।
- Files Staging Area में Add होनी चाहिए।

---

# 🌍 Real World Scenario

Hello Team,

आज हम Project Documentation पर किए गए Changes को Repository में Save करेंगे।

Enterprise Environment में हर Change को एक Meaningful Commit Message के साथ Save किया जाता है ताकि भविष्य में किसी भी Change को आसानी से Track किया जा सके।

मैं आपको एक Example दिखाऊँगा, उसके बाद आपको उसी Pattern पर Practice करनी है।

---

# 📝 Task 1 - Repository Status Verify करें

Current Status Check करें।

### Example

```bash
git status
```

---

# 📝 Task 2 - पहला Commit करें

README.md के Changes Commit करें।

### Example

```bash
git commit -m "docs: create project readme"
```

---

# 📝 Task 3 - Commit History Verify करें

Commit History देखें।

### Example

```bash
git log --oneline
```

---

# 📝 Task 4 - दूसरा Commit करें

Azure.md में कुछ Information Add करें।

Stage करें।

Commit करें।

### Example

```bash
git commit -m "docs: add Azure documentation"
```

---

# 📝 Task 5 - तीसरा Commit करें

Terraform.md Update करें।

### Example

```bash
git commit -m "docs: add Terraform notes"
```

---

# 📝 Task 6 - Practice Assignment

नीचे दिए गए सभी Topics पर एक-एक Commit करें।

```
Storage

Virtual Network

Virtual Machine

NSG

Key Vault
```

Commit Message स्वयं लिखें।

---

# 📝 Task 7 - Professional Commit Messages

नीचे दिए गए Prefix का उपयोग करके कम से कम एक-एक Commit करें।

```
docs:

feat:

fix:

refactor:

chore:
```

---

# 📝 Task 8 - Repeat Practice

कम से कम 10 अलग-अलग Meaningful Commits करें।

हर Commit से पहले

- File Modify करें।
- Stage करें।
- Commit करें।
- History Verify करें।

---

# ✅ Verification Checklist

- Commit Successfully Create हुआ।
- Commit History Verify की।
- Meaningful Commit Messages उपयोग किए।
- कम से कम 10 Commits Complete किए।
- `git log --oneline` Successfully Verify किया।

---

# 🏆 Final Challenge

बिना Notes देखे

10 नई Commits Create करें।

हर Commit का Message अलग होना चाहिए।

Commit History Verify करें और सुनिश्चित करें कि सभी Commits सही क्रम में दिखाई दे रहे हैं।

---

# 📚 आपने क्या सीखा?

- Git Commit Create करना।
- Meaningful Commit Message लिखना।
- Commit History Verify करना।
- Professional Commit Naming Follow करना।
- Repository Changes को Version History में Save करना।