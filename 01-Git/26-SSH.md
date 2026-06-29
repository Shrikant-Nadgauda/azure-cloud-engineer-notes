# 📘 Topic 26 - SSH 

# SSH (Secure Shell)

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- SSH क्या है?
- SSH क्यों उपयोग किया जाता है?
- SSH Key Pair क्या होती है?
- Public Key और Private Key में अंतर
- GitHub के साथ SSH कैसे Configure करें?
- SSH Authentication कैसे काम करता है?
- Production में SSH का उपयोग
- Best Practices

---

# SSH क्या है?

SSH (Secure Shell) एक Secure Network Protocol है

जिसका उपयोग

दो Computers के बीच

Encrypted Communication स्थापित करने के लिए किया जाता है।

SSH का सबसे बड़ा उपयोग

✔ Remote Login

✔ Secure File Transfer

✔ Git Authentication

में होता है।

---

# आसान उदाहरण

मान लो

तुम्हारा Laptop

↓

GitHub

के साथ Communication कर रहा है।

अगर Communication Secure नहीं होगा

तो कोई बीच में Data चुरा सकता है।

SSH

पूरे Communication को Encrypt कर देता है।

---

# Real Life Example

मान लो

तुम्हारे घर की एक Key है।

उस Key से केवल तुम ही दरवाज़ा खोल सकते हो।

SSH भी बिल्कुल ऐसा ही काम करता है।

GitHub तुम्हारी Public Key रखता है।

Private Key केवल तुम्हारे Laptop में रहती है।

जब तुम GitHub से Connect करते हो,

GitHub Verify करता है

कि तुम्हारे पास सही Private Key है या नहीं।

अगर Verification सफल हुआ

तो Access मिल जाता है।

---

# SSH Key Pair क्या होती है?

SSH हमेशा दो Keys बनाता है।

```
Public Key

↓

Private Key
```

दोनों एक-दूसरे से जुड़े होते हैं।

लेकिन

Public Key से Private Key नहीं बनाई जा सकती।

---

# Public Key

Public Key

GitHub

Server

या Remote Machine

को दी जाती है।

इसे Share करना सुरक्षित है।

Example

```
id_ed25519.pub
```

---

# Private Key

Private Key

केवल तुम्हारे Computer में रहती है।

इसे कभी भी

Share नहीं करना चाहिए।

Example

```
id_ed25519
```

---

# Golden Rule

Public Key

सबको दे सकते हो।

Private Key

कभी किसी को मत देना।

---

# SSH Authentication कैसे काम करता है?

```
Laptop

↓

Private Key

↓

Internet

↓

GitHub

↓

Public Key Verification

↓

Authentication Success
```

---

# SSH Key Generate करना

```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
```

अगर पुराना System हो

```bash
ssh-keygen -t rsa -b 4096
```

---

# Generated Files

Linux / Git Bash

```
~/.ssh
```

Windows

```
C:\Users\<User>\.ssh
```

Files

```
id_ed25519

id_ed25519.pub
```

---

# Public Key देखना

```bash
cat ~/.ssh/id_ed25519.pub
```

Windows PowerShell

```powershell
Get-Content ~/.ssh/id_ed25519.pub
```

---

# GitHub में Public Key Add करना

GitHub

↓

Settings

↓

SSH and GPG Keys

↓

New SSH Key

↓

Paste Public Key

↓

Save

---

# Connection Test

```bash
ssh -T git@github.com
```

Output

```
Hi username!

You've successfully authenticated.
```

---

# Remote URL बदलना

HTTPS

```
https://github.com/user/repo.git
```

SSH

```
git@github.com:user/repo.git
```

Change करने के लिए

```bash
git remote set-url origin git@github.com:user/repo.git
```

---

# Remote Verify

```bash
git remote -v
```

Output

```
origin

git@github.com:user/repo.git
```

---

# Push

अब

```bash
git push
```

Password नहीं पूछेगा।

---

# SSH Agent

Private Key को Memory में Load करने के लिए

```bash
eval "$(ssh-agent -s)"
```

Key Add

```bash
ssh-add ~/.ssh/id_ed25519
```

---

# Real Production Example

Azure VM

↓

SSH

↓

Terraform Server

↓

GitHub

↓

Automatic Deployment

पूरी Automation SSH Keys के माध्यम से होती है।

कोई Password उपयोग नहीं होता।

---

# Common Mistakes

❌ Private Key GitHub पर Upload कर देना।

❌ Private Key Email करना।

