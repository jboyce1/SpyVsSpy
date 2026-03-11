---
layout: default
title: Operation Silk Road II
---

# Operation Silk Road II

<div style="text-align: center;">
  <img src="{{ 'OperationSilkRoadII/site/silkroadii.png' | relative_url }}" alt="Operation Silk Road II" style="max-width: 80%; height: auto;">
</div>

<div class="scroll-box">
The Silk Road linked distant places through trade, trust, intermediaries, and long routes.
This operation uses that idea to introduce how information moves across networks and how attackers abuse that movement.
</div>

<div class="terminal">
student162@admin162:~/missions/silk_road_ii$ cat overview.txt

MISSION CONTEXT:
Operation Silk Road II focuses on how data travels from one place to another.

You will use a network simulator to observe how traffic moves, how systems
identify one another, and how attacks can interfere with communication.

This lesson builds the foundation for later work involving network mapping,
weak points, and attack planning.

You should leave this lesson with a better understanding of:
- how devices communicate across a network
- how packets move between systems
- how attackers fake, intercept, or overwhelm traffic
- how trust on the Internet can be misused
</div>

# The Silk Road

<div class="scroll-box">
The Silk Road was a long trade network that connected East Asia, Central Asia,
the Middle East, and Europe. It moved goods, ideas, religions, technologies,
and diseases across great distances.
</div>

<div class="terminal">
student162@admin162:~/missions/silk_road_ii$ cat silk_road_facts.txt

1. The Silk Road began more than 2,100 years ago.
   Long-distance trade became useful once states saw value in moving goods
   and messages across regions.

2. The Silk Road covered thousands of miles.
   Like modern networks, it depended on many routes, relay points, and
   intermediaries.

3. Early trade included silk for horses.
   Trade often followed strategic need as much as profit.

4. There were multiple Silk Road routes.
   Networks also use multiple possible paths rather than one straight line.

5. It was the longest major overland trade route of the ancient world.
   Distance created delay, risk, and dependence on trusted middle points.

6. Marco Polo became its most famous traveler.
   Well-known travelers helped spread information between distant regions.

7. The Silk Road eventually declined.
   Trade systems change when routes, technology, or political control change.

8. It changed the world.
   Major networks spread both value and disruption.

9. Buddhism entered China through Silk Road exchange.
   Networks move ideas as well as goods.

10. The name "Silk Road" is modern.
    People often name systems long after they already exist.

11. New "Silk Road" routes exist today.
    Modern transport networks still reshape trade, speed, and influence.
</div>

# Netsim

<div class="terminal">
student162@admin162:~/missions/silk_road_ii$ cat mission.txt

MISSION:
Utilize https://netsim.erinn.io/ to enhance understanding of network communication.

INSTRUCTIONS:
1. Open Firefox
2. Navigate to: https://netsim.erinn.io/
3. Log in with the given username and password
4. Complete the second five levels
5. Submit a screenshot as directed in Teams

LEVELS:
Level 6: IP Spoofing
Level 7: Stealing Packets
Level 8: Basic DoS
Level 9: Distributed DoS
Level 10: Smurf Attack
</div>

<div class="scroll-box">
As you work through the simulator, pay attention to how devices identify one
another, how traffic is routed, and how attacks take advantage of trust.
</div>

# Terms and Ideas

## CIA Triad

<div class="terminal">
student162@admin162:~/missions/silk_road_ii$ cat cia_triad.txt

Confidentiality
Keeping information from being seen by unauthorized people.

Integrity
Keeping information accurate and preventing unauthorized changes.

Availability
Keeping systems and information accessible when needed.
</div>

## Layers

### 1: Physical Layer

<div class="terminal">
student162@admin162:~/missions/silk_road_ii$ cat layer1.txt

Physical Layer
The hardware and signals that move data between devices.

Examples:
- cables
- fiber
- wireless radio
- ports
- switches as physical devices
</div>

### 2: Data Link Layer

<div class="terminal">
student162@admin162:~/missions/silk_road_ii$ cat layer2.txt

Data Link Layer
The layer that moves data between nearby devices on the same network segment.

MAC Address
A hardware address used to identify a network interface on a local network.

Switch
A device that forwards frames based on local hardware addresses.

On-Path / Man in the Middle
An attacker inserts themselves between systems to observe or alter traffic.

Packet Sniffing
Capturing traffic moving across a local segment or shared medium.
</div>

### 3: Network Layer

<div class="terminal">
student162@admin162:~/missions/silk_road_ii$ cat layer3.txt

Network Layer
The layer that moves traffic between networks and determines where it goes.

