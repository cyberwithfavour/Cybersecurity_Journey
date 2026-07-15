# Reflection – Day 48

Today's lesson helped me understand why Windows Event Logs are one of the most valuable sources of information during a security investigation.

Before today, I had heard people talk about Event IDs like **4624** and **4625**, but I didn't really understand what they meant. Now I know that each Event ID represents a specific activity, such as a successful login, a failed login, or the creation of a new user account.

One thing that stood out to me is that SOC analysts don't randomly search through thousands of logs. Instead, they know which Event IDs to look for depending on the type of investigation they're conducting. This makes investigations faster and more effective.

I also learned that Windows Event Viewer is an essential tool for viewing and analyzing logs, while SIEM platforms collect these logs from multiple systems and present them in one place for easier monitoring.

This lesson showed me that logs are more than just records—they are evidence. Every login, account change, or privilege assignment leaves a trail that can help investigators understand what happened during a security incident.

As I continue learning, I want to become more confident reading Windows Event Logs and identifying suspicious activities using common Event IDs.
