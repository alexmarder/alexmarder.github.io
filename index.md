---
title: Alex Marder's Website
---

Welcome to my github website.
I'm currently a postdoc at CAIDA/UCSD focusing on Internet measurements, and anything related to uncovering the topology of the Internet.
I received my PhD at the University of Pennsylvania in 2019.
I can be reached at amarderATcaida.org.

# Research
## bdrmapIT
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