IP Address
A logical address used to identify a device across networks.

IPv4
The older and still common addressing format.

IPv6
A newer addressing format with a much larger address space.

Routing Table
A list of paths a system uses to decide where traffic should go.

ICMP
A protocol used for control messages, troubleshooting, and status.

Ping
A tool that uses ICMP to test reachability.

Traceroute
A tool that shows the path traffic takes through intermediate systems.

TTL
A value that limits how long a packet can travel before being discarded.

IP Spoofing
Faking a source IP address to mislead the target or hide the sender.

Basic Denial of Service
Overwhelming a target with traffic from one source.

Distributed Denial of Service
Overwhelming a target with traffic from many sources.

Smurf Attack
A denial-of-service attack that abuses ICMP broadcast behavior.

Smurf Amplifier
A system or network that multiplies attack traffic toward the victim.

Router
A device that forwards traffic between networks.
</div>

### 4: Transport Layer

<div class="terminal">
student162@admin162:~/missions/silk_road_ii$ cat layer4.txt

Transport Layer
The layer that manages end-to-end communication between applications.

Packet
A general unit of network data moving through a system.

TCP
A protocol focused on reliable and ordered delivery.

UDP
A protocol focused on speed with fewer delivery guarantees.

Port
A numbered destination that helps traffic reach the right service.
</div>

### 5: Session Layer

<div class="terminal">
student162@admin162:~/missions/silk_road_ii$ cat layer5.txt

Session Layer
The layer that manages conversations between systems.

Session
A maintained exchange between devices or applications over time.

Connection State
Information about whether a communication session is active and valid.
</div>

### 6: Presentation Layer

<div class="terminal">
student162@admin162:~/missions/silk_road_ii$ cat layer6.txt

Presentation Layer
The layer that translates, formats, compresses, or encrypts data.

Encryption
Changing readable data into protected form.

Encoding
Changing data into a format another system can interpret.

Compression
Reducing data size for storage or transmission.
</div>

### 7: Application Layer

<div class="terminal">
student162@admin162:~/missions/silk_road_ii$ cat layer7.txt

Application Layer
The layer where user-facing network services operate.

Web Browser
A program that requests and displays web content.

Proxy Server
A server that requests content on behalf of another system.

DNS
A service that translates names into IP addresses.

HTTP / HTTPS
Protocols used to request and deliver web content.
</div>

# What to Notice in Netsim

<div class="scroll-box">
Watch how identity, trust, and routing interact. A device may accept traffic
because it appears familiar, reachable, or properly formed even when it is not.
</div>

<div class="terminal">
student162@admin162:~/missions/silk_road_ii$ cat what_to_notice.txt

NOTICE:
- how source and destination addresses affect delivery
- how spoofed traffic changes what a system believes
- how packet capture reveals information in transit
- how denial-of-service changes availability
- how ICMP can be useful for both troubleshooting and abuse
- how trust can be exploited when systems assume traffic is legitimate
</div>

# Discussion

<div class="terminal">
student162@admin162:~/missions/silk_road_ii$ cat discussion.txt

1. If an attacker gains control of confidentiality, how might that hurt a school district?

2. If an attacker gains control of integrity, how might that hurt a local government?

3. If an attacker gains control of availability, how might that hurt a hospital?

4. How does the Internet's trust model create vulnerabilities?

5. Should you be allowed to inspect packets moving through your own network?

6. Should you be allowed to inspect wireless packets moving through your property?

7. What is the difference between observing traffic and changing traffic?

8. Why does it matter whether an attacker is on-path instead of just nearby?

9. How do traceroute and TTL help explain the path traffic takes?

10. Why are proxy servers useful for both legitimate purposes and misuse?
</div>

# Standards

<div class="terminal">
student162@admin162:~/SpyVsSpy$ cat PA_standards_silk_road_ii.txt

2.CS.03 - Systematically identify and fix problems with computing devices and their components.

2.NI.04 - Model the role of protocols in transmitting data across networks and the Internet.

3A.CS.02 - Compare levels of abstraction and interactions between application software, system software, and hardware layers.

3A.CS.03 - Develop guidelines that convey systematic troubleshooting strategies that others can use to identify and fix errors.

3A.NI.04 - Evaluate the scalability and reliability of networks by describing the relationship between routers, switches, servers, topology, and addressing.

3A.NI.08 - Explain tradeoffs when selecting and implementing cybersecurity recommendations.

15.4.8.F - Identify network communication technologies.

6.4.8.D - Explain how the level of transportation, communication networks, and technology affect economic interdependence.
</div>
