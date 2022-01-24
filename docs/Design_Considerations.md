# Design Considerations

**Note**: This file is written according to the current status of the project. It will be regularly updated to reflect new ideas, 
design decisions, answers to how-to questions, and so on, according to the development of the project. 

Note that this file mostly contains *project ideas*, is provided only as a draft. *Some* of the design requirements are highlighted, 
with their reasons and results. Also, some thoughts about what has to be done is given. These ideas should not be taken as exact requirements, 
they are only given as helping aids. It is nice if you have words to say!  

Any part of the proposed system (Teleporta) can be changed, updated, or deleted, including the names in the system. 
Do not hesitate to share your ideas, ask questions, or make suggestions of "wouldn't-it-be-nice-if-we-add-this-feature" concepts. 
Also, if you have great ideas on the design of the system, or you want to help implementing it, that is great! 
For [contributions](../CONTRIBUTING.md), please email me at [ilterismanisali@teleporta.org](mailto:ilterismanisali@teleporta.org). 
Any contributions are welcome, and are greatly appreciated. 

Teleporta has its own terminology (which can be changed as proposed). If any of the terms, names or the systems are unfamiliar to you,
please check out our [key terminology](Key_Terminology.md) Some features of Teleporta are repeated here, to understand the design problems. 
For better understanding of the proposed system, check out the [concepts](Conceptual_Understanding.md).
For more detailed information, check out the Docs folder. 

# Short Summary of Teleporta

Teleporta is based on the idea that with clever combination of revolutionary technologies like internet, 3D printers and blockchain, 
we can develop a decentralized transportation system that does not include any physical medium between the sender and receiver. 
To develop such a system, three different (but related) components are necessary:
- **Smart Transporters**: This is the *hardware* part of the system, responsible for the physical transportation. 
- **Virtual Transportation System (VTS)**: This is the internet system that connects two Smart Transporters.
- **Portal**: The blockchain system that is responsible for the security and economics in the system. 

Smart Transporters will also have three components, a 3D printer, a 3D scanner and so-called **3D recycler**, responsible for the melting.

Virtual Transportation system will be responsible for the communications between any two Smart Transporters. 3D models and operation instructions
to the Smart Transporters are sent. These files and instructions might possible be needed to be encrypted (depending on the case). The system must work together 
with the Portal. All information (or some of it) might be stored on the blockchain.  

Portal will be the blockchain-based system. 

For a detailed explanation of Teleporta, check out [features of Teleporta](../WHITEPAPER.md).

# Important Design Decisions 

Before we start the implementations, we need to clearly define the interfaces between these systems. Along the way, there are important design decisions to make.
Few considerations that comes to mind are:
- Do we need to develop our own blockchain, or can we use existing blockchain mediums like Ethereum?
- How to design and manufacture Smart Transporters? 
- What file transfer protocols must be used in VTS? 

1. Smart Transporters: The design of Smart Transporters requires some thought. 
As an analogy, in Teleporta, we are trying to design both the *internet* and the *computer* together, one cannot exist without the other. 
However, the *computer* does not exist in our case, we need to design it. Some of the components do exist, though. The properties of 
3D printers and 3D scanners are known, and melting devices are simple to design in principle. But they still need to be combined. 
Also, Teleporta needs to allow the existing owners of 3D printers and scanners to use the system, without Smart Transporters. 

2. Blockchain system: We need to decide whether we need our own blockchain system, or should we use one of the existing blockchains
like Ethereum. We also need to decide how this system interfaces with VTS. 

3. Standardization Required: Teleporta needs to guarantee that the reproduced item has the same properties with the original item.
To be able to transport goods anywhere globally, we need to ensure that Teleporta produces all items with the same or similar quality,
with some guarantees provided by the system. For this purpose, we need to design a standardization system that is shared by both Smart Transporters 
and third-party 3D printers and scanners, so that anyone can use the system fearlessly about the quality of the transported product. 


# Smart Transporters Manufactured By Smart Transporters? 

Note that the hardware must be manufactured, for the users to be able to use the Teleporta. For world-wide adoption, massive production of Smart Transporters
is required. It is known in open-source 3D communities that the components of some 3D printers can be manufactured by 3D printers, which, in a sense, 3D printers
manufacturing themselves. It is a feasible design feature for Smart Transporters. If Smart Transporters will be able to build other Smart Transporters,
at least some parts, the system is allowed to build itself. 
