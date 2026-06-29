# Lab 10 - Merge Conflict

## 🎯 Objective

इस Lab में आप Merge Conflict Create करना, Conflict को समझना, Resolve करना और Changes को Successfully Merge करना सीखेंगे।

---

# 📋 Prerequisites

- Git Repository पहले से Create होनी चाहिए.
- Repository में Multiple Branches मौजूद होनी चाहिए.
- Branches में अलग-अलग Commits होने चाहिए.

---

# 🌍 Real World Scenario

Hello Team,

हमारा **Audix Azure Cloud Project** अब Production के काफी करीब पहुँच चुका है.

दो Developers एक ही Project पर काम कर रहे थे.

- Developer A ने **README.md** में Changes किए.
- Developer B ने भी उसी **README.md** में Changes किए.

अब दोनों Developers अपने Changes को **main** Branch में Merge करना चाहते हैं.

लेकिन Git यह Decide नहीं कर सकता कि कौन सा Change सही है.

यही Situation **Merge Conflict** कहलाती है.

आज आपका उद्देश्य केवल Conflict Resolve करना नहीं है, बल्कि यह समझना है कि Enterprise Projects में Merge Conflict को सुरक्षित तरीके से कैसे Handle किया जाता है.

---

# ⚠️ Merge Conflict Resolve करने से पहले ध्यान रखें

- Conflict वाली Files को ध्यान से पढ़ें.
- बिना समझे Code Delete न करें.
- दोनों Developers के Changes Compare करें.
- सही Content Select करें.
- Conflict Resolve होने के बाद File Save करें.
- Merge Complete करने से पहले `git status` Verify करें.
- Final Commit करना न भूलें.

---

# 📝 Task 1 - Feature Branch Create करें

नीचे दी गई Branch Create करें.

```
feature/login
```

उस Branch पर Switch करें.

---

# 📝 Task 2 - README.md Modify करें

README.md में नीचे दिया गया Text Add करें.

```
Developer A Changes
```

Commit करें.

---

# 📝 Task 3 - Main Branch पर वापस जाएँ

Main Branch पर Switch करें.

```
main
```

---

# 📝 Task 4 - README.md दोबारा Modify करें

अब उसी README.md में नीचे दिया गया Text Add करें.

```
Developer B Changes
```

Commit करें.

---

# 📝 Task 5 - Merge करें

अब `feature/login` Branch को Main Branch में Merge करें.

### Example

```bash
git merge feature/login
```

Git अब Merge Conflict दिखाएगा.

---

# 📝 Task 6 - Conflict Identify करें

README.md Open करें.

Conflict Markers Identify करें.

```
<<<<<<< HEAD

=======

>>>>>>>
```

समझें कि कौन सा Change Main Branch का है और कौन सा Feature Branch का.

---

# 📝 Task 7 - Conflict Resolve करें

दोनों Developers के सही Changes रखकर File Save करें.

Conflict Markers पूरी तरह Remove करें.

---

# 📝 Task 8 - Conflict Verify करें

Repository Status Verify करें.

### Example

```bash
git status
```

---

# 📝 Task 9 - Final Commit करें

Conflict Resolve होने के बाद Final Merge Commit करें.

### Example

```bash
git commit
```

---

# 📝 Task 10 - Practice Assignment

नीचे दिए गए सभी Files पर स्वयं Merge Conflict Create करें.

```
Azure.md

Terraform.md

Docker.md

Network.md

Security.md
```

हर File के लिए

- Branch Create करें.
- Same Line Modify करें.
- Commit करें.
- Merge करें.
- Conflict Resolve करें.
- Final Commit करें.

---

# ✅ Verification Checklist

- Merge Conflict Successfully Create किया.
- Conflict Markers Identify किए.
- Conflict Successfully Resolve किया.
- Final Merge Commit किया.
- `git status` Verify किया.
- सभी Practice Tasks Successfully Complete किए.

---

# 🏆 Final Challenge

बिना Notes देखे

कम से कम 3 अलग-अलग Files में Merge Conflict Create करें.

सभी Conflicts Manually Resolve करें.

Merge Complete करें.

Final Repository Verify करें.

पूरा Workflow बिना किसी Error के Complete करें.

---

# 📚 आपने क्या सीखा?

- Merge Conflict क्या होता है.
- Conflict क्यों आता है.
- Conflict Markers समझना.
- Conflict Resolve करना.
- Merge Complete करना.
- Enterprise Merge Conflict Workflow Follow करना.