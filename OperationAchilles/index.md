---
layout: default
title: Operation Achilles
---

# Operation Achilles

<div style="text-align: center;">
  <img src="{{ 'OperationAchilles/site/achilles.png' | relative_url }}" alt="Achilles" style="max-width: 80%; height: auto;">    
  <p>Achillion Palace in Corfu, Greece</p>
</div>

<div class="scroll-box">
In Greek myth, Achilles was the greatest warrior of the Greek force at Troy,
but even he had a vulnerable point: his heel. That idea gives us the theme
for this operation. A network may look strong overall and still have one weak
point that matters more than everything else. In this mission, students act
either as defenders trying to protect the most important part of the network
or as attackers trying to identify and exploit that weak point.
</div>
<div class="terminal">
student162@admin162:~/missions/operation_achilles$ cat overview.txt

MISSION CONTEXT:
Operation Achilles is about identifying the weak point in a network and
deciding what matters most before a real attacker does.

In the story of Achilles, the greatest warrior still had a vulnerable point.
In cybersecurity, strong networks also have weak points:
- a poorly placed server
- exposed wireless access
- weak credentials
- outdated firmware
- unnecessary trust between devices
- a device whose failure would cripple the mission

Your job is to examine a network map, decide what is most important,
and then justify either how to defend it or how to attack it.

This is not a guessing exercise.
Only vulnerabilities that are clearly explained and supported with evidence
will be approved for action.

At the end, the class will compare what the defenders protected with what
the attackers planned to target and determine whether the attack would
likely have succeeded.
</div>

# Troy - The Battlefields

<div class="terminal">
student162@admin162:~/missions/operation_achilles/networks$ ls

To get the resources for this exercise, download them from:

SpyVsSpy/OperationAchilles/networks/

Open a terminal and run the following commands.

To get the resources for the basic star:

wget https://raw.githubusercontent.com/jboyce1/SpyVsSpy/main/OperationAchilles/networks/basic_star.drawio
wget https://raw.githubusercontent.com/jboyce1/SpyVsSpy/main/OperationAchilles/networks/basic_star_infrastructure.txt


To get the resources for the full mesh:

wget https://raw.githubusercontent.com/jboyce1/SpyVsSpy/main/OperationAchilles/networks/full_mesh.drawio
wget https://raw.githubusercontent.com/jboyce1/SpyVsSpy/main/OperationAchilles/networks/full_mesh_infrastructure.txt


To get the resources for the partial mesh:

wget https://raw.githubusercontent.com/jboyce1/SpyVsSpy/main/OperationAchilles/networks/partial_mesh.drawio
wget https://raw.githubusercontent.com/jboyce1/SpyVsSpy/main/OperationAchilles/networks/partial_mesh_infrastructure.txt


To get the resources for the tree:

wget https://raw.githubusercontent.com/jboyce1/SpyVsSpy/main/OperationAchilles/networks/tree.drawio
wget https://raw.githubusercontent.com/jboyce1/SpyVsSpy/main/OperationAchilles/networks/tree_infrastructure.txt
</div>

<div class="scroll-box">
This lesson introduces common network topologies and asks you to think about
how structure affects security.

Topologies you may see:
- Star
- Tree
- Full Mesh
- Partial Mesh

As you study each network, pay attention to:
- where communication depends on one device
- where trust is concentrated
- where credentials may be stored or transmitted
- where a single failure could disrupt the network
- where segmentation appears weak or absent
</div>

<div class="terminal">
student162@admin162:~/missions/operation_achilles$ cat lecture_notes.txt

NETWORK TYPES:
- Star: a central device connects many endpoints. Efficient, but the center
  can become a critical point of failure.
- Tree: layered branching structure. Good for organization and scale, but
  compromise near the top can affect large portions of the network.
- Full Mesh: devices connect broadly to each other. Resilient, but difficult
  to secure and monitor if trust spreads too widely.
- Partial Mesh: some redundancy without full connectivity. Better efficiency,
  but weakly chosen connections can still expose critical paths.

