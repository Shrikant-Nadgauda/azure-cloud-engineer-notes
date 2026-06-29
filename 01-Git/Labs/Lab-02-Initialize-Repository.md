# Lab 02 - Initialize Repository

## 🎯 Objective

इस Lab में आप एक नए Folder को Git Repository में Initialize करना सीखेंगे और `.git` Folder की Structure को समझेंगे।

---

# 📋 Prerequisites

- Git Installed होना चाहिए।
- Git Configuration पहले से Complete होनी चाहिए।
- Git Bash या PowerShell उपलब्ध होना चाहिए।

---

# 🌍 Real World Scenario

Hello Team,

Workspace तैयार हो चुका है।

अब हमें Project को Git के द्वारा Version Control में लाना है।

आज का Task है एक नए Project को Git Repository के रूप में Initialize करना और Verify करना कि Repository सही तरीके से Create हुई है।

मैं आपको एक Example दिखाऊँगा, उसके बाद आपको उसी Pattern पर Practice करनी है।

---

# 📝 Task 1 - Project Folder Create करें

नीचे दिया गया Folder Create करें।

```
D:\
└── Audix-Git-Repository
```

### Example

```powershell
mkdir D:\Audix-Git-Repository
```

---

# 📝 Task 2 - Project Folder Open करें

Folder के अंदर जाएँ।

### Example

```bash
cd /d/Audix-Git-Repository
```

---

# 📝 Task 3 - Repository Initialize करें

Current Folder को Git Repository बनाएँ।

### Example

```bash
git init
```

---

# 📝 Task 4 - Hidden Files Verify करें

Check करें कि `.git` Folder Create हुआ है या नहीं।

### Example

```bash
ls -la
```

या

```powershell
dir -Force
```

---

# 📝 Task 5 - Repository Status Check करें

Repository की Current Status Verify करें।

### Example

```bash
git status
```

---

# 📝 Task 6 - Practice Assignment

अब नीचे दिए गए पाँच Project Folders Create करें और हर Folder में Git Repository Initialize करें।

```
Audix-Network

Audix-Azure

Audix-Terraform

Audix-DevOps

Audix-Production
```

हर Folder के लिए

- Create Folder
- Open Folder
- Run `git init`
- Verify `.git`
- Run `git status`

---

# 📝 Task 7 - Cleanup Practice

ऊपर बनाए गए सभी Practice Folders Delete करें।

फिर वही पाँचों Folder दोबारा Create करें और Repository Initialize करें।

---

# ✅ Verification Checklist

- Repository Successfully Initialize हुई।
- `.git` Folder Create हुआ।
- `git status` Successfully Run हुआ।
- सभी Practice Tasks Complete हुए।
- Cleanup और Recreate Successfully किया।

---

# 🏆 Final Challenge

बिना Notes देखे नीचे दिया गया Folder Create करें।

```
Audix-Disaster-Recovery
```

उसे Git Repository में Initialize करें और Verify करें कि `.git` Folder Successfully Create हुआ है।

---

# 📚 आपने क्या सीखा?

- Git Repository Initialize करना
- `.git` Folder Verify करना
- Repository Status Check करना
- Multiple Repositories Create करना
- Repository Delete और Recreate करना