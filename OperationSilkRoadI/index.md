---
layout: default
title: Operation Silk Road
---

# Operation Silk Road

<div style="text-align: center;">
  <img src="{{ 'OperationSilkRoad/site/silkroad.png' | relative_url }}" alt="Silk Road" style="max-width: 80%; height: auto;">
</div>

<div class="scroll-box">
The Silk Road connected distant civilizations through trade routes that
moved goods, ideas, technologies, and diseases across continents.

Modern computer networks operate in a similar way: information moves through
many intermediaries before reaching its destination.

Operation Silk Road introduces how information travels across networks and
how systems identify where data should go.
</div>

<div class="terminal">
student162@admin162:~/missions/silk_road$ cat overview.txt

MISSION CONTEXT:
The Silk Road linked East and West through long chains of travelers,
caravans, ports, and middlemen.

No single trader usually crossed the entire route.
Goods moved step by step through many hands.

The Internet works the same way.

Information moves through many systems before reaching its destination.

Each device along the path only needs to know where to send the next step.
</div>

# The Historical Silk Road

<div class="scroll-box">
The Silk Road was a network of trade routes connecting China with the
Mediterranean world.

Goods such as silk traveled west while gold, silver, and wool traveled east.

Religions, technologies, and ideas also spread along the same routes.

Like modern networks, the route depended on trust, intermediaries,
and the ability to move information across long distances.
</div>

<div class="terminal">
student162@admin162:~/missions/silk_road$ cat history.txt

Silk Road routes began in Xi'an in China and stretched thousands of miles
through Central Asia toward the Mediterranean.

Caravans moved goods across deserts and mountains before transferring them
to merchants who continued the journey.

Few people traveled the entire distance.

Trade succeeded because many smaller exchanges worked together.

Major trade routes often spread knowledge as well as disease.

Historians believe the Black Death may have spread west along these routes.

Modern highways and rail systems now follow parts of the same path.
</div>

# Video

<div class="scroll-box">
The Internet was designed to connect distant places through shared protocols
and communication systems.
</div>

<div style="text-align: center;">
<iframe width="560" height="315" src="https://www.youtube.com/embed/EOYe71RWMvk?si=0a7Vvt8nh1sCJLu6" title="YouTube video player" frameborder="0" allowfullscreen></iframe>
</div>

# Netsim

<div class="terminal">
student162@admin162:~/missions/silk_road$ cat silk_road.txt

MISSION:
Utilize https://netsim.erinn.io/ to enhance understanding of network communication.

INSTRUCTIONS:
1. Open Firefox
2. Navigate to https://netsim.erinn.io/
3. Log in with the provided username and password
4. Complete the first five levels
5. Submit a screenshot as directed in Teams

LEVELS:
Level 1: Getting Started
Level 2: Packet Fields
Level 3: Ping
Level 4: Routing
Level 5: Modems
</div>

<div class="scroll-box">
Focus on how packets move, how systems identify one another, and how routing
decisions determine where traffic travels.
</div>

# Terms and Ideas

## OSI (Open Systems Interconnection)

<div class="terminal">
student162@admin162:~/missions/silk_road$ cat osi_model.txt

The OSI model describes seven layers used to understand how networks operate.

Each layer handles a different responsibility in the movement of data.

Understanding the layers helps explain where failures or attacks occur.
</div>

## Layers

### 1: Physical Layer

<div class="terminal">
student162@admin162:~/missions/silk_road$ cat layer1.txt

Physical Layer
The physical signals and hardware used to move data between devices.

Examples:
- cables
- fiber
- radio waves
- wireless transmission
</div>

### 2: Data Link Layer

<div class="terminal">
student162@admin162:~/missions/silk_road$ cat layer2.txt

Data Link Layer
The layer responsible for communication between devices on the same network.

MAC Address
A hardware identifier assigned to each network interface.

Header
Information attached to frames that identifies source and destination devices.

FCS Footer
A checksum used to detect corruption during transmission.
</div>

### 3: Network Layer

<div class="terminal">
student162@admin162:~/missions/silk_road$ cat layer3.txt

Network Layer
The layer responsible for moving packets between networks.

Source IP
The address of the sending system.

Destination IP
The address of the receiving system.

Protocol Data Unit (Packet)
The unit of data transmitted at the network layer.

Routing
The process of deciding where packets should travel next.

Routing Table
A list of possible network paths used to forward packets.

Protocols

ICMP
Used for diagnostics and status messages.

ARP
Resolves IP addresses into MAC addresses on local networks.

IGMP
Manages group communication for multicast traffic.

RARP
Used historically to discover IP addresses from hardware addresses.
</div>

### 4: Transport Layer

<div class="terminal">
student162@admin162:~/missions/silk_road$ cat layer4.txt

Transport Layer
The layer responsible for end-to-end communication between systems.

TCP
A reliable protocol that ensures ordered delivery.

UDP
A faster protocol that sends data without guaranteed delivery.
</div>

### 5: Session Layer

<div class="terminal">
student162@admin162:~/missions/silk_road$ cat layer5.txt

Session Layer
The layer responsible for managing communication sessions between systems.
</div>

### 6: Presentation Layer

<div class="terminal">
student162@admin162:~/missions/silk_road$ cat layer6.txt

Presentation Layer
The layer responsible for translating, compressing, or encrypting data.
</div>

### 7: Application Layer

<div class="terminal">
student162@admin162:~/missions/silk_road$ cat layer7.txt

Application Layer
The layer where user-facing network services operate.

Examples include:
- web browsers
- email systems
- file transfer services
</div>

# Discussion

<div class="terminal">
student162@admin162:~/missions/silk_road$ cat discussion.txt

1. How does a modem expose your network to the outside world?

2. What role do routing tables play in deciding where traffic goes?

3. Why might an attacker want to study routing behavior?

4. What information can be learned from a successful ping?

5. When might allowing ping responses become a security risk?

6. Why is it important to understand where packets travel in a network?
</div>

# Standards

<div class="terminal">
student162@admin162:~/SpyVsSpy$ cat PA_standards_silk_road.txt

2.CS.03 - Systematically identify and fix problems with computing devices and their components.

2.NI.04 - Model the role of protocols in transmitting data across networks and the Internet.

3A.CS.02 - Compare levels of abstraction and interactions between application software, system software, and hardware layers.

3A.CS.03 - Develop guidelines that convey systematic troubleshooting strategies others can use.

3A.NI.04 - Evaluate the scalability and reliability of networks by describing the relationship between routers, switches, servers, topology, and addressing.

3A.NI.08 - Explain tradeoffs when selecting and implementing cybersecurity recommendations.

15.4.8.F - Identify network communication technologies.

6.4.8.D - Explain how transportation, communication networks, and technology affect economic interdependence.
</div>
