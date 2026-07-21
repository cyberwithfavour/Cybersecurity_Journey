# Day 56 – Reflection

## What I Learned

Today's lesson taught me that investigating a phishing email is much more than simply deciding whether it looks suspicious. A SOC analyst follows a structured process to collect evidence, verify the sender, inspect email headers, analyze links and attachments, and determine the overall risk.

One thing that stood out to me was the importance of **email headers**. Before today, I thought they were just technical details, but I now understand that they can reveal where an email originated, how it traveled across mail servers, and whether it passed important authentication checks like SPF, DKIM, and DMARC.

I also learned that a phishing investigation should never rely on a single indicator. A legitimate email may fail one authentication check due to configuration issues, while a malicious email may successfully pass authentication if an attacker compromises a trusted account. This means analysts must evaluate all available evidence before making a conclusion.

---

## Key Takeaway

Effective phishing investigations require both technical analysis and critical thinking. Rather than trusting appearances, SOC analysts verify every part of an email before determining whether it is safe or malicious.

---

## Personal Reflection

This lesson made me appreciate how much attention to detail is required in a SOC.

A small clue, such as a mismatched domain name or an unusual email header, could be the difference between stopping an attack and allowing an organization to be compromised. As I continue my journey toward becoming a SOC analyst, I want to develop the habit of analyzing evidence carefully instead of making assumptions.
