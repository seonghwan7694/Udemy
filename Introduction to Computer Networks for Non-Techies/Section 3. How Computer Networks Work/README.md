# Section 3. How Computer Networks Work

### 18. Introduction to Computer Networking Protocols

Computer communicate with each other with network protocols.

**Protocols are rules** governing how machines exchange data and enable effective communication.

**Physical Protocols** : describe **the medium**(wiring), **the connections**(RJ-45 port), and **the signal**(voltage level on a wire).

**Logical Protocols** : software controlling how and when data is sent and received to computers, supporting physical protocols.

Computer networks depend on many different types of protocols in order to work properly.

### 19. Introduction to the OSI Model

The Open Systems Interconnection (OSI) is **Reference Model**.

- **A conceptual framework** showing us **how data moves throughout a network**.
- Developed by the International Organization for Standardization(ISO) in 1977.
  
**OSI Model gives us a guide to understanding how networks operate. It's only a reference model. Wasn't implemented in the real word, TCP/IP is.**

The OSI Model breaks down the complex task of computer-to-computer network communications into seven layers.

- Upper Layers(Host Layers, L4 to L7) : Handled by the host computer and performs application-specific functions such as data formmating, encryption, and connection management.
- Lower Layers(Media Layers, L1 to L3) : Provide network-specific functions such as routing, addressing, and flow control.

|   Data  |        Layer       |                  Specific                  |
|:-------:|:------------------:|:------------------------------------------:|
|   Data  |  Application Layer |       Network Process to Application       |
|   Data  | Presentation Layer |      Data Representation & Encryption      |
|   Data  |    Session Layer   |           Interhost Communication          |
| Segment |   Transport Layer  |     End-to-End Connection & Reliability    |
|  Packet |    Network Layer   | Path Detemination & IP(Logical Addressing) |
|  Frame  |   Data Link Layer  |      MAC and LLC(Physical Addressing)      |
|   Bit   |   Physical Layer   |    Media, Signal & Binary Transmissions    |

**P**lease **D**o **N**ot **T**hrow **S**ausage **P**izza **A**way

### 20. Introduction to the TCP/IP Model

The TCP/IP suite is the most commonly used protocol suite in the networking world.

It’s essentially the protocol suite in which the Internet was built.

It’s the standard for computer networking.

It is based on a 4-layer model that is similar to the OSI model.

|   Data  |        Layer       |                  Specific                  |
|:-------:|:------------------:|:------------------------------------------:|
|   Data  |  Application Layer |       Network Process to Application       |
|   Data  | Presentation Layer |      Data Representation & Encryption      |
|   Data  |    Session Layer   |           Interhost Communication          |
| Segment |   Transport Layer  |     End-to-End Connection & Reliability    |
|  Packet |    Network Layer   | Path Detemination & IP(Logical Addressing) |
|  Frame  |   Data Link Layer  |      MAC and LLC(Physical Addressing)      |



