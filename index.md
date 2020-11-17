---
title: Alex Marder's Website
---

Welcome to my github website.
I'm currently a research scientist at CAIDA/UCSD focusing on Internet measurements, and anything related to uncovering and interpreting the topology of the Internet.
I received my PhD at the University of Pennsylvania in 2019.
I can be reached at amarderATcaidaDOTorg.

# Research
## Learning to Extract and Use ASNs in Hostnames
Authors: Matthew Luckie, **Alexander Marder**, Marianne Fletcher, Bradley Huffaker, kc claffy

One major problem with inferring router operators is the lack of validation information available.
We used bdrmapIT's inferences as input to a machine learning algorithm to extract AS operator information from DNS hostnames.
This can provide much greater breadth to router operator validation.

<details>
<summary><b>Abstract</b></summary>

### Abstract
We present the design, implementation, evaluation, and validation of a system that learns regular expressions (regexes) to extract Autonomous System Numbers (ASNs) from hostnames associated with router interfaces.
We train our system with ASNs inferred by RouterToAsAssignment and bdrmapIT using topological constraints from traceroute paths, as well as ASNs recorded by operators in PeeringDB, to learn regexes for 206 different suffixes.
Because these methods for inferring router ownership can infer the wrong ASN, we modify bdrmapIT to integrate this new capability to extract ASNs from hostnames.
Evaluating against ground truth, our modification correctly distinguished stale from correct hostnames for 92.5% of hostnames with an ASN different from bdrmapIT’s initial inference.
This modification allowed bdrmapIT to increase the agreement between extracted and inferred ASNs for these routers in the January 2020 ITDK from 87.4% to 97.1% and reduce the error rate from 1/7.9 to 1/34.5.
This work presents a new avenue for collecting validation data, opening a broader horizon of opportunity for evidence-based router ownership inference.

<summary><b>Resources</b></summary>

