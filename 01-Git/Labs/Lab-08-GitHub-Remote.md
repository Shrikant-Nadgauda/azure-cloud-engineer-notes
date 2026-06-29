# Lab 08 - GitHub Remote

## 🎯 Objective

इस Lab में आप Local Repository को Remote Repository से Connect करना, Remote Verify करना, Remote Change करना और Multiple Remote URLs के साथ Practice करना सीखेंगे।

---

# 📋 Prerequisites

- Git Repository पहले से Create होनी चाहिए.
- Repository में कम से कम एक Commit होना चाहिए.
- GitHub Account उपलब्ध होना चाहिए.

---

# 🌍 Real World Scenario

Hello Team,

हमारा **Audix Azure Cloud Project** Local Machine पर Successfully Develop हो चुका है.

अब समय आ गया है कि Project को Company के Central Git Server (GitHub) पर Publish किया जाए ताकि पूरी Team एक ही Repository पर Collaboration कर सके.

मैं आपको एक Example दिखाऊँगा, उसके बाद आपको अलग-अलग Remote Repositories के साथ स्वयं Practice करनी है.

---

# ⚠️ Remote Add करने से पहले ध्यान रखें

- सही GitHub Repository Create करें.
- Repository URL Verify करें.
- Repository Public या Private है, यह Check करें.
- Remote Name पहले से मौजूद है या नहीं Verify करें.
- `git remote -v` से हमेशा Remote Verify करें.

---

# 📝 Task 1 - GitHub Repository Create करें

GitHub पर एक नई Repository Create करें.

### Example

```
Audix-Azure-Project
```

---

# 📝 Task 2 - Remote Add करें

Local Repository को GitHub Repository से Connect करें.

### Example

```bash
git remote add origin https://github.com/username/Audix-Azure-Project.git
```

---

# 📝 Task 3 - Remote Verify करें

Verify करें कि Remote Successfully Add हुआ है.

### Example

```bash
git remote -v
```

---

# 📝 Task 4 - Project Push करें

Main Branch को पहली बार GitHub पर Push करें.

### Example

```bash
git push -u origin main
```

---

# 📝 Task 5 - दूसरा Remote बनाकर Practice करें

नीचे दिए गए Sample Repository Name का उपयोग करके दूसरा Remote Add करने की Practice करें.

```
Audix-Terraform

Audix-Network

Audix-DevOps

Audix-Security

Audix-Monitoring
```

Sample URL

```text
https://github.com/username/Audix-Terraform.git
```

> **Note:** `username` की जगह अपना GitHub Username उपयोग करें।

---

# 📝 Task 6 - Remote URL Change करें

यदि Repository का URL बदल जाए तो Remote Update करें.

### Example

```bash
git remote set-url origin https://github.com/username/New-Repository.git
```

Verify करें.

```bash
git remote -v
```

---

# 📝 Task 7 - Remote Remove करें

Practice के लिए Remote Remove करें.

### Example

```bash
git remote remove origin
```

Verify करें.

```bash
git remote -v
```

---

# 📝 Task 8 - Practice Assignment

नीचे दिए गए सभी Repository Names का उपयोग करके स्वयं Practice करें.

```
Cloud-Labs

Azure-Labs

Terraform-Labs

DevOps-Labs

Production-Labs
```

हर Repository के लिए

- Remote Add करें.
- Remote Verify करें.
- URL Change करें.
- Remote Verify करें.
- Remote Remove करें.

---

# ✅ Verification Checklist

- GitHub Repository Successfully Create की.
- Remote Successfully Add किया.
- Remote Verify किया.
- Project Successfully Push किया.
- Remote URL Successfully Change किया.
- Remote Successfully Remove किया.
- सभी Practice Tasks Complete किए.

---

# 🏆 Final Challenge

बिना Notes देखे

3 अलग-अलग GitHub Repositories Create करें.

हर Repository के लिए

- Remote Add करें.
- Project Push करें.
- Remote Verify करें.
- URL Change करें.
- Remote Remove करें.

पूरा Workflow बिना किसी Error के Complete करें.

---

# 📚 आपने क्या सीखा?

- GitHub Repository Create करना.
- Remote Add करना.
- Remote Verify करना.
- Project Push करना.
- Remote URL Update करना.
- Remote Remove करना.
- Enterprise Remote Workflow Follow करना.