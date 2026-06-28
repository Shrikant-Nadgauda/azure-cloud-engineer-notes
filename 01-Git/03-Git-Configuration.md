# Git Configuration

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Git Configuration क्या है?
- Configuration की आवश्यकता क्यों होती है?
- Local और Global Configuration
- Username और Email Configure करना
- Configuration Verify करना
- Configuration Edit और Remove करना
- Real Industry Example

---

# Git Configuration क्या है?

Git Configuration वह प्रक्रिया है जिसमें हम Git को अपनी पहचान (Identity) बताते हैं।

जब भी हम Commit करते हैं, Git उस Commit के साथ हमारा Name और Email जोड़ता है।

सरल भाषा में:

> Git Configuration = Git को अपनी पहचान बताना।

---

# Git Configuration की आवश्यकता क्यों है?

मान लो 10 Engineers एक ही Repository पर काम कर रहे हैं।

अगर Git को यह पता ही न हो कि Commit किसने किया है,

तो History का कोई मतलब नहीं रहेगा।

इसीलिए Git हर Commit के साथ Author की जानकारी Save करता है।

---

# Git Configuration में क्या-क्या Store होता है?

✔ User Name

✔ Email Address

✔ Default Branch

✔ Editor

✔ Merge Behavior

✔ Line Ending Settings

✔ Alias

---

# Git Configuration के प्रकार

## 1. System Configuration

पूरे Computer के सभी Users पर लागू होती है।

---

## 2. Global Configuration

एक User के सभी Repositories पर लागू होती है।

---

## 3. Local Configuration

केवल Current Repository पर लागू होती है।

Local Configuration हमेशा Global Configuration से अधिक प्राथमिकता (Priority) रखती है।

---

# अगले Chapter में

हम सीखेंगे:

- `git config --global`
- `git config --local`
- `.gitconfig` File
- Practical Configuration
- Verification Commands
- Real Production Example

# Git Configuration क्या है?

Git Configuration वह प्रक्रिया है जिसमें हम Git को अपनी पहचान (Identity) बताते हैं।

जब भी हम Commit करते हैं, Git उस Commit के साथ हमारा Name और Email जोड़ता है।

सरल भाषा में:

> Git Configuration = Git को अपनी पहचान बताना।

---

# Git Configuration की आवश्यकता क्यों है?

मान लो एक Project पर 15 Engineers काम कर रहे हैं।

सभी रोज़ Commit कर रहे हैं।

अगर Git को यह पता ही न हो कि Commit किसने किया है, तो Project History बेकार हो जाएगी।

इसीलिए Git हर Commit के साथ Author की जानकारी भी Save करता है।

---

# Git Configuration में क्या-क्या Store होता है?

Git कई प्रकार की Settings Store कर सकता है।

जैसे:

✔ User Name

✔ Email Address

✔ Default Branch

✔ Default Editor

✔ Merge Behavior

✔ Line Ending Settings

✔ Git Alias

---

# Git Configuration के प्रकार

Git Configuration तीन Levels पर होती है।

## 1. System Configuration

पूरे Computer के सभी Users पर लागू होती है।

कम उपयोग होती है।

---

## 2. Global Configuration

पूरे User Account पर लागू होती है।

अगर तुम 20 Repository बनाओगे,

तो सभी में यही Configuration उपयोग होगी।

यही सबसे अधिक उपयोग होती है।

---

## 3. Local Configuration

केवल Current Repository पर लागू होती है।

अगर Local और Global दोनों मौजूद हों,

तो Local Configuration पहले लागू होगी।

Priority

Local

↓

Global

↓

System

---

# Git Configuration Commands

Username Set करना

```bash
git config --global user.name "Shrikant Nadgauda"
```

Email Set करना

```bash
git config --global user.email "shrikantpnadgauda@gmail.com"
```

---

# Configuration Verify करना

सभी Configuration देखने के लिए

```bash
git config --list
```

केवल Username

```bash
git config user.name
```

केवल Email

```bash
git config user.email
```

Global Configuration

```bash
git config --global --list
```

Local Configuration

```bash
git config --local --list
```

---

# Git Configuration कहाँ Store होती है?

Windows में Global Configuration

```
C:\Users\<Username>\.gitconfig
```

Linux

```
~/.gitconfig
```

Repository की Local Configuration

```
.git/config
```

---

# Configuration Edit करना

```bash
git config --global --edit
```

---

# Configuration Remove करना

Username Remove

```bash
git config --global --unset user.name
```

Email Remove

```bash
git config --global --unset user.email
```

---

# Real Industry Example

मान लो Company में 50 Developers काम कर रहे हैं।

अगर किसी Developer का Email गलत Configure हो जाए,

तो GitHub उस Commit को उसके Account से Link नहीं कर पाएगा।

इससे Contribution Graph भी गलत हो सकता है।

इसीलिए Project शुरू करने से पहले Git Configuration Verify करना जरूरी होता है।

---

# Practical

अपनी Machine पर ये Commands Run करें।

```bash
git config --global user.name
```

```bash
git config --global user.email
```

```bash
git config --list
```

```bash
git config --global --list
```

---

# Verification

यदि Output में आपका Name और Email दिखाई देता है,

तो Git Configuration सही है।

उदाहरण

```text
user.name=Shrikant Nadgauda
user.email=shrikantpnadgauda@gmail.com
```

---

# Best Practices

✔ हमेशा अपना Official Email उपयोग करें।

✔ GitHub Account वाला Email Configure करें।

✔ Project शुरू करने से पहले Configuration Verify करें।

✔ Personal और Office Repository के लिए Local Configuration का उपयोग करें।

✔ समय-समय पर Configuration Check करते रहें।

---

# Common Mistakes

❌ गलत Email Configure करना।

❌ Username खाली छोड़ देना।

❌ Office Project में Personal Email उपयोग करना।

❌ Local और Global Configuration का अंतर न समझना।

---

# 💡 Engineer Tip

एक Engineer को सबसे पहले Git Configuration Verify करनी चाहिए।

कई बार Push Fail नहीं होता,

लेकिन GitHub Contribution दिखाई नहीं देती,

क्योंकि Email गलत Configure होती है।

---

# 🏭 Production Note

बड़ी Companies में अक्सर Developers के Laptop पहले से Configure होते हैं।

लेकिन नया Project Join करने के बाद पहला Verification Command हमेशा यही होता है:

```bash
git config --list
```

---

# Interview Questions

Q1. Git Configuration क्या है?

Q2. Global और Local Configuration में क्या अंतर है?

Q3. Git अपना Username कहाँ Store करता है?

Q4. Git Configuration Verify करने का Command क्या है?

Q5. Local Configuration की Priority Global से अधिक क्यों होती है?

---

# 📝 Summary

इस Chapter में हमने सीखा:

✔ Git Configuration

✔ Global Configuration

✔ Local Configuration

✔ Username और Email Configure करना

✔ Verification

✔ Best Practices

✔ Production Example

अगले Chapter में हम Git Repository सीखेंगे।

---

# 🔗 Related Topics

⬅ Previous: Git Installation

➡ Next: Git Repository

## 🧠 Quick Revision

Git Configuration = Git की Identity

Global = सभी Repositories

Local = केवल Current Repository

Priority:

Local → Global → System