### Resources
[Paper website](https://www.caida.org/publications/papers/2020/learning_extract_use_asns/) <br />
[IMC 2020 Paper](https://www.caida.org/publications/papers/2020/learning_extract_use_asns/learning_extract_use_asns.pdf) <br />
[IMC 2020 Presentation](https://www.youtube.com/watch?v=SuUoSxsjp9s) <br />
</details>

## Alias Pruning by Path Length Estimation (APPLE)
Authors: **Alexander Marder**

APPLE is a new alias resolution technique that uses pings from many vantage points to group together addresses they belong to the same routers.
This is not the expected final product, but a proof of concept that the technique has merit.

### Abstract
Uncovering the Internet’s router graph is vital to accurate measurement and analysis.
In this paper, we present a new technique for resolving router IP aliases that complements existing techniques.
Our approach, Alias Pruning by Path Length Estimation (APPLE), avoids relying on router manufacturer and operating system specific implementations of IP.
Instead, it filters potential router aliases seen in traceroute by comparing the reply path length from each address to a distributed set of vantage points.

We evaluated our approach on Internet-wide collections of IPv4 and IPv6 traceroutes.
We compared APPLE’s router alias inferences against router configurations from two R&E networks, finding no false positives.
Moreover, APPLE’s coverage of the potential alias pairs in the ground truth networks rivals the current state-of-the-art in IPv4, and far exceeds existing techniques in IPv6.
We also show that APPLE complements existing alias resolution techniques, increasing the total number of inferred alias pairs by 109.6% in IPv4, and by 1071.5% in IPv6.

### Resources
[PAM 2020 Paper](data/apple/apple.pdf) <br />
[PAM 2020 Presentation](https://www.youtube.com/watch?v=GU_MJQGYXFQ) <br />
[Github Repository](https://github.com/alexmarder/apple)

## vrfinder
Authors: **Alexander Marder**, Matthew Luckie, Bradley Huffaker, kc claffy

Finds outbound addresses (usually caused by L3VPNs) in traceroute paths.

### Abstract
Current methods to analyze the Internet’s router-level topology with paths collected using traceroute assume that the source address for each router in the path is either an inbound or off-path address on each router.
In this work, we show that outbound addresses are common in our Internet-wide traceroute dataset collected by CAIDA’s Ark vantage points in January 2020, accounting for 1.7% – 5.8% of the addresses seen at some point before the end of a traceroute.
This phenomenon can lead to mistakes in Internet topology analysis, such as inferring router ownership and identifying interdomain links.
We hypothesize that the primary contributor to outbound addresses is Layer 3 Virtual Private Networks (L3VPNs), and propose vrfinder, a technique for identifying L3VPN outbound addresses in traceroute collections.
We validate vrfinder against ground truth from two large research and education networks, demonstrating high precision (100.0%) and recall (82.1% – 95.3%).
We also show the benefit of accounting for L3VPNs in traceroute analysis through extensions to bdrmapIT, increasing the accuracy of its router ownership inferences for L3VPN outbound addresses from 61.5% – 79.4% to 88.9% – 95.5%.

### Resources
[SIGMETRICS 2020 Paper](data/vrfinder/vrfinder.pdf)<br />
[SIGMETRICS 2020 Presentation](https://www.youtube.com/watch?v=P9jrEz2trJs)

## bdrmapIT
Authors: **Alexander Marder**, Matthew Luckie, Amogh Dhamdhere, Bradley Huffaker, kc claffy, Jonathan M. Smith

<tt>bdrmapIT</tt> creates accurate maps of the Internet's graph.
It uses traceroutes from any number of vantage points and identifies the AS operator for every router interface address seen in the tracroute dataset.

### Abstract
Two complementary approaches to mapping network boundaries from traceroute paths recently emerged.
Both approaches apply heuristics to inform inferences extracted from traceroute measurement campaigns.
[bdrmap](https://www.caida.org/publications/papers/2016/bdrmap/) used targeted traceroutes from a specific network, alias resolution probing techniques, and AS relationship inferences, to infer the boundaries of that specific network and the other networks attached at each boundary.
[MAP-IT](#map-it) tackled the ambitious challenge of inferring all AS-level network boundaries in a massive archived collection of traceroutes launched from many different networks.
Both were substantial contributions to the state-of-the-art, and inspired a collaboration to explore the potential to combine the approaches.
We present and evaluate bdrmapIT, the result of that exploration, which yielded a more complete, accurate, and general solution to this persistent and central challenge of Internet topology research.
bdrmapIT achieves 91.8%-98.8% accuracy when mapping AS boundaries in two Internet-wide traceroute datasets, vastly improving on MAP-IT’s coverage without sacrificing bdrmap’s ability to map a single network.

### Resources
[IMC 2018 Paper]((data/bdrmapit/bdrmapit_paper.pdf))<br />
[IMC 2018 Slides](data/bdrmapit/bdrmapit_slides.pdf)<br />
[Github Repository](https://github.com/alexmarder/bdrmapit)

## MAP-IT
Authors: **Alexander Marder**, Jonathan M. Smith

A constant challenge to both researchers and network diagnosticians is identifying AS boundaries in traceroute data.
We provide the MAP-IT algorithm for doing so that is highly precise and is able to identify most inter-AS links that are revealed through traceroute.

### Abstract
Mapping the Internet at scale is increasingly important to network security, failure diagnosis, and performance analysis, yet remains challenging.
Accurately determining the interface IP addresses used for inter-AS links from traceroute traces can be hard because these interfaces are often assigned addresses from neighboring ASes.
Identifying these interfaces can benefit Internet researchers and network diagnosticians by providing accurate IP-to-AS mappings where such mapping is most difficult - at AS boundaries.

We describe a new algorithm, Multipass Accurate Passive Inferences from Traceroute (MAP-IT), for inferring the exact interface addresses used for point-to-point inter-AS links, as well as the specific ASes involved.
MAP-IT combines evidence of an AS switch from distinct traceroute traces; using traceroute data makes it portable across IP networks.
Each pass leverages prior inferences to refine existing inferences and to discover additional inter-AS link interfaces.

We test MAP-IT with interface-level ground truth information from Internet2, achieving 100% precision.
Using approximate ground truth from Level 3 and TeliaSonera yields 95.0% precision.
These results suggest that MAP-IT is sufficiently reliable for network diagnostics.

### Resources
[IMC 2016 Paper](data/mapit/mapit_paper.pdf)<br />
[IMC 2018 Slides](data/mapit/mapit_imc_slides.pdf)<br />
[Github Repository](https://github.com/alexmarder/MAP-IT)