❌ Wrong Remote URL उपयोग करना।

❌ SSH Test न करना।

---

# Best Practices

✔ ED25519 Keys उपयोग करें।

✔ Private Key सुरक्षित रखें।

✔ Strong Passphrase रखें।

✔ नियमित रूप से Keys Rotate करें।

✔ GitHub में केवल Public Key Add करें।

---

# 🏭 Production Note

Enterprise Companies में

GitHub

Azure DevOps

GitLab

Linux Servers

Cloud VMs

सब जगह SSH आधारित Authentication उपयोग किया जाता है।

Password आधारित Authentication लगभग समाप्त हो चुका है।

---

# Interview Questions

Q1. SSH क्या है?

Q2. Public Key और Private Key में अंतर क्या है?

Q3. SSH Authentication कैसे काम करता है?

Q4. SSH Key कैसे Generate करेंगे?

Q5. GitHub के साथ SSH क्यों उपयोग किया जाता है?

---

# 🧠 Quick Revision

```
ssh-keygen

↓

Public Key

↓

GitHub

↓

Private Key

↓

Laptop

↓

ssh -T

↓

git push
```

---

# 📝 Summary

इस Chapter में हमने सीखा

✔ SSH

✔ SSH Keys

✔ Public Key

✔ Private Key

✔ GitHub Authentication

✔ SSH Agent

✔ Production Workflow

अब Git Module पूरा हो चुका है।

अगला Module

➡ GitHub

---

# 🔗 Related Topics

⬅ Previous : Merge Conflict

➡ Next : GitHub Introduction

---

# 🔥 Real Production Scenario1 SSH in Enterprise

एक DevOps Pipeline Azure VM पर Deploy होती है।

Pipeline

↓

GitHub से Code Pull करती है।

↓

Terraform Execute करती है।

↓

Azure Resources Create करती है।

अगर यहाँ Password उपयोग किया जाए

तो Automation रुक जाएगी।

इसीलिए Production में SSH Keys उपयोग की जाती हैं।

Automation + Security + Password-less Authentication

यही SSH की सबसे बड़ी ताकत है।

----

# 💻 Practical Lab

- Step 1 - SSH Folder देखें

ls -la ~/.ssh

- Step 2 - नई SSH Key बनाएँ

ssh-keygen -t ed25519 -C "your-email@example.com"

Enter दबाएँ।

- Step 3 - Files Verify करें

ls ~/.ssh

Output

id_ed25519

id_ed25519.pub

- Step 4 - Public Key देखें

cat ~/.ssh/id_ed25519.pub

- Step 5 - SSH Agent Start करें

eval "$(ssh-agent -s)"
 - Step 6 - Private Key Add करें

ssh-add ~/.ssh/id_ed25519

- Step 7 - GitHub Connection Test करें

ssh -T git@github.com

Expected Output

Hi Shrikant-Nadgauda!

You've successfully authenticated, but GitHub does not provide shell access.

- Step 8 - Remote URL देखें
git remote -v

- Step 9 - HTTPS से SSH में बदलें

git remote set-url origin git@github.com:Shrikant-Nadgauda/azure-cloud-engineer-notes.git

- Step 10 - Verify करें

git remote -v

- अब Output कुछ ऐसा होना चाहिए:

origin  git@github.com:Shrikant-Nadgauda/azure-cloud-engineer-notes.git (fetch)
origin  git@github.com:Shrikant-Nadgauda/azure-cloud-engineer-notes.git (push)

----

# 💡 Senior Engineer Tips

1. Private Key कभी Share मत करना

❌ WhatsApp

❌ Email

❌ GitHub Repository

❌ Teams Chat

2. Public Key Share करना Safe है

इसे GitHub, Azure DevOps, GitLab या Linux Server पर Add किया जा सकता है।

3. ED25519 को प्राथमिकता दें
ssh-keygen -t ed25519

यह RSA की तुलना में Modern, Faster और अधिक Secure माना जाता है।

----

# 🧠 10 सेकंड का Interview Answer

अगर Interviewer पूछे:

"GitHub के साथ SSH क्यों उपयोग करते हैं?"

तो सीधे बोलना:

SSH एक Secure Authentication Mechanism है जो Public Key Cryptography का उपयोग करता है। GitHub में Public Key Store की जाती है और Private Key केवल Local System पर रहती है। इससे Password-less, Secure और Automated Authentication संभव होती है, इसलिए Enterprise Projects में HTTPS की तुलना में SSH अधिक उपयोग किया जाता है।

----