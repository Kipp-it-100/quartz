---
sticker: lucide//layers
tags: 
aliases:
  - OSI
  - OSI model
---
# The OSI Model
  
The OSI Model, short for "Open Systems Interconnection," is a conceptual framework used to understand and standardize the functions of a telecommunication or computing system without regard to its underlying internal structure and technology. Its goal is to facilitate the interoperability of diverse communication systems with standard protocols. The OSI Model is divided into seven layers, each with specific responsibilities:

## Contains seven layers

### Layer 7 - Application
The Application layer is the closest to the end user. It interacts with software applications that implement a communicating component. This layer provides services such as email, file transfer, and web browsing.

Devices

### Layer 6 - Presentation
This layer translates data between the application layer and the network. It's responsible for data encryption, decryption, compression, and conversion to ensure that data from the application layer of one system can be read by the application layer of another.

### Layer 5 - Session
The Session layer establishes, manages, and terminates connections between applications. It sets up, coordinates, and terminates conversations, exchanges, and dialogues between the applications at each end.

### Layer 4 - Transport 
The Transport layer provides transparent transfer of data between end systems or hosts. It is responsible for error recovery, data integrity, and flow control mechanisms. This layer ensures complete data transfer.

### Layer 3 - Network
This layer is responsible for packet forwarding, including routing through intermediate routers. It's where you'll find most of the routing protocols that manage path determination and logical addressing (IP addresses).

### Layer 2 - Data Link
The Data Link layer is responsible for node-to-node data transfer—a link between two directly connected nodes. It also handles error correction from the physical layer, flow control, and frame synchronization.

### Layer 1 - Physical
This layer deals with the physical connection between devices and the transmission and reception of raw bit streams over a physical medium. It includes specifications for cables, connectors, and signal specification

## Flashcards
#flashcards/osi

which layer is the closest to the user(Number and name)? :: Layer 7, the Application layer.
<!--SR:!2024-07-11,24,270-->

which layer occurs at 
