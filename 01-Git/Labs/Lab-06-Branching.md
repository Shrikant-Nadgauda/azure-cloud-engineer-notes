# Lab 06 - Branching

## 🎯 Objective

इस Lab में आप नई Branch Create करना, Branch Switch करना, Branch Rename करना और Branch Delete करना सीखेंगे।

---

# 📋 Prerequisites

- Git Repository पहले से Create होनी चाहिए।
- Repository में कम से कम एक Commit होना चाहिए।

---

# 🌍 Real World Scenario

Hello Team,

बहुत बढ़िया काम!

आप सभी ने **Audix Azure Cloud Project** के लिए Workspace तैयार किया, Project Repository Create की, Files Manage कीं और Documentation को Successfully Commit भी कर दिया.

अब Project में नए Engineers Join हो चुके हैं.

पूरी Team एक ही Repository पर काम करेगी.

यदि सभी Developers सीधे **main** Branch पर काम करेंगे, तो Code Conflicts, Data Loss और Production Issues होने की संभावना बढ़ जाएगी.

इसी समस्या को रोकने के लिए Enterprise Projects में हर Developer अपनी अलग **Feature Branch** पर काम करता है.

आज से आप भी उसी Professional Workflow को Follow करेंगे.

मैं आपको एक Example दिखाऊँगा, उसके बाद आपको उसी Pattern पर Project की अलग-अलग Features के लिए अपनी Branches Create करनी हैं.

---

# 📝 Task 1 - Current Branch Verify करें

Current Branch Check करें.

### Example

```bash
git branch
```

---

# 📝 Task 2 - Feature Branch Create करें

नीचे दी गई Branch Create करें.

```
feature/login
```

### Example

```bash
git branch feature/login
```

---

# 📝 Task 3 - Branch Switch करें

नई Branch पर जाएँ.

### Example

```bash
git switch feature/login
```

या

```bash
git checkout feature/login
```

Verify करें कि आप सही Branch पर हैं.

```bash
git branch
```

---

# 📝 Task 4 - Multiple Branches Create करें

नीचे दी गई सभी Branches Create करें.

```
feature/network

feature/terraform

feature/storage

feature/security

feature/monitoring
```

---

# 📝 Task 5 - Branch Switching Practice

एक-एक करके सभी Branches पर जाएँ.

हर Branch Switch करने के बाद Verify करें.

```bash
git branch
```

---

# 📝 Task 6 - Branch Rename करें

नीचे दी गई Branch का नाम बदलें.

```
feature/storage

↓

feature/storage-account
```

---

# 📝 Task 7 - Branch Delete करें

Practice के लिए नीचे दी गई Branch Delete करें.

```
feature/network
```

Verify करें कि Branch Delete हो चुकी है.

---

# 📝 Task 8 - Practice Assignment

अब नीचे दिए गए Project Modules के लिए स्वयं Branches Create करें.

```
feature/vnet

feature/vm

feature/nsg

feature/keyvault

feature/devops
```

हर Branch के लिए

- Branch Create करें.
- Branch Switch करें.
- Current Branch Verify करें.
- वापस main Branch पर आएँ.

---

# ✅ Verification Checklist

- Current Branch Verify की.
- नई Branch Create की.
- Branch Switch की.
- Multiple Branches Create कीं.
- Branch Rename की.
- Branch Delete की.
- सभी Practice Tasks Successfully Complete किए.

---

# 🏆 Final Challenge

बिना Notes देखे

नीचे दिए गए सभी Branches Create करें.

```
feature/application-gateway

feature/load-balancer

feature/private-endpoint

feature/bastion

feature/aks
```

अब

- सभी Branches पर Switch करें.
- एक Branch Rename करें.
- एक Branch Delete करें.
- अंत में main Branch पर वापस आएँ.

---

# 📚 आपने क्या सीखा?

- Branch Create करना.
- Branch Switch करना.
- Current Branch Verify करना.
- Branch Rename करना.
- Branch Delete करना.
- Enterprise Branching Workflow को Follow करना.