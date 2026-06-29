# Lab 02 - Working Directory

## 🎯 Objective

इस Lab में आप Git Working Directory में Files Create, Modify और Delete करना सीखेंगे तथा `git status` के माध्यम से उनके Changes को Verify करेंगे।

---

# 📋 Prerequisites

- Git Repository पहले से Initialize होनी चाहिए।
- Git Bash या PowerShell उपलब्ध होना चाहिए।

---

# 🌍 Real World Scenario

Hello Team,

हमारी Git Repository तैयार हो चुकी है।

अब हमें Project Documentation पर काम शुरू करना है।

आज का Task है Repository के अंदर नई Files Create करना, Existing Files को Modify करना और Git के माध्यम से Changes को Track करना।

मैं आपको एक Example दिखाऊँगा, उसके बाद आपको उसी Pattern पर Practice करनी है।

---

# 📝 Task 1 - Project Folder Open करें

पहले अपनी Git Repository के अंदर जाएँ।

### Example

```bash
cd /d/Audix-Git-Repository
```

---

# 📝 Task 2 - Repository Status Check करें

Current Repository की Status Check करें।

### Example

```bash
git status
```

---

# 📝 Task 3 - नई Files Create करें

नीचे दी गई Files Create करें।

```
README.md

Network.md

Azure.md
```

---

# 📝 Task 4 - Changes Verify करें

Repository की Status दोबारा Check करें।

### Example

```bash
git status
```

Verify करें कि सभी Files **Untracked** दिखाई दे रही हैं।

---

# 📝 Task 5 - Existing File Modify करें

README.md में नीचे दिया गया Text Add करें।

```
Azure Cloud Engineering Lab
```

Status फिर से Verify करें।

---

# 📝 Task 6 - नई Files Add करें

अब नीचे दी गई तीन नई Files Create करें।

```
Terraform.md

Docker.md

Kubernetes.md
```

Status Verify करें।

---

# 📝 Task 7 - File Delete करें

Network.md Delete करें।

Status Check करें।

Verify करें कि Git Delete हुए File को Detect कर रहा है।

---

# 📝 Task 8 - Practice Assignment

नीचे दिए गए पाँच Documentation Files स्वयं Create करें।

```
Storage.md

Virtual-Machine.md

Virtual-Network.md

NSG.md

Azure-DevOps.md
```

अब

- किसी भी 2 Files में Changes करें।
- 1 File Delete करें।
- हर Step के बाद `git status` Run करें।

---

# ✅ Verification Checklist

- Repository Successfully Open हुई।
- New Files Create हुईं।
- Existing File Modify की गई।
- File Delete की गई।
- हर Change के बाद `git status` Verify किया।
- Git ने सभी Changes Detect किए।

---

# 🏆 Final Challenge

बिना Notes देखे

एक नया Folder Create करें।

उसके अंदर कम से कम 5 Markdown Files बनाएँ।

- 2 Files Modify करें।
- 1 File Delete करें।
- हर Step के बाद `git status` Run करें।

---

# 📚 आपने क्या सीखा?

- Working Directory में काम करना।
- नई Files Create करना।
- Existing Files Modify करना।
- Files Delete करना।
- `git status` के माध्यम से Changes Verify करना।