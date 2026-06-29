# Git Security Best Practices

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे

- Git Repository को Secure कैसे रखें?
- Common Security Mistakes
- Enterprise Security Standards

---

# 1. Never Commit Secrets

Repository में कभी भी

❌ Password

❌ API Keys

❌ Access Tokens

❌ SSH Private Keys

❌ Certificates

Commit न करें।

---

# Examples

❌

```
password=Admin123

api_key=xxxxxxxx

client_secret=xxxxxxxx
```

✔

Secrets हमेशा

```
.env

Azure Key Vault

GitHub Secrets

Azure DevOps Library
```

में रखें।

---

# 2. Use .gitignore

Sensitive Files को हमेशा Ignore करें।

```
.env

*.pem

*.key

*.pfx

terraform.tfvars

*.tfstate
```

---

# 3. Use SSH Authentication

HTTPS की जगह

SSH Authentication उपयोग करें।

✔ More Secure

✔ Password-less

✔ Enterprise Standard

---

# 4. Enable Multi-Factor Authentication (MFA)

GitHub Account पर

हमेशा MFA Enable रखें।

Password Leak होने पर भी

Account सुरक्षित रहेगा।

---

# 5. Use Personal Access Token (PAT)

Password की जगह

Personal Access Token उपयोग करें।

---

# 6. Protect Main Branch

Main Branch पर

Direct Push Disable रखें।

Merge केवल

Pull Request से होना चाहिए।

---

# 7. Review Every Pull Request

हर Pull Request

Merge करने से पहले

Review करें।

---

# 8. Keep Repository Private

अगर Project Public नहीं है

तो Repository Private रखें।

---

# 9. Remove Sensitive Data Immediately

अगर गलती से Secret Commit हो जाए

तो

✔ Secret Rotate करें

✔ History Clean करें

✔ नया Secret Generate करें

---

# 10. Keep Dependencies Updated

पुरानी Libraries

Security Risk बन सकती हैं।

Dependencies नियमित रूप से Update करें।

---

# 11. Sign Your Commits

जहाँ संभव हो

Signed Commits उपयोग करें।

इससे Commit की Authenticity Verify होती है।

---

# 12. Follow Least Privilege

जिस User को जितनी Permission चाहिए

उतनी ही दें।

---

# Common Mistakes

❌ Push Passwords

❌ Commit SSH Private Keys

❌ Disable MFA

❌ Direct Push to Main

❌ Public Repository में Secrets

❌ Ignore Security Alerts

---

# Production Security Checklist

✅ MFA Enabled

✅ SSH Authentication

✅ Branch Protection

✅ Pull Request Review

✅ .gitignore Configured

✅ Secrets in Key Vault

✅ Repository Access Reviewed

---

# Summary

Git Security का उद्देश्य केवल Repository को सुरक्षित रखना नहीं है,

बल्कि

Source Code,

Credentials,

Infrastructure,

और पूरी Development Process को सुरक्षित रखना है।

छोटी Security Mistake

Production Environment पर बड़ा प्रभाव डाल सकती है।

---

# 🔥 सबसे Valuable Section 

- Golden Security Rules

✔ Never Commit Passwords

✔ Never Commit API Keys

✔ Never Commit SSH Private Keys

✔ Enable MFA

✔ Use SSH Instead of HTTPS

✔ Protect Main Branch

✔ Review Every Pull Request

✔ Store Secrets in Key Vault / GitHub Secrets

✔ Keep Repository Private When Required

✔ Rotate Secrets Regularly

---

# 🌍 Real Production Example

Developer

↓

Writes Code

↓

Uses .env File

↓

Git Ignore Protects Secret

↓

Push to GitHub

↓

GitHub Actions Uses Secret

↓

Azure Key Vault Provides Credentials

↓

Application Deploys Securely

----