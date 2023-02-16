# Vuln assessment + Pen Test

### Vulnerabilty assessment

Vulnerabilty assessments only identify possible security problem, not try to exploit them
Only scans as many hosts

### Penetration Tests
attemps to actively exploit found vulnerabilites as well as post-exploitation tasks

### Advanced Persitent Threats
APT differ from contracted penetrations tests
security is relaxed during pen test
pen testers are loud and don't care
APT's need to be quite, evade IDS/IPS and can remain in systems undetected for long periods of time

## Questions
1. Would vulnerability assessments prepare us to detect a real attacker on our networks? (Yay/Nay)
	- ***Nay***
2. During a penetration test, are you concerned about being detected by the client? (Yay/Nay)
	- ***Nay*
3. Highly organised groups of skilled attackers are nowadays referred to as ...
	- ***Advanced Persistent threats***

# Red Team Engagements

Red team engagements have shifted to focus on the abilities of a companies ability to defend and see what they would do 
Red teamers emulate real world threat actors **Tactics, Techniques and Procedures(TTP)** 
Every engagment will have clearly defined goal. e.g. Steal sensitive data
usually the blue team won't know about any of it
Red teams will do all they can to evade and remain undetected until the goal has been reached, no need to target every host. 

Red Team engagements will also consider different attack surfaces
- Technical infrastructutre - hacking
- Social Engineering - people hacking
- Physical - Lockpick etc

Red team excercises can also be run in various ways
- Full engagement - Simulate real world
- Assumed breach - red teamers already start with access to interal system
- Table top - conversation about theoreticals and what each team would do

## Questions
1. The goals of a red team engagement will often be referred to as flags or... 
	- ***Crown jewels**
2. During a red team engagement, common methods used by attackers are emulated against the target. Such methods are usually called TTPs. What does TTP stand for?
	- ***Tactics, Techniques and Procedures*
3. The main objective of a red team engagement is to detect as many vulnerabilities in as many hosts as possible (Yay/Nay)
	- ***Nay*

# Teams and Functions of an Engagement

There are 3 cells/teams
Red - Offensive 
Blue - Defensive - includes internal stuff and org's management
White - Acts as a referee between red and blue

## Questions
1. What cell is responsible for the offensive operations of an engagement?
	- ***Red Cell*
2. What cell is the trusted agent considered part of?
	- ***White Cell*

# Engagement Structure

Red teams use various kill chains to simulate real world 
Some kill chains are: 
    Lockheed Martin Cyber Kill Chain
    Unified Kill Chain
    Varonis Cyber Kill Chain
    Active Directory Attack Cycle
    MITRE ATT&CK Framework

Lockheed Kill Chain
| Technique            | Purpose                                                                           | Examples                                         |
| -------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------ |
| Reconnaissance       | Obtain information on the target                                                  | Harvesting emails, OSINT                         
| Weaponization        | Combine the objective with an exploit. Commonly results in a deliverable payload. | Exploit with backdoor, malicious office document 
| Delivery             | How will the weaponized function be delivered to the target                       | Email, web, USB                                  
| Exploitation         | Exploit the target's system to execute code                                       | MS17-010, Zero-Logon, etc.                       
| Installation         | Install malware or other tooling                                                  | Mimikatz, Rubeus, etc.                           
| Command and Control  | Control the compromised asset from a remote central controller                    | Empire, Cobalt Strike, etc.                      
| Action on Objectives | Any end objectives: ransomware, data exfiltration, etc.                           | Conti, LockBit2.0, etc.                          

## Questions
1.  If an adversary deployed Mimikatz on a target machine, where would they be placed in the Lockheed Martin cyber kill chain? 
	- ***Installation*
2.  What technique's purpose is to exploit the target's system to execute code? 
	- ***Exploitation*