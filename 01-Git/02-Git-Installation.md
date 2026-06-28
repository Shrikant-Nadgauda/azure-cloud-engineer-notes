# Git Installation

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Git क्या है?
- Git को Install कैसे करें?
- Windows, Linux और macOS में Installation
- Installation Verify कैसे करें?
- Git Update कैसे करें?
- Real Industry Example

---

# Git क्या है?

Git एक Distributed Version Control System (DVCS) है।

इसे Linus Torvalds ने Linux Kernel Development के लिए बनाया था।

आज लगभग हर Software Company Git का उपयोग करती है।

---

# Git Install करने की आवश्यकता क्यों है?

Git Install करने के बाद हम:

✔ Repository बना सकते हैं

✔ Version History रख सकते हैं

✔ GitHub से Code Download कर सकते हैं

✔ अपना Code GitHub पर Upload कर सकते हैं

✔ Team के साथ Collaboration कर सकते हैं

---

# Windows में Git Installation

1. Git की Official Website खोलें

https://git-scm.com

2. Windows Installer Download करें

3. Installer Run करें

4. Default Settings रखें

5. Install पर Click करें

6. Installation Complete होने के बाद Git Bash Open करें

---

# Linux Installation

Ubuntu / Debian

```bash
sudo apt update
sudo apt install git -y
```

RHEL / CentOS

```bash
sudo yum install git -y
```

Rocky Linux

```bash
sudo dnf install git -y
```

---

# macOS Installation

```bash
brew install git
```

या

```bash
xcode-select --install
```

---

# Installation Verify कैसे करें?

Command

```bash
git --version
```

Example Output

```bash
git version 2.50.1.windows.1
```

यदि Version दिखाई देता है,

तो Git Successfully Install हो चुका है।

---

# Git कहाँ Install होता है?

Windows

```
C:\Program Files\Git\
```

Git Bash भी इसी Installation के साथ आता है।

---

# Git Components

Git Install होने के बाद मुख्य Components

✔ Git Bash

✔ Git CMD

✔ Git Executables

✔ Git Configuration Files

---

# Git Upgrade कैसे करें?

Windows

नई Installer Download करके Install करें।

Linux

Ubuntu

```bash
sudo apt update
sudo apt upgrade git
```

---

# Git Uninstall

Windows

Settings

↓

Apps

↓

Git

↓

Uninstall

---

# Real Industry Example

एक नई Company में Join करने के बाद सबसे पहले Laptop में Install होने वाले Tools:

✔ Git

✔ VS Code

✔ Azure CLI

✔ Terraform

✔ Docker

✔ PowerShell

✔ kubectl

इनके बिना Cloud Engineer अपना Daily Work शुरू नहीं कर सकता।

---

# Verification

नीचे दिए गए Commands Run करें

```bash
git --version
```

```bash
where git
```

Git Bash में

```bash
which git
```

इन Commands से Confirm करें कि Git सही Install हुआ है।

---

# Best Practices

✔ हमेशा Official Website से Git Download करें।

✔ Latest Stable Version उपयोग करें।

✔ Installation के बाद Version Verify करें।

✔ Git Bash का उपयोग करना सीखें।

✔ Git Update करते रहें।

---

# Common Mistakes

❌ Third-party Website से Git Download करना

❌ Installation Verify नहीं करना

❌ पुरानी Version उपयोग करना

❌ PATH Variable खराब कर देना

---

# Engineer Tip

Git Install करना सबसे आसान Step है।

असल Skill Git Install करने में नहीं,

बल्कि Git को सही तरीके से उपयोग करने में है।

---

# Production Note

Enterprise Environment में Git अक्सर

Software Center,

Intune,

SCCM,

या Automation Scripts द्वारा Install किया जाता है।

Engineer को Manual Installation की आवश्यकता भी नहीं पड़ती।

---

# Interview Questions

Q1. Git किसने बनाया?

Q2. Git और GitHub में क्या अंतर है?

Q3. Git Install होने के बाद पहला Verification Command कौन सा है?

Q4. Git Bash और Command Prompt में क्या अंतर है?

Q5. Git Install होने के बाद कौन-कौन से Components उपलब्ध होते हैं?

---

# Summary

इस Chapter में हमने सीखा:

✔ Git क्या है

✔ Git Installation

✔ Windows Installation

✔ Linux Installation

✔ Verification

✔ Upgrade

✔ Best Practices

✔ Industry Use Case

अगले Chapter में हम Git Configuration सीखेंगे।