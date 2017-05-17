# Protocol-Informatics
“Protocol Informatics” is a project to design for automatically network protocol reverse engineering based on frame or packet analysis. "PI" is short for “Protocol Informatics”, which introduces local and global sequence alignment algorithms. The PI project is famous in network protocol reverse engineering based on network trace. I am **not** the author of PI project but an amateur of PI project. However, the previous website storing old codes of PI project has been disappeared. That warns and makes me to open a github issue to keep the codes of PI poject for the convenience of other researchers.

# What is network protocol reverse engineering
* According to reference, a certain of traffic on backbone networks worldwide comprises protocols of nonpublic descriptions such as C&C botnet servers, data link networks, wireless network protocols, instant messaging protocols and industrial control protocols.
 
* Automatic protocol reverse engineering processes undocumented protocols to deduce message formats without a priori knowledge of protocol specifications. With the help of closed-protocol analysis, network protocol reverse engineering (NPRE) plays an important role in network management and security applications (e.g. intrusion detection systems and vulnerability mining). 

* In early, network protocol analysis is currently performed by hand using only intuition and a protocol analyzer tool such as tcpdump or Ethereal. Now, automatic analysis way is developed by the researchers because of the time-consumig work in the NPRE. To date, network-based, program-based and hybrid methods have constituted the types of NPRE techniques.

# What is the algorithm of PI (Protocol Informatics)
* An early attempt in automatic NPRE, the Protocol Informatics (PI) Project (as this Github Repository shown), applied a multiple sequence alignment (MSA) algorithm to extract the protocol structure and infer message fields from network traces.

* The core of PI project is the sequence alignment. The author of PI project found the sequence alignment algorithm from bioinformatics is able to applicable for field extraction of protocol sequences as well. The sequence alignment algorithm at first was used for the DNA similarity detection.

* The principle of algorithm can be outlined as the follow.

![](https://github.com/bitpeach/Protocol-Informatics/blob/master/PI%20paper%20figure.png)

# What is code of PI
* PI code was writted by Python 2.x. In the old version, PI.tgz imported the Numerical Function which was outdated. So, the author has produced the PI-0.02 beta version which has conquered the Numertical wanrings. 
