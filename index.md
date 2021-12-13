---
title: Alex Marder's Website
---

Welcome to my website.
I'm currently a research scientist at CAIDA/UCSD focusing on Internet measurements, Internet data science, cloud networks, network security.
I received my PhD at the University of Pennsylvania in 2019.
I can be reached at amarderATcaidaDOTorg.

- [Research](#research)
- [Other Recorded Presentation](#other-recorded-presentations)

# Research
## Learning Regexes to Extract Network Names from Hostnames [AINTEC 2021]
Authors: Matthew Luckie, **Alexander Marder**, Bradley Huffaker, kc claffy

Operators often provide DNS hostnames for network interconnection addresses that indicate the interconnecting networks.
We used machine learning to extract network names from the hostnames, and map the names to autonomous system numbers (ASNs).

<details>
<summary><b>Abstract</b></summary>

We present the design, implementation, evaluation, and validation of a system that automatically learns regular expressions (regexes) to extract network names from Internet hostnames assigned by operators using their own conventions.
Our fully automated method does not rely on a human to provide a starting regex, labeled examples of valid extractions, or a dictionary of network names.
Our method first learns the dictionary of network names, and then automatically generates and evaluates regexes that extract these names.
We validate our dictionary against ground truth, finding that 97.3% of the names our regexes extract are valid names for the networks.
</details>

<details>
<summary><b>Resources</b></summary>

[Paper Website](https://catalog.caida.org/details/paper/2021_learning_regexes_extract_network_names)
[AINTEC 2021 Paper](data/aintec21/learning_regexes_extract_network_names.pdf)
</details>

## Learning to Extract Geographic Information from Internet Router Hostnames [CoNEXT 2021]
Authors: Matthew Luckie, Bradley Huffaker, **Alexander Marder**, Zachary Bischof, Marianne Fletcher, kc claffy

DNS hostnames associated with router IP addresses often contain a code indicating the geographic locations of the router.
We devised a machine learning technique to extract and interpret the code.
<details>
<summary><b>Abstract</b></summary>

Geolocating Internet routers is a long-standing and notoriously difficult challenge, and current solutions lack the accuracy and adaptability to yield reliable results.
We revisit this problem, designing a solution capable of accurately and comprehensively extracting geographic information that network operators embed into router interface hostnames.
We train our system using dictionaries that map geographic codes to known locations, and constrain inferences with delay measurements conducted from a distributed set of vantage points.
While most operators use known geographic codes, some devise their own mnemonic codes for locations, which our system also extracts and interprets.

We evaluate our system on Internet-wide topology datasets, automatically learning regular expressions (regexes) for 1023 different domain suffixes with IPv4 routers, and 241 different domain suffixes with IPv6 routers.
We received ground truth from operators of 13 domain suffixes, all of whom confirmed the correctness of our learned regexes, and that our system correctly interpreted 78.6% of the custom geographic codes.
For these 13 suffixes, our solution more accurately extracts and interprets geographic information than the previous state-of-the-art, correctly geolocating 94.0% of router hostnames with a geohint compared to DRoP (56.6%) and HLOC (73.1%).
This work advances the ability of researchers and network operators to characterize the location of critical Internet infrastructure, a foundational building block of network performance, security, and resilience analysis.
We release the source code of our system and our inferred regexes.
</details>

<details>
<summary><b>Resources</b></summary>

[Paper Website](https://catalog.caida.org/details/paper/2021_learning_extract_geographic_information)
[CoNEXT 2021 Paper](data/conext21/learning_extract_geographic_information.pdf)
</details>

## Inferring Regional Access Network Topologies: Methods and Applications [IMC 2021]
Authors: Zesen Zhang, **Alexander Marder**, Ricky Mok, Bradley Huffaker, Matthew Luckie, kc claffy, Aaron Schulman

Mapping access networks in the United States.
For wireline access networks, the maps help reveal the facility-level structure of each access networks and the  edge facilities that rely on other facilities for Internet connectivity.
For wireless networks, we revealed geographic regions that rely on the same exit location from the wireless networks.
We also presented new ways of finding measurement vantage points in wireline and wireless networks.

<details>
<summary><b>Abstract</b></summary>

Using a toolbox of Internet cartography methods, and new ways of applying them, we have undertaken a comprehensive active measurement-driven study of the topology of U.S. regional access ISPs.
We used state-of-the-art approaches in various combinations to accommodate the geographic scope, scale, and architectural richness of U.S. regional access ISPs.
In addition to vantage points from research platforms, we used public WiFi hotspots and public transit of mobile devices to acquire the visibility needed to thoroughly map access networks across regions.
We observed many different approaches to aggregation and redundancy, across links, nodes, buildings, and at different levels of the hierarchy.
One result is substantial disparity in latency from some Edge COs to their backbone COs, with implications for end users of cloud services.
Our methods and results can inform future analysis of critical infrastructure, including resilience to disasters, persistence of the digital divide, and challenges for the future of 5G and edge computing.
</details>

<details>
<summary><b>Resources</b></summary>

[Paper Website](https://catalog.caida.org/details/paper/2021_inferring_regional_access_network_topologies/) <br />
[IMC 2021 Paper](https://www.caida.org/catalog/papers/2021_inferring_regional_access_network_topologies/inferring_regional_access_network_topologies.pdf) <br />
</details>

## Inferring Cloud Interconnections: Validation, Geolocation, and Routing Behavior [PAM 2021]
Authors: **Alexander Marder**, kc claffy, Alex C. Snoeren

Early work trying to interpret traceroutes from large public cloud providers with global WANs.
Intended to start a larger research effort, we improved bdrmapIT's accuracy for traceroute paths from clouds, analyzed differences across geographic regions, and geolocated interconnections between cloud providers.

<details>
<summary><b>Abstract</b></summary>

Public clouds fundamentally changed the Internet landscape, centralizing traffic generation in a handful of networks.
Internet performance, robustness, and public policy analyses struggle to properly reflect this centralization, largely because public collections of BGP and traceroute reveal a small portion of cloud connectivity.

This paper evaluates and improves our ability to infer cloud connectivity, bootstrapping future measurements and analyses that more accurately reflect the cloud-centric Internet.
We also provide a technique for identifying the interconnections that clouds use to reach destinations around the world, allowing edge networks and enterprises to understand how clouds reach them via their public WAN.
Finally, we present two techniques for geolocating the interconnections between cloud networks at the city level that can inform assessments of their resilience to link failures and help enterprises build multi-cloud applications and services.
</details>

<details>
<summary><b>Resources</b></summary>

[PAM 2021 Paper](data/pam21/cloud.pdf)
</details>

## Learning to Extract and Use ASNs in Hostnames [IMC 2020]
Authors: Matthew Luckie, **Alexander Marder**, Marianne Fletcher, Bradley Huffaker, kc claffy

One major problem with inferring router operators is the lack of validation information available.
We used bdrmapIT's inferences as input to a machine learning algorithm to extract AS operator information from DNS hostnames.
This can provide much greater breadth to router operator validation.

<details>
<summary><b>Abstract</b></summary>

We present the design, implementation, evaluation, and validation of a system that learns regular expressions (regexes) to extract Autonomous System Numbers (ASNs) from hostnames associated with router interfaces.
We train our system with ASNs inferred by RouterToAsAssignment and bdrmapIT using topological constraints from traceroute paths, as well as ASNs recorded by operators in PeeringDB, to learn regexes for 206 different suffixes.
Because these methods for inferring router ownership can infer the wrong ASN, we modify bdrmapIT to integrate this new capability to extract ASNs from hostnames.
Evaluating against ground truth, our modification correctly distinguished stale from correct hostnames for 92.5% of hostnames with an ASN different from bdrmapIT’s initial inference.
This modification allowed bdrmapIT to increase the agreement between extracted and inferred ASNs for these routers in the January 2020 ITDK from 87.4% to 97.1% and reduce the error rate from 1/7.9 to 1/34.5.
This work presents a new avenue for collecting validation data, opening a broader horizon of opportunity for evidence-based router ownership inference.
</details>

<details>
<summary><b>Resources</b></summary>

[Paper website](https://www.caida.org/publications/papers/2020/learning_extract_use_asns/) <br />
[IMC 2020 Paper](https://www.caida.org/publications/papers/2020/learning_extract_use_asns/learning_extract_use_asns.pdf) <br />
[IMC 2020 Presentation](https://www.youtube.com/watch?v=SuUoSxsjp9s) <br />
</details>

## Alias Pruning by Path Length Estimation (APPLE) [PAM 2020]
Authors: **Alexander Marder**

APPLE is a new alias resolution technique that uses pings from many vantage points to group together addresses they belong to the same routers.
This is not the expected final product, but a proof of concept that the technique has merit.

<details>
<summary><b>Abstract</b></summary>

Uncovering the Internet’s router graph is vital to accurate measurement and analysis.
In this paper, we present a new technique for resolving router IP aliases that complements existing techniques.
Our approach, Alias Pruning by Path Length Estimation (APPLE), avoids relying on router manufacturer and operating system specific implementations of IP.
Instead, it filters potential router aliases seen in traceroute by comparing the reply path length from each address to a distributed set of vantage points.

We evaluated our approach on Internet-wide collections of IPv4 and IPv6 traceroutes.
We compared APPLE’s router alias inferences against router configurations from two R&E networks, finding no false positives.
Moreover, APPLE’s coverage of the potential alias pairs in the ground truth networks rivals the current state-of-the-art in IPv4, and far exceeds existing techniques in IPv6.
We also show that APPLE complements existing alias resolution techniques, increasing the total number of inferred alias pairs by 109.6% in IPv4, and by 1071.5% in IPv6.
</details>

<details>
<summary><b>Resources</b></summary>

[PAM 2020 Paper](data/apple/apple.pdf) <br />
[PAM 2020 Presentation](https://www.youtube.com/watch?v=GU_MJQGYXFQ) <br />
[Github Repository](https://github.com/alexmarder/apple)
</details>

## vrfinder: Finding Outbound Addresses in Traceroute [SIGMETRICS 2020]
Authors: **Alexander Marder**, Matthew Luckie, Bradley Huffaker, kc claffy

Finds outbound addresses (usually caused by L3VPNs) in traceroute paths.

<details>
<summary><b>Abstract</b></summary>

Current methods to analyze the Internet’s router-level topology with paths collected using traceroute assume that the source address for each router in the path is either an inbound or off-path address on each router.
In this work, we show that outbound addresses are common in our Internet-wide traceroute dataset collected by CAIDA’s Ark vantage points in January 2020, accounting for 1.7% – 5.8% of the addresses seen at some point before the end of a traceroute.
This phenomenon can lead to mistakes in Internet topology analysis, such as inferring router ownership and identifying interdomain links.
We hypothesize that the primary contributor to outbound addresses is Layer 3 Virtual Private Networks (L3VPNs), and propose vrfinder, a technique for identifying L3VPN outbound addresses in traceroute collections.
We validate vrfinder against ground truth from two large research and education networks, demonstrating high precision (100.0%) and recall (82.1% – 95.3%).
We also show the benefit of accounting for L3VPNs in traceroute analysis through extensions to bdrmapIT, increasing the accuracy of its router ownership inferences for L3VPN outbound addresses from 61.5% – 79.4% to 88.9% – 95.5%.
</details>

<details>
<summary><b>Resources</b></summary>

[SIGMETRICS 2020 Paper](data/vrfinder/vrfinder.pdf)<br />
[SIGMETRICS 2020 Presentation](https://www.youtube.com/watch?v=P9jrEz2trJs)
</details>

## Pushing the Boundaries with bdrmapIT: Mapping Router Ownership at Internet Scale [IMC 2018]
Authors: **Alexander Marder**, Matthew Luckie, Amogh Dhamdhere, Bradley Huffaker, kc claffy, Jonathan M. Smith

<tt>bdrmapIT</tt> creates accurate maps of the Internet's graph.
It uses traceroutes from any number of vantage points and identifies the AS operator for every router interface address seen in the tracroute dataset.

<details>
<summary><b>Abstract</b></summary>

Two complementary approaches to mapping network boundaries from traceroute paths recently emerged.
Both approaches apply heuristics to inform inferences extracted from traceroute measurement campaigns.
[bdrmap](https://www.caida.org/publications/papers/2016/bdrmap/) used targeted traceroutes from a specific network, alias resolution probing techniques, and AS relationship inferences, to infer the boundaries of that specific network and the other networks attached at each boundary.
[MAP-IT](#map-it) tackled the ambitious challenge of inferring all AS-level network boundaries in a massive archived collection of traceroutes launched from many different networks.
Both were substantial contributions to the state-of-the-art, and inspired a collaboration to explore the potential to combine the approaches.
We present and evaluate bdrmapIT, the result of that exploration, which yielded a more complete, accurate, and general solution to this persistent and central challenge of Internet topology research.
bdrmapIT achieves 91.8%-98.8% accuracy when mapping AS boundaries in two Internet-wide traceroute datasets, vastly improving on MAP-IT’s coverage without sacrificing bdrmap’s ability to map a single network.
</details>

<details>
<summary><b>Resources</b></summary>

[IMC 2018 Paper]((data/bdrmapit/bdrmapit_paper.pdf))<br />
[IMC 2018 Slides](data/bdrmapit/bdrmapit_slides.pdf)<br />
[Github Repository](https://github.com/alexmarder/bdrmapit)
</details>

## MAP-IT: Multipass Accurate Passive Inferences from Traceroute [IMC 2016]
Authors: **Alexander Marder**, Jonathan M. Smith

A constant challenge to both researchers and network diagnosticians is identifying AS boundaries in traceroute data.
We provide the MAP-IT algorithm for doing so that is highly precise and is able to identify most inter-AS links that are revealed through traceroute.

<details>
<summary><b>Abstract</b></summary>

Mapping the Internet at scale is increasingly important to network security, failure diagnosis, and performance analysis, yet remains challenging.
Accurately determining the interface IP addresses used for inter-AS links from traceroute traces can be hard because these interfaces are often assigned addresses from neighboring ASes.
Identifying these interfaces can benefit Internet researchers and network diagnosticians by providing accurate IP-to-AS mappings where such mapping is most difficult - at AS boundaries.

We describe a new algorithm, Multipass Accurate Passive Inferences from Traceroute (MAP-IT), for inferring the exact interface addresses used for point-to-point inter-AS links, as well as the specific ASes involved.
MAP-IT combines evidence of an AS switch from distinct traceroute traces; using traceroute data makes it portable across IP networks.
Each pass leverages prior inferences to refine existing inferences and to discover additional inter-AS link interfaces.

We test MAP-IT with interface-level ground truth information from Internet2, achieving 100% precision.
Using approximate ground truth from Level 3 and TeliaSonera yields 95.0% precision.
These results suggest that MAP-IT is sufficiently reliable for network diagnostics.
</details>

<details>
<summary><b>Resources</b></summary>

[IMC 2016 Paper](data/mapit/mapit_paper.pdf)<br />
[IMC 2018 Slides](data/mapit/mapit_imc_slides.pdf)<br />
[Github Repository](https://github.com/alexmarder/MAP-IT)
</details>

# Other Recorded Presentations
EuroIX presentation of preliminary research in to how public clouds (Amazon AWS, Microsoft Azure, and Google Cloud) use IXPs.
<details>
<summary><b>Resources</b></summary>

YouTube Link: [https://www.youtube.com/watch?v=_KMiLnjFrSQ](https://www.youtube.com/watch?v=_KMiLnjFrSQ)<br />
Video Download: [How Do Clouds Use IXPs?](data/euroix/how_do_clouds_use_ixps.mkv)
</details>
