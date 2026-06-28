# Version Control

## 🎯 उद्देश्य

इस Chapter में हम सीखेंगे:

- Version Control क्या होता है?
- इसकी जरूरत क्यों पड़ती है?
- Manual Versioning की Problems
- Git क्यों बनाया गया?
- Version Control के प्रकार
- Real Industry Example

---

# Version Control क्या है?

Version Control एक ऐसा System है जो किसी भी Project में हुए सभी Changes का पूरा इतिहास (History) सुरक्षित रखता है।

अगर भविष्य में कोई गलती हो जाए, तो हम किसी भी पुराने Version पर वापस जा सकते हैं।

सरल भाषा में:

> Version Control = Project की Time Machine

---

# बिना Version Control के क्या Problem होती है?

मान लो तुमने एक Terraform Project बनाया।

आज File का नाम है

main.tf

कल थोड़ा Change किया

main-final.tf

फिर Client ने Change मांगा

main-final-v2.tf

फिर

main-final-v2-latest.tf

फिर

main-working.tf

कुछ दिनों बाद...

तुम्हें खुद नहीं पता होगा कि सही File कौन सी है।

यही सबसे बड़ी Problem है।

---

# Version Control यह Problem कैसे Solve करता है?

Version Control हर Change का Record रखता है।

उदाहरण

Version 1
↓
Version 2
↓
Version 3
↓
Version 4

अगर Version 4 खराब हो जाए

तो

Version 3

या

Version 2

पर तुरंत वापस जा सकते हैं।

---

# Version Control क्या-क्या Store करता है?

✔ किसने Change किया

✔ कब किया

✔ क्या Change किया

✔ क्यों किया

✔ पुराने Version

---

# Version Control के प्रकार

## 1. Local Version Control

History केवल Local Machine पर रहती है।

Example

RCS

---

## 2. Centralized Version Control

एक Central Server होता है।

सभी उसी Server से Connect होते हैं।

Examples

SVN

CVS

---

## 3. Distributed Version Control

हर Developer के पास Project की पूरी Copy होती है।

Internet न होने पर भी काम कर सकते हैं।

Examples

Git

Mercurial

यही आज सबसे ज्यादा उपयोग होता है।

---

# Git क्यों Popular हुआ?

✔ Fast

✔ Secure

✔ Offline Work

✔ Branching आसान

✔ Merge आसान

✔ Open Source

✔ Industry Standard

---

# Real Industry Example

मान लो

5 Engineers

एक ही Azure Infrastructure पर काम कर रहे हैं।

Engineer-1

Virtual Machine बना रहा है।

Engineer-2

VNet बना रहा है।

Engineer-3

NSG बना रहा है।

Engineer-4

Terraform Modules बना रहा है।

Engineer-5

Azure DevOps Pipeline बना रहा है।

अगर Version Control नहीं होगा

तो सभी एक-दूसरे का Code Overwrite कर देंगे।

Git इस Problem को पूरी तरह Solve करता है।

---

# Verification

अब तक आपको यह समझ आ जाना चाहिए:

✔ Version Control क्या है

✔ इसकी जरूरत क्यों पड़ती है

✔ Git क्यों बनाया गया

✔ Git Industry Standard क्यों है

---

# Best Practices

✔ Meaningful Commit करें

✔ रोज़ Code Commit करें

✔ Main Branch पर Direct काम न करें

✔ हमेशा Branch बनाकर काम करें

✔ Repository को Organized रखें

---

# Common Mistakes

❌ File के अलग-अलग नाम बनाना

Project-final

Project-final-new

Project-final-latest

Project-final-final

❌ Backup Folder बनाना

Backup

Backup-New

Backup-Latest

Git होने के बाद इसकी जरूरत नहीं रहती।

---

# Interview Questions

Q1. Version Control क्या है?

Q2. Git क्यों उपयोग किया जाता है?

Q3. Git और GitHub में क्या अंतर है?

Q4. Centralized और Distributed Version Control में क्या अंतर है?

---

# Summary

इस Chapter में हमने सीखा:

✔ Version Control

✔ इसकी आवश्यकता

✔ Version Types

✔ Git की जरूरत

✔ Real Industry Use Case

अगले Chapter में हम Git Installation सीखेंगे।