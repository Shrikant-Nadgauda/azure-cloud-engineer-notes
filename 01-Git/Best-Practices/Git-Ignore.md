# Git Ignore Best Practices

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे

- .gitignore क्या है?
- इसका उपयोग क्यों किया जाता है?
- किन Files को Git में Track नहीं करना चाहिए?
- Azure, Terraform, Python, Docker आदि के लिए Common Examples

---

# .gitignore क्या है?

`.gitignore` एक Configuration File है

जो Git को बताती है

कि किन Files और Folders को Track नहीं करना है।

---

# क्यों जरूरी है?

हर File Repository में Store नहीं करनी चाहिए।

कुछ Files

- Temporary होती हैं
- Automatically Generate होती हैं
- Sensitive Information रखती हैं

ऐसी Files को `.gitignore` में Add किया जाता है।

---

# Basic Examples

Ignore एक File

```
secret.txt
```

Ignore सभी Log Files

```
*.log
```

Ignore सभी ZIP Files

```
*.zip
```

Ignore पूरा Folder

```
temp/
```

---

# Common Files to Ignore

```
*.log
*.tmp
*.bak
*.cache
```

---

# Environment Files

```
.env
.env.local
.env.production
```

इनमें अक्सर Passwords और API Keys होती हैं।

---

# Terraform

```
.terraform/
*.tfstate
*.tfstate.*
crash.log
terraform.tfvars
```

---

# Python

```
__pycache__/
*.pyc
.venv/
venv/
```

---

# Node.js

```
node_modules/
npm-debug.log
```

---

# Docker

```
*.tar
docker-compose.override.yml
```

---

# VS Code

```
.vscode/
```

---

# IntelliJ

```
.idea/
```

---

# Visual Studio

```
.vs/
bin/
obj/
```

---

# macOS

```
.DS_Store
```

---

# Linux

```
*~
```

---

# Windows

```
Thumbs.db
Desktop.ini
```

---

# Azure

```
local.settings.json

*.publishsettings
```

---

# Logs

```
logs/

*.log
```

---

# Backup Files

```
backup/

*.bak
```

---

# Certificates

```
*.pem

*.key

*.pfx

*.crt
```

Private Certificates Repository में Commit नहीं करनी चाहिए।

---

# SSH Keys

```
id_rsa

id_ed25519

*.ppk
```

---

# Good Example

```
.env
.terraform/
*.tfstate
*.log
.vscode/
node_modules/
```

---

# Bad Practice

❌ Password Files Commit करना

❌ API Keys Commit करना

❌ Terraform State Commit करना

❌ SSH Private Keys Commit करना

---

# Best Practices

✔ Sensitive Files Ignore करें

✔ Generated Files Ignore करें

✔ Large Files Ignore करें

✔ Team के लिए Common .gitignore रखें

✔ Project Start होते ही .gitignore बनाएँ

---

# Real Azure + Terraform Example

```
.terraform/
*.tfstate
terraform.tfvars
.env
.vscode/
*.log
```

---

# Summary

`.gitignore` Repository को

✔ Secure

✔ Clean

✔ Lightweight

रखने में मदद करती है।

हर Project की शुरुआत में `.gitignore` बनाना एक अच्छी आदत है।

---

# Production .gitignore

# Terraform

.terraform/

*.tfstate

*.tfstate.*

terraform.tfvars

crash.log

# Environment
.env
.env.*

# Logs
*.log
logs/

# VS Code
.vscode/

# Python
__pycache__/
*.pyc
.venv/

# Node
node_modules/

# Windows
Thumbs.db
Desktop.ini

# macOS
.DS_Store

# SSH
id_rsa
id_ed25519
*.pem
*.key
*.ppk

# Backup
*.bak
*.tmp

-----