HARDWARE VULNERABILITIES:
- unmanaged switches
- insecure wireless access points
- exposed ports
- weakly secured routers
- shared admin interfaces
- poor physical security
- consumer hardware used in enterprise roles

FIRMWARE VULNERABILITIES:
- outdated router firmware
- default credentials left enabled
- old access point software
- unpatched switch management interfaces
- insecure remote administration
- known CVEs not remediated

BOTTOM LINE:
The network diagram is not just a picture.
It is a map of trust, dependence, and opportunity.
</div>

# King Priam of Troy (blue mission)

## Defend your network

<div class="terminal">
student162@blue-team:~/missions/operation_achilles$ cat defend.txt

ROLE:
You are a newly hired sysadmin defending a network of Troy besieged by the Achaeans.

MISSION:
Identify the most critical vulnerability or high-value target in the network.
Recommend what must be defended first.
Convince the CEO / Superintendent that your recommendationds are specific,
important, and supported by evidence.

EXPECTED OUTPUT:
A short executive briefing with:
- the network map enumerated with relevant details
- the most critical vulnerabilities or targets called out
- what actions should be taken and why it matters
  minimum of 2 'fixes' and max of 6 'fixes' proposed
- what damage or problems not fixing the issues would cause
- evidence from the topology, device role, trust relationships, or known
  weaknesses in hardware / firmware / credentials

RULE:
Only vulnerabilities that are well described will be approved for action.
If you cannot explain it clearly, you are not ready to defend it.
</div>

<div style="text-align: right;">
  <img src="{{ 'OperationAchilles/site/achilles-need-sword.gif' | relative_url }}" alt="Achilles" style="max-width: 80%; height: auto;">    
</div> 

<div class="scroll-box">
Blue team members should think like sysadmins, not just like people naming
random cyber threats. Your task is to decide what is most important to keep
safe. That might be a server, a router, a wireless segment, a set of
credentials, or a choke point in the topology.

Your presentation should answer:
1. What should be defended first?
2. Why is it the most critical point?
3. What would an attacker gain if it were compromised?
4. What business, school, or mission impact would follow?
5. What concrete defensive action should be taken?

Acceptable evidence may include (not limited to):
- centrality in the network map
- control over authentication or routing
- access to sensitive data
- potential to disrupt availability
- likely role in confidentiality or integrity loss
- outdated or vulnerable hardware / firmware
</div>

