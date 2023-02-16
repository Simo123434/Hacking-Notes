# Task 2
1. In a Windows domain, credentials are stored in a centralised repository called...
	Answer: **Active Directory**
2. The server in charge of running the Active Directory services is called...
	Answer: **Domain Controller**

# Task 3
Many object types e.g User, machines etc.
Users have 2 types - people, services (msqlsvc)
The machine account name is the computer's name followed by a dollar sign. For example, a machine named `DC01` will have a machine account called `DC01$`
Security groups:
- Domain Admins - Admin over entire domain
- Server operators - adminsiter domain controllers
- backup operators - allowed to access any file - used to perform data backups
- Account operators - create and modify other account on domain
- Domain user - duh
- domain computers - duh
- domain controllers - Includes all existing DCs on the domain.

# Task 4
AD User Management
remove unnecscary groups and users
delegate control it it admin
change sophie password
1. What was the flag found on Sophie's desktop?
	Answer : What was the flag found on Sophie's desktop?
2. The process of granting privileges to a user over some OU or other AD Object is called...
	Answer: Delegation

# Task 5
Computers
create workstation and server OU
move correctly 
1. After organising the available computers, how many ended up in the Workstations OU?
	Answer: 7
2. Is it recommendable to create separate OUs for Servers and Workstations? (yay/nay)
	Answer: yay

# Task 6
GPO creation etc
1. What is the name of the network share used to distribute GPOs to domain machines?
	Answer: SYSVOL
2. Can a GPO be used to apply settings to users and computers? (yay/nay)
	Answer: yay

# Task 7
authentication
netNTLM
kerberos
1. Will a current version of Windows use NetNTLM as the preferred authentication protocol by default? (yay/nay)
	Answer: nay
2. When referring to Kerberos, what type of ticket allows us to request further tickets known as TGS?
	Answer: Ticket granting ticket
3. When using NetNTLM, is a user's password transmitted over the network at any point? (yay/nay)
	Answer: nay

# Task 8
1. What is a group of Windows domains that share the same namespace called?
	Answer: tree
2.  What should be configured between two domains for a user in Domain A to access a resource in Domain B?
	Answer: a trust relationship