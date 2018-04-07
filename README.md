# Protocol-Informatics
* `Protocol Informatics Project` is a project for automatically network protocol reverse engineering based on protocol frames or packets. "PI" is short for “Protocol Informatics”, which introduces local and global sequence alignment algorithms. The `PI` project is famous in network protocol reverse engineering based on network trace. I am `not` the author of `PI` project but an amateur of `PI` project, which was undertaking by its author `Marshall A. Beddoe`.

* In 2017, the previous website storing old codes of `PI` project has disappeared. However, those program codes or ideas have been deeply promoting the protocol-reversing researching work. That warns me to open a github issue to back up `PI` project codes for the convenience of other researchers.

# What is network protocol reverse engineering
* According to reference, a certain of traffic on backbone networks worldwide comprises protocols of nonpublic descriptions such as C&C botnet servers, data link networks, wireless network protocols, instant messaging protocols and industrial control protocols.
 
* Automatic protocol reverse engineering processes undocumented protocols to deduce message formats without a priori knowledge of protocol specifications. With the help of closed-protocol analysis, network protocol reverse engineering (NPRE) plays an important role in network management and security applications (e.g. intrusion detection systems and vulnerability mining). 

* In early, network protocol analysis was intuitively performed by hands. Then, the protocol analyzer tools were considered such as tcpdump or Ethereal. Now, the methods of automatic protocol analyses are developed by the researchers because of the time-consuming and diverse works in the different NPRE. To date, network-based, program-based and hybrid methods have constituted the types of NPRE techniques.

# What is the algorithm of `PI` (Protocol Informatics)
* An early attempt in automatic NPRE, such as Protocol Informatics (`PI`) Project, applied a multiple sequence alignment (MSA) algorithm to extract the protocol structure and infer message fields from network traces.

* The core of `PI` project is the sequence alignment. The sequence alignment algorithm at first was used for the DNA similarity detection. The author of `PI` project found the sequence alignment algorithm from bioinformatics is applicable to the field extraction of protocol sequences as well.

* The [paper](https://github.com/bitpeach/Protocol-Informatics/blob/master/PI%20paper%20(Network%20Protocol%20Analysis%20using%20Bioinformatics%20Algorithms).pdf) entitled `Network Protocol Analysis using Bioinformatics Algorithms` has been presented by its author `Marshall A. Beddoe`. The principle of algorithm can be outlined as the follow.

![](https://github.com/bitpeach/Protocol-Informatics/blob/master/PI%20paper%20figure.png)

# What is code of `PI`
* `PI` code was writted by Python 2.x. In the old version of `PI-0.01.tgz`, `PI.tgz` imported the Numerical function which was outdated. So, another author [`@phreakocious`](https://twitter.com/phreakocious) has produced the `PI-0.02beta.tgz` version which has conquered the Numertical warnings by using the new function of NumPy. It is really excellent work that `Marshall A. Beddoe` and `@phreakocious` do.

* In the python environment, `PI` code complements the job of comparing two sequences of frames or packets to give two new sequences with the symbol of gap as the follow. The example as follows can illustrate that the sequence alignment algorithm can analyse the common and diversity fields of packets or frames when comparing two different protocol sequences by the sequence alignment.

**Input Two Network Packets**</br>
`http://github.com/TomSmith/Hello-World`</br>
`https://github.com/STAN/HelloWorld`</br>
**Output**</br>
`http_://github.com/_TomSmith/Hello-World`</br>
`https://github.com/STAN_____/Hello_World`</br>

# The development of `PI` project Programming Code
* In 2004, the old version of `PI-0.01.tgz` was uploaded to this website `http://www.4tphi.net/~awalters/PI/PI.html` by the author of `PI` project. He has a lecture on the Toorcon 2004 conference, which has a [video recording on the Youtube](https://www.youtube.com/watch?v=YLDWBSyjkAc).

![](https://github.com/bitpeach/Protocol-Informatics/blob/master/%5BOld%20Website%5D4tphi_net.png)

* Now his old version code of `4tphi.net` domain has disappeared. Instead, a new domain name `http://phreakocious.net/PI/` has been changed during March, 2017. The `PI-0.02beat` version code has been uploaded to [this new website](http://phreakocious.net/PI/). The author [`phreakocious`](https://github.com/phreakocious) contributes the important work as well.

![](https://github.com/bitpeach/Protocol-Informatics/blob/master/%5BNew%20Website%5DProtocol%20Informatics%20-%20Tools%20for%20Binary%20Protocol%20Analysis.png)

# The characteristics of `PI` project Code 
* For the 0.01 version, the old code has several errors. The data structures adopted the Numerical library, which has been disappeared in the new library of Numpy.

* For the 0.02 version, this code has several updates. According to [the author](http://phreakocious.net/PI), there are some enhancements to the original tool:
- [x] Replaced the deprecated Numeric Python library with numpy.

- [x] Detection of terminal width to maximize screen real estate using python-consolesize.

- [x] Updated command line arguments for xargs in Makefile.
