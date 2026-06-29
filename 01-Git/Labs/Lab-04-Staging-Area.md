# Lab 04 - Staging Area

## 🎯 Objective

इस Lab में आप Git Staging Area को समझेंगे और `git add` का उपयोग करके Files को Stage करना सीखेंगे।

---

# 📋 Prerequisites

- Git Repository पहले से Initialize होनी चाहिए।
- Repository में कुछ Untracked या Modified Files होनी चाहिए।

---

# 🌍 Real World Scenario

Hello Team,

आज से हम Project में Changes को Commit करने की तैयारी करेंगे।

लेकिन किसी भी Change को Commit करने से पहले उसे **Staging Area** में भेजना आवश्यक होता है।

आज आपका Task है अलग-अलग Files को Stage करना, Verify करना और समझना कि Git Commit से पहले Files को कैसे Manage करता है।

मैं आपको एक Example दिखाऊँगा, उसके बाद आपको उसी Pattern पर Practice करनी है।

---

# 📝 Task 1 - Project Folder Open करें

Repository के अंदर जाएँ।

### Example

```bash
cd /d/Audix-Git-Repository
```

---

# 📝 Task 2 - Repository Status Check करें

Current Status Verify करें।

### Example

```bash
git status
```

---

# 📝 Task 3 - नई Files Create करें

नीचे दी गई Files Create करें।

```
README.md

Azure.md

Terraform.md

Docker.md
```

---

# 📝 Task 4 - Single File Stage करें

सिर्फ **README.md** को Stage करें।

### Example

```bash
git add README.md
```

Status Verify करें।

---

# 📝 Task 5 - Multiple Files Stage करें

अब Azure.md और Terraform.md को Stage करें।

### Example

```bash
git add Azure.md Terraform.md
```

Status Verify करें।

---

# 📝 Task 6 - सभी Files Stage करें

बाकी बची हुई सभी Files को Stage करें।

### Example

```bash
git add .
```

Status Verify करें।

सभी Files **Changes to be committed** में दिखाई देनी चाहिए।

---

# 📝 Task 7 - Practice Assignment

नीचे दी गई पाँच Files Create करें।

```
Storage.md

Virtual-Network.md

Virtual-Machine.md

NSG.md

KeyVault.md
```

अब Practice करें।

- सिर्फ 1 File Stage करें।
- फिर 2 Files Stage करें।
- फिर सभी Files Stage करें।
- हर Step के बाद `git status` Run करें।

---

# 📝 Task 8 - Repeat Practice

ऊपर वाला पूरा Process कम से कम 5 बार Repeat करें।

हर बार अलग-अलग Files Select करें।

---

# ✅ Verification Checklist

- Single File Successfully Stage हुई।
- Multiple Files Successfully Stage हुईं।
- सभी Files Successfully Stage हुईं।
- हर Step के बाद `git status` Verify किया।
- Practice Assignment Successfully Complete किया।

---

# 🏆 Final Challenge

बिना Notes देखे

10 नई Markdown Files Create करें।

- पहले केवल 1 File Stage करें।
- फिर 3 Files Stage करें।
- फिर सभी Files Stage करें।
- हर Step पर `git status` Verify करें।

---

# 📚 आपने क्या सीखा?

- Staging Area क्या है।
- Single File Stage करना।
- Multiple Files Stage करना।
- सभी Files Stage करना।
- `git status` के माध्यम से Staging Verify करना।