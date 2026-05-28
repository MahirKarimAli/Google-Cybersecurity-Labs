
# Incident Response & Architecture Analysis: 


# Volumetric ICMP Flood 

Prepared by **<span style="text-decoration:underline;">Mahir Karim Ali</span>**


<table>
  <tr>
   <td><strong>Summary</strong>
   </td>
   <td>The organization experienced a Denial of Service (DoS) attack through a volumetric ICMP ping flood. The root cause behind this attack was perimeter defense misconfiguration, specifically an unconfigured firewall that lacked ingress filtering that could have identified  and dropped spoof IP addresses. This vulnerability caused resource exhaustion, which caused complete network accessibility outage for internal systems that lasted 2 hours. For the containment of the threat, the Incident response team immediately blocked all incoming ICMP traffic and took non-critical systems offline. The long term plan includes, implementation of rate limiting on incoming ICMP packets, Source IP verification, advanced network monitoring and an active IDS/IPS deployment.
   </td>
  </tr>
  <tr>
   <td><strong>Identify</strong>
   </td>
   <td>
<ul>

<li><strong>What Happened (The Attack):</strong> The company was attacked with a Denial of Service (DoS) attack. The attacker tried to crash the system by sending a volumetric flood of fake "ping" messages. To get through basic security checks, the attacker spoofed their IP addresses.</li>

<li><strong>What Was Affected (The Damage):</strong> TheFirewall was not properly configured with ingress filtering that could have blocked this bad traffic. This massive wave of fake ICMP packets poured inside and completely exhausted the network's routers. As a result, the entire system crashed, and employees couldn't access the internet, their files, or the tools they needed to do their jobs.</li>
</ul>
   </td>
  </tr>
  <tr>
   <td><strong>Protect</strong>
   </td>
   <td>To further secure the organization’s assets and mitigate the risk of future DoS events , the following system configurations and procedures must be implemented immediately:
<ul>

<li>Reconfigure the perimeter firewall to enforce strict ingress filtering to automatically identify and drop incoming packets with spoofed IP addresses.</li>

<li>Implement ICMP rate-limiting rules on the perimeter defenses to restrict the volume of acceptable ping requests, preventing resource exhaustion from volumetric floods.</li>

<li>Deploy an Intrusion Prevention System (IPS) inline with the network traffic to dynamically detect and filter out malicious traffic based on behavioral signatures and suspicious characteristics.</li>

<li>Establish a formal change-management policy and routine audit schedule for all perimeter devices (routers/firewalls) to ensure no hardware is ever deployed to the production environment in an "unconfigured" or default state.</li>
</ul>
   </td>
  </tr>
  <tr>
   <td><strong>Detect</strong>
   </td>
   <td>To spot future attacks early, the team will set up monitoring tools that act as alarms for our network, applications, and user accounts.
<ul>

<li><strong>Monitoring Network Traffic:</strong> We will deploy a SIEM (Security Information and Event Management) system. This tool acts as a central hub that collects logs from our firewall. We will configure the SIEM to trigger an alert if it sees a sudden spike in traffic, such as an abnormal amount of pings from outside IP addresses.</li>

<li><strong>Monitoring Applications:</strong> We will track how much computer power our software normally uses on a regular day (defining a baseline) . If an application suddenly starts overworking or crashing, the system will flag it as a highly unusual behavior. This gives us early warning that a DoS attack might be starting.</li>

<li><strong>Monitoring User Accounts:</strong> We will track user logins to watch for Indicators of Compromise (IoCs), which are specific clues that a hacker is trying to break in. For example, the system will automatically alert us if an account has too many failed login attempts in a row, or if someone tries to log in from an unusual location.</li>
</ul>
   </td>
  </tr>
  <tr>
   <td><strong>Respond</strong>
   </td>
   <td>If another cybersecurity incident occurs, the team will follow this step-by-step plan to stop the attack and get the network back to normal:
<ul>

<li><strong>Contain the Attack:</strong> We will immediately disconnect the affected computers and block off the compromised parts of the network so the attack cannot spread to other areas. For a flood of fake pings, we will set our main router to automatically drop the bad traffic before it gets inside.</li>

<li><strong>Stop the Threat:</strong> We will use security tools (like the IPS) to actively block the attacker's IP addresses and limit the number of connection requests allowed. This will completely cut off the attacker's access to our network.</li>

<li><strong>Analyze the Data:</strong> Once the attack is stopped, we will review the data to figure out exactly how they got in. We will examine the firewall logs, the alerts from our security systems, and the recorded network traffic to find the root cause of the problem.</li>

<li><strong>Improve for the Future:</strong> Shortly after the incident is resolved, the team will hold a "lessons learned" meeting. We will use the information we gathered to update our security rules and step-by-step response plans, ensuring we can react even faster the next time.</li>
</ul>
   </td>
  </tr>
  <tr>
   <td><strong>Recover</strong>
   </td>
   <td>To fully recover from the incident and return to normal business operations safely, the organization will follow a structured restoration plan:
<ul>

<li><strong>Immediate Information Needed: </strong>The team must immediately know the priority level of all offline systems, identifying which network services are "critical" (like client web design databases and internal communication tools) versus "non-critical" (like background software updates). We also need confirmation from the firewall logs that the ICMP flood has completely stopped before bringing everything back online.</li>

<li><strong>Prioritized Restoration:</strong> We will slowly bring the critical systems back online first so the company can resume its main graphic design and marketing work. Once those are stable, we will restore the noncritical systems.</li>

<li><strong>System Health Checks:</strong> Before allowing employees to fully reconnect, the IT team will test the internal network services to ensure they are functioning properly and did not suffer any data corruption during the crash.</li>

<li><strong>Communication:</strong> Management will notify all employees that the network is safe to use again. If any client projects were delayed during the 2-hour outage, the company will proactively communicate the situation to those clients.</li>
</ul>
   </td>
  </tr>
</table>

