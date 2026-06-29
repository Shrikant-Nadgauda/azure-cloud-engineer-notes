# Lab 09 - SSH Authentication

## 🎯 Objective

इस Lab में आप SSH Key Generate करना, GitHub में SSH Public Key Add करना, Connection Verify करना और Password के बिना Secure Authentication करना सीखेंगे।

---

# 📋 Prerequisites

- Git Installed होना चाहिए.
- GitHub Account उपलब्ध होना चाहिए.
- GitHub Remote Repository पहले से Configure होनी चाहिए.

---

# 🌍 Real World Scenario

Hello Team,

हमारा **Audix Azure Cloud Project** अब GitHub पर Successfully Publish हो चुका है.

लेकिन Company की Security Policy के अनुसार **Username और Password Authentication** की अनुमति नहीं है.

अब सभी Developers को **SSH Authentication** का उपयोग करना होगा ताकि Git Operations सुरक्षित, तेज़ और Password-Free हो सकें.

आज मैं आपको एक Example दिखाऊँगा, उसके बाद आपको अपनी स्वयं की SSH Key Generate करके GitHub के साथ Configure करनी है.

---

# ⚠️ SSH Configure करने से पहले ध्यान रखें

- GitHub Account Ready होना चाहिए.
- सही Email Address का उपयोग करें.
- Public Key और Private Key को कभी Mix न करें.
- Private Key किसी के साथ Share न करें.
- GitHub में केवल Public Key Add करें.
- Connection Test करना न भूलें.

---

# 📝 Task 1 - Existing SSH Keys Check करें

System में पहले से SSH Keys हैं या नहीं Verify करें.

### Example

```bash
ls ~/.ssh
```

---

# 📝 Task 2 - नई SSH Key Generate करें

अपनी GitHub Email के साथ नई SSH Key Generate करें.

### Example

```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
```

---

# 📝 Task 3 - SSH Agent Start करें

SSH Agent Start करें.

### Example

```bash
eval "$(ssh-agent -s)"
```

---

# 📝 Task 4 - Private Key Add करें

Generate की गई Private Key को SSH Agent में Add करें.

### Example

```bash
ssh-add ~/.ssh/id_ed25519
```

---

# 📝 Task 5 - Public Key Copy करें

Public Key Open करें और उसकी पूरी Content Copy करें.

### Example

```bash
cat ~/.ssh/id_ed25519.pub
```

---

# 📝 Task 6 - GitHub में SSH Key Add करें

GitHub Account में जाएँ.

```
Settings

↓

SSH and GPG Keys

↓

New SSH Key
```

Copy की हुई Public Key Paste करें और Save करें.

---

# 📝 Task 7 - SSH Connection Verify करें

GitHub के साथ Connection Test करें.

### Example

```bash
ssh -T git@github.com
```

Expected Output

```
Hi username!

You've successfully authenticated.
```

---

# 📝 Task 8 - Remote URL Update करें

HTTPS Remote को SSH Remote में Change करें.

### Example

```bash
git remote set-url origin git@github.com:username/Audix-Azure-Project.git
```

Verify करें.

```bash
git remote -v
```

---

# 📝 Task 9 - SSH Push Test करें

Repository में एक छोटा Change करें.

Commit करें.

SSH का उपयोग करके Push करें.

### Example

```bash
git push origin main
```

---

# 📝 Task 10 - Practice Assignment

नीचे दिए गए सभी Tasks स्वयं Complete करें.

- SSH Key Generate करें.
- SSH Agent Start करें.
- Key Add करें.
- GitHub में Public Key Add करें.
- Connection Verify करें.
- Remote URL को SSH में Change करें.
- Test Push करें.

---

# ✅ Verification Checklist

- SSH Key Successfully Generate हुई.
- SSH Agent Successfully Start हुआ.
- Private Key Successfully Add हुई.
- Public Key GitHub में Add हुई.
- SSH Connection Successfully Verify हुआ.
- Remote URL SSH में Update हुआ.
- SSH से Push Successfully Complete हुआ.

---

# 🏆 Final Challenge

बिना Notes देखे

- नई SSH Key Generate करें.
- GitHub में Add करें.
- Connection Verify करें.
- Remote URL Update करें.
- SSH का उपयोग करके Repository Push करें.

पूरा Process बिना किसी Error के Complete करें.

---

# 📚 आपने क्या सीखा?

- SSH Key Generate करना.
- SSH Agent का उपयोग करना.
- GitHub में Public Key Add करना.
- SSH Authentication Verify करना.
- HTTPS से SSH पर Switch करना.
- Secure Git Authentication Follow करना.