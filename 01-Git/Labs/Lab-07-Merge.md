# Lab 07 - Merge

## 🎯 Objective

इस Lab में आप Git Branches को Merge करना, Merge से पहले आवश्यक सावधानियाँ लेना और Merge के बाद Repository Verify करना सीखेंगे।

---

# 📋 Prerequisites

- Git Repository पहले से Create होनी चाहिए।
- Repository में Multiple Branches मौजूद होनी चाहिए।
- प्रत्येक Branch में कम से कम एक Commit होना चाहिए।

---

# 🌍 Real World Scenario

Hello Team,

आप सभी ने अपनी-अपनी Feature Branch पर Development Successfully Complete कर ली है.

अब समय आ गया है कि सभी Changes को Main Project में Merge किया जाए.

लेकिन Production Repository में Merge करने से पहले कुछ महत्वपूर्ण Checks करना आवश्यक होता है.

आज हम वही Professional Workflow Follow करेंगे जो Enterprise Projects में उपयोग किया जाता है.

---

# ⚠️ Merge करने से पहले ध्यान रखें

Merge शुरू करने से पहले हमेशा नीचे दिए गए Checks करें.

- सभी Changes Commit होने चाहिए।
- Working Directory Clean होनी चाहिए।
- सही Branch पर होना चाहिए।
- Merge करने वाली Branch Updated होनी चाहिए।
- Merge से पहले `git status` Verify करें।
- आवश्यकता हो तो Backup Branch Create करें।
- Production Branch में Direct Changes न करें।
- Merge के बाद Project Verify करना न भूलें।

---

# 📝 Task 1 - Repository Status Verify करें

Repository Clean है या नहीं Verify करें.

### Example

```bash
git status
```

---

# 📝 Task 2 - Available Branches Check करें

Repository की सभी Branches देखें.

### Example

```bash
git branch
```

---

# 📝 Task 3 - Main Branch पर जाएँ

Merge हमेशा Main Branch से करें.

### Example

```bash
git switch main
```

---

# 📝 Task 4 - Feature Branch Merge करें

`feature/login` Branch को Main में Merge करें.

### Example

```bash
git merge feature/login
```

---

# 📝 Task 5 - Merge Verify करें

Merge Successfully Complete हुआ या नहीं Verify करें.

### Example

```bash
git log --oneline --graph
```

---

# 📝 Task 6 - Multiple Branches Merge करें

नीचे दी गई सभी Branches को एक-एक करके Merge करें.

```
feature/terraform

feature/security

feature/storage-account

feature/monitoring
```

हर Merge के बाद History Verify करें.

---

# 📝 Task 7 - Delete Merged Branch

Merge Successfully Complete होने के बाद Branch Delete करें.

### Example

```bash
git branch -d feature/login
```

---

# 📝 Task 8 - Practice Assignment

नीचे दिए गए सभी Branches Create करें.

```
feature/vnet

feature/vm

feature/nsg

feature/keyvault
```

हर Branch में एक छोटा Change करें.

Commit करें.

Main Branch में Merge करें.

Merge Verify करें.

Merge के बाद Branch Delete करें.

---

# ✅ Verification Checklist

- Repository Status Verify किया।
- Main Branch पर Switch किया।
- Feature Branch Successfully Merge की।
- Merge History Verify की।
- Merged Branch Delete की।
- सभी Practice Tasks Successfully Complete किए।

---

# 🏆 Final Challenge

बिना Notes देखे

कम से कम 5 Feature Branches Create करें.

हर Branch में अलग-अलग Change करें.

Commit करें.

Main Branch में Merge करें.

Merge Verify करें.

Merged Branch Delete करें.

पूरा Workflow बिना किसी Error के Complete करें.

---

# 📚 आपने क्या सीखा?

- Merge से पहले आवश्यक Checks करना।
- Main Branch में Feature Branch Merge करना।
- Merge History Verify करना।
- Merged Branch Delete करना।
- Enterprise Merge Workflow Follow करना।