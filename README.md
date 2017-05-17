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
* PI code was writted by Python 2.x. In the old version of `PI-0.01.tgz`, PI.tgz imported the Numerical function which was outdated. So, the author has produced the `PI-0.02beta.tgz` version which has conquered the Numertical warnings by using the new function of NumPy. 

* In the python environment, PI code complements the job of comparing two sequences of frames or packets to give two new sequences with the symbol of gap as the follow. The example can illustrate that the sequence alignment algorithm can pick two different protocol sequences for analyzing the common and diversity fields of protocol.

**Input Two Network Packets**</br>
`http://github.com/TomSmith/Hello-World`</br>
`https://github.com/STAN/HelloWorld`</br>
**Output**</br>
`http_://github.com/_TomSmith/Hello-World`</br>
`https://github.com/STAN_____/Hello_World`</br>

# The development of PI project Programming Code
* In 2004, the old version of PI-0.01.tgz was uploaded to this website `http://www.4tphi.net/~awalters/PI/PI.html` by the author of PI project. He has a lecture on the Toorcon 2004 conference, which has a [video recording on the Youtube](https://www.youtube.com/watch?v=YLDWBSyjkAc).

![](https://github.com/bitpeach/Protocol-Informatics/blob/master/%5BOld%20Website%5D4tphi_net.png)

* Now his old version code of `4tphi.net` domain has disappeared. Instead, a new domain name `http://phreakocious.net/PI/` has been changed during March, 2017. The `PI-0.02beat` version code has been uploaded to [this new website](http://phreakocious.net/PI/).

![](https://github.com/bitpeach/Protocol-Informatics/blob/master/%5BNew%20Website%5DProtocol%20Informatics%20-%20Tools%20for%20Binary%20Protocol%20Analysis.png)