### Template:
[Operation Achilles Defend Template](https://raw.githubusercontent.com/jboyce1/SpyVsSpy/main/OperationAchilles/OperationAchilles-Defend.odp)

# This is Sparta (attack frameworks)
## Cyber Kill Chain
### "Come back with your shield, or on it."
<div class="terminal">
student162@admin162:~/frameworks$ cat cyber_kill_chain.txt

1. Reconnaissance
   The attacker gathers information about the target before acting.

2. Weaponization
   The attacker prepares a method, payload, or exploit for use.

3. Delivery
   The attacker transmits the malicious tool or access method to the target.

4. Exploitation
   The attacker triggers a weakness to gain execution or access.

5. Installation
   The attacker establishes a foothold on the target system.

6. Command and Control
   The attacker creates a way to remotely direct compromised systems.

7. Actions on Objectives
   The attacker achieves the goal: theft, disruption, surveillance, or damage.
</div>

## MITRE
### "He who sweats more in training bleeds less in war."

<div class="terminal">
student162@admin162:~/frameworks$ cat mitre_tactics.txt

Reconnaissance
Gathering information about the target organization, people, and systems.

Resource Development
Acquiring or building infrastructure, accounts, tools, or capabilities.

Initial Access
Getting into the target environment for the first time.

Execution
Running malicious code or attacker-controlled actions on a system.

Persistence
Maintaining access across reboots, logouts, or defensive actions.

Privilege Escalation
Gaining higher-level permissions than originally obtained.

Defense Evasion
Avoiding detection or bypassing security controls.

Credential Access
Stealing or abusing usernames, passwords, tokens, or hashes.

Discovery
Learning how the target environment is structured and what exists inside it.

Lateral Movement
Moving from one system or account to another inside the network.

Collection
Gathering data of interest from systems or users.

Command and Control
Communicating with compromised systems to issue instructions.

Exfiltration
Removing data from the target environment.

Impact
Disrupting, destroying, changing, or denying access to systems or data.
</div>

### "We've forgotten the first half of your speech and didn't understand the second."

# King Menelaus of Sparta (red mission)

## Plan an attack

<div class="terminal">
student162@red-team:~/missions/operation_achilles$ cat attack.txt

ROLE:
You are working for Sparta and have been tasked with planning a breach of Troy.

MISSION:
Think like an attacker.
Study the network you have been given.
Identify the most promising target and explain how you would attack it.

EXPECTED OUTPUT:
A short approval briefing to your boss with:
- the target(s) you intend to attack
  min target 1 max targets 4
- why that target is vulnerable or high value
- what attack path you will attempt
- what effect you hope to achieve
- which Cyber Kill Chain step(s) you'll use
- which MITRE tactic(s) best match your plan
- evidence from the network map, device role, trust relationships, or weak
  hardware / firmware / credentials

RULE:
Only breaches that are specific will be approved.
This you're walking into enemy territory and known breech will weaken other efforts
</div>

<div style="text-align: right;">
  <img src="{{ 'OperationAchilles/site/achilles-spear-throw.gif' | relative_url }}" alt="Achilles" style="max-width: 80%; height: auto;">    
</div> 

<div class="scroll-box">
Red team members must move beyond "what looks vulnerable" and explain
"how the attack would actually work."

Your presentation should answer:
1. What target would you choose first?
2. Why is that target reachable or weak?
3. What do you gain if it is compromised?
4. What could you do next from there?
5. What evidence supports your plan?

Strong attack plans may focus on:
- a central router or switch
- exposed wireless access
- credentials likely to provide privileged access
- an unpatched or poorly managed device
- a system whose compromise enables lateral movement
- a target whose failure damages confidentiality, integrity, or availability
</div>

Template:
[Operation Achilles Attack Template](https://raw.githubusercontent.com/jboyce1/SpyVsSpy/main/OperationAchilles/OperationAchilles-Attack.odp)


# Review questions

<div class="terminal">
student162@admin162:~/missions/operation_achilles$ cat review_questions.txt

1. How does network topology shape both attack opportunities and defense priorities?

2. In a star or tree network, what devices become the most dangerous to lose,
   and why?

3. What is the difference between a "valuable" target and a "vulnerable" target?

4. Why might an attacker choose credentials or wireless access over directly
   attacking a server?

5. How can defenders use knowledge of network structure to make attacks more
   difficult or less rewarding?

6. What tradeoffs appear when you improve security but reduce convenience,
   efficiency, or ease of management?

7. Why is it dangerous to describe a cyber attack too vaguely?

8. What kinds of evidence make a defense recommendation convincing?

9. If both teams study the same network, why might they still choose
   different priorities?

10. After comparing the red plan and the blue defense, what would you change
    in the network first if you were actually responsible for it?
</div>

<div style="text-align: right;">
  <img src="{{ 'OperationAchilles/site/achilles_dodge.gif' | relative_url }}" alt="Achilles" style="max-width: 80%; height: auto;">    
</div> 
# Standards

<div class="terminal">
student162@admin162:~/SpyVsSpy$ cat PA_standards_operation_achilles.txt

3A.NI.04 - Evaluate the scalability and reliability of networks by describing
the relationship between routers, switches, servers, topology, and addressing.

3A.NI.05 - Give examples to illustrate how sensitive data can be affected by
malware and other attacks.

3A.NI.06 - Recommend security measures to address various scenarios based on
factors such as efficiency, feasibility, and ethical impacts.

3A.NI.08 - Explain tradeoffs when selecting and implementing cybersecurity
recommendations.

15.4.8.F - Identify network communication technologies.

6.4.8.D - Explain how transportation, communication networks, and technology
affect economic interdependence.
</div>
