Domain Generation Algorithm (DGA) Classifier
===================================================================

### Background

The creation of Botnets is an illegal activity that is widely practiced by cyber criminals around the world. A Botnet is a network of compromised computers that have been illegally co-opted and is under the control of a cyber criminal.  Botnets are formed by compromising individual computers, known as Bots, by subvertly installing some form of malicious software that renders control to the Botnet operator.

Cyber criminals generate revenue from Botnets in much the same way as cloud computing providers like Amazon, Google, or Rackspace.  The Botnet operator sells the computational capacity of the Botnet for revenue-generating activities.  These activities can themselves range from the legal to the illegal including sending spam email, mining bitcoins, or generating fraudulant ad click throughs.

#### Command and Control

A Botnet operator must maintain command and control of the Botnet to further their criminal activities.  Typically, each Bot will "phone home" to a Command and Control server on a periodic basis to request the next set of commands.  The necessity for command and control serves as a weak point that can be exploited by those attempting to take down Botnets.  Identifying the means through which a Bot communicates with a Command and Control server can be used to identify and repair individual Bots, revoke control from the Botnet operator, or to identify and apprehend the Botnet operator.

#### Domain Generating Algorithms

Early Botnets simply contained a fixed list of domain names that were used by the Bot to contact a Command and Control server.  For example, each day the Bot would attempt to contact **bot-commander-1.com** and **bot-commander-2.com** for updated commands.  By monitoring network traffic patterns, it was simple to identify and block this fixed list of command and control servers, which rendered the Botnet useless.

Botnet operators evolved Domain Generating Algorithms (DGA) that automatically generate a large list of domain names through which to contact Command and Control servers.  Seeded cryptographic algorithms, similar to security tokens such as the RSA SecurID, enable the Botnet operator, and not those wishing to take down Botnets, to know with some degree of certainty which domains a Bot will use and at which time.  This mechanism makes it difficult to identify and disrupt access to Botnet Command and Control servers.  

This is but one approach among many that are collectively called "Command & Control Discovery Mechanisms."  More advanced approaches will continue to evolve to avoid detection including those that leverage P2P networks or The Onion Router (Tor).

#### DGA Classifier

This project contains a rudimentary classifier that can determine if a domain is legitimate or if it has been generated by a DGA.  Monitoring network traffic with a DGA Classifier enables defenders to identify and remediate Bots before significant damage can be caused.  For example, a computer requesting **ibxaoddvcped.ru** is much more indicative of an a Bot versus one requesting **facebook.com**.

### Approach

### Getting Started



