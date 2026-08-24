NAME: PRITHVI RAAJ KUMAR L

REG. NO: 192512275

Question 4 – Comparative Study of IDS and IPS
Introduction

An Intrusion Detection System (IDS) and an Intrusion Prevention System (IPS) are security technologies used to protect computer networks from cyberattacks. Both systems monitor network traffic and look for suspicious activities. The main difference is that IDS detects and reports an attack, whereas IPS can detect and block the attack.

1. Intrusion Detection System (IDS)

IDS is mainly used for monitoring and detecting suspicious activities in a network. It checks incoming and outgoing traffic and compares it with known attack patterns or unusual behavior.

When IDS finds something suspicious, it sends an alert to the administrator. The administrator can then examine the alert and take suitable action.

#Advantages of IDS

Helps detect unauthorized activities.
Provides alerts when an attack is suspected.
Helps administrators monitor network security.
Useful for analyzing security incidents.
Does not normally interfere with normal network traffic.

#Limitations of IDS

It mainly detects attacks rather than stopping them.
It may sometimes produce false alarms.
A security administrator is needed to investigate alerts.
An attack may reach the system before action is taken.

2. Intrusion Prevention System (IPS)

IPS is more active than IDS. It monitors network traffic and, when it identifies malicious activity, it can automatically block or drop the harmful traffic.

IPS is normally placed directly in the path of network traffic so that it can take action immediately when a threat is detected.

#Advantages of IPS

Can detect and block attacks automatically.
Provides protection against known threats in real time.
Reduces the chances of malicious traffic reaching the target.
Helps enforce network security rules.
Reduces the amount of manual action required.

#Limitations of IPS

Incorrect configuration can block legitimate traffic.
It requires regular updates and maintenance.
It may slightly affect network performance.
A wrong security rule can interrupt normal communication.

3. IDS vs IPS
   
I. Main Purpose

IDS: Detects threats.
IPS: Detects and prevents threats.

II. Action

IDS: Sends an alert to the administrator.
IPS: Blocks or drops harmful traffic.

III. Traffic Blocking

IDS: Does not block traffic.
IPS: Can block malicious traffic.

IV. Deployment

IDS: Usually deployed passively for monitoring.
IPS: Usually deployed inline with network traffic.

V. Administrator Action

IDS: Administrator usually needs to investigate and respond to alerts.
IPS: Can automatically take action against detected threats.

VI. Main Benefit

IDS: Provides monitoring and attack detection.
IPS: Provides real-time threat prevention.

4. Deployment Scenarios

IDS:
IDS is useful when an organization mainly wants to monitor its network and identify suspicious activities. It can be used for security monitoring, investigation, and collecting information about attacks.

IPS:
IPS is useful when an organization needs active protection. It can be placed at important points such as network gateways or near critical servers to stop harmful traffic before it reaches the protected system.

5. Conclusion

IDS and IPS are both important parts of network security. IDS is mainly used to identify and report attacks, while IPS goes one step further by detecting and blocking attacks. IDS is suitable when monitoring and analysis are the main requirements, whereas IPS is useful when immediate protection is needed. Using both together can provide better protection for an enterprise network.

