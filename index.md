---
title: Alex Marder
---

[//]: # (*Still a work in progress*)

<img src="assets/alexander_marder.jpg" align="right">

* [News](#news)
* [Background](#background)
* [Research Interests](#research-interests)
* [Current Research](#current-research-efforts)
* [Prior Research](#prior-research)
* [Actively Maintained Software](#actively-maintained-software)

# News
* August 2022 - NSF medium ($1,200,000) awarded to [bottlenecks in the cloud-centric Internet](#nsf-cns-medium-detection-and-analysis-of-infrastructure-bottlenecks-in-a-cloud-centric-internet-1200000)
* July 2022 - Paper accepted to [USENIX Security 2023!](#access-denied-assessing-physical-risks-to-internet-access-networks-usenix-security-2023)
* June 2022 - NSF/DOD convergence accelerator ($750,000) awarded [securely operating through 5G networks](#nsf-convergence-accelerator-2022-joint-nsfdod-phase-1)

# Background
I'm currently a research scientist at CAIDA/UCSD focusing on analyzing and improving the security, resiliency, and performance of the Internet through empirical measurements.
I completed a postdoc at CAIDA/UCSD in 2020 and I received my PhD at the University of Pennsylvania in 2019.
I can be reached at amarderATcaidaDOTorg.

My CV can be found here: [CV](data/app/cv_amarder.pdf)

# Research Interests
* Evaluating and improving the security and resilience of communication networks
* Using data science to reveal and measure performance characteristics of networks
* Identifying common failure modes for distributed and replicated applications


[//]: # (* [Research Statement]&#40;data/app/statement.pdf&#41;)

[//]: # (* [Teaching Statement]&#40;data/app/teachstate.pdf&#41;)

[//]: # (* [Inclusion and Diversity Statement]&#40;data/app/divstate.pdf&#41;)

[//]: # (Site anchors:)

[//]: # (* [Research]&#40;#research&#41;)

[//]: # (* [Other Recorded Presentation]&#40;#other-recorded-presentations&#41;)

# Current Research Efforts
## NSF Convergence Accelerator 2022 Joint NSF/DOD Phase 1
### 5G Traffic Sovereignty: Operating Through an Adversarial Internet ($750,000)
#### *Alexander Marder (PI)*, Ricky Mok (Co-PI), kc claffy (Co-PI)
This is one of 16 commercial or university-led projects funded in response to the joint solicitation by NSF and DOD to allow DOD operators to securely communicate with 5G devices in commercial networks.
Our project synthesizes recent advances in Internet measurement and programmable data planes to automatically send traffic along verified safe paths.

<details>
<summary><b>Project description</b></summary>

5G wireless technology has the potential to transform DOD mission-critical operations, but taking full advantage of this opportunity requires new techniques to operate through commercial networks worldwide.
Connecting mission-critical devices to commercial 5G networks will transform DOD communications, but it also increases the attack surface for sensitive and critical communications by exposing the traffic to the Internet at large.
Nation-states have nearly inexhaustible resources to disrupt traffic or passively recognize communications patterns via network infrastructure under their control, and the verified-trust paradigm in a zero-trust architecture cannot prevent these attacks.
Any secure communication solution in the 5G space must account for adversarial Internet paths that traverse networks and routers that are potentially controlled by adversary nation-states.
In essence, operating through 5G networks requires not just focusing on the wireless last hop, but also the Internet paths to reach the last hop.

This project combines three components to create an unprecedented ability to leverage commercial 5G networks for secure and resilient communication.
The first component takes advantage of programmable data planes to facilitate path measurements – and shift communications onto trustworthy paths – without modifying DOD applications, existing network devices, or third-party networks.
Component 2 creates an automated measurement application that interfaces with the router from Component 1 to identify router-level paths that avoid adversaries, as well as verify in real-time that communication paths for active flows behave as expected.
Component 3 will recommend ways for DOD to expand the availability of secure communication paths to 5G networks.
This last component will identify high-value networks whose inclusion in an industry zone-of-trust could benefit DOD, and apply existing geopolitical influence frameworks to evaluate trustworthy communication paths between DOD and geographic regions.

Tackling this problem requires convergence research across six areas of expertise: network measurement for path assessment; 5G communication and transport; programmable switch implementation; realistic evaluation platforms; security constraints of 5G-connected infrastructure; and geopolitical influence and strategy in the cyber domain.
This interdisciplinary and cross-sector collaboration targets a persistently unsolved challenge that the 5G ecosystem amplifies in importance: automatic selection of communication paths with 5G devices to avoid networks, locations, or hardware potentially controlled by a nation-state adversary.
This project will provide broad impact by complementing zero-trust architectures and secure 5G implementations, and by offering a transformative approach to how DoD and critical infrastructure can operate through the exploding yet dangerously opaque 5G ecosystem.
</details>

## Analyzing the Performance of the Cloud-Centric Internet
The shift to running user-facing applications in the public cloud providers requires us to similarly shift measurement focus to the cloud networks.
But, the cloud also provides the unprecedented opportunity to colocate our measurement infrastructure in the same data centers and networks as popular applications.
These project address our current shortcomings in empirical measurements and take advantage of the enormous opportunity that public cloud afford performance analyses.

### NSF CNS Medium: Detection and Analysis of Infrastructure Bottlenecks in a Cloud-Centric Internet ($1,200,000)
#### Ricky Mok (PI), *Alexander Marder (Co-PI)*, kc claffy (Co-PI)
<details>
<summary><b>Project description</b></summary>

The CoVID-19 pandemic and associated quarantine has accelerated the Internet’s fundamental shift from a peer-to-peer to a cloud-centric model.
Our entire lives have moved online, now predominantly mediated by services in the cloud, and public clouds are rapidly evolving to meet increasing requirements and demands from customers and end users.
The importance of the clouds in the modern Internet triggers questions regarding how well existing Internet backbone networks support the applications and content now served from the clouds.
Cloud providers can afford the infrastructure upgrades to support the needs of low latency or high throughput applications, but their ability to adapt infrastructure to application demands ends at their network border.
The economics of deploying and operating transit backbone infrastructure combine with the surge in traffic toward cloud services to induce performance bottlenecks in the changing Internet landscape.

This project proposes an ambitious effort to design measurement and analysis tools that can transform our understanding of cloud connectivity performance and reachability in the U.S. and around the world.
Researchers currently lack the measurement ability to even identify such bottlenecks at scale, much less assess their impact on Internet users.
The project is structured as two tasks that will combine to reveal performance bottlenecks outside the cloud networks where the high cost of deployment and operations leads to infrastructure bottlenecks for cloud applications.
The first task will develop novel techniques to identify performance bottleneck links between cloud datacenters and thousands of publicly accessible speed test servers, by synthesizing active measurements with TCP flows.
The second task will analyze the bottleneck links we identify with comprehensive path measurements from cloud datacenters to the entire public Internet, and we will develop new techniques to support inference of the geographic locations of bottleneck links by geolocating where paths exit cloud networks.

The intellectual merit of this project stems from the innovative methods we will develop and validate to conduct accurate, scalable, and reliable topology and performance measurements of a critical component of the modern Internet, overcoming cost barriers that have prevented measurement studies from the cloud.
The measured features and labels the project generates will provide an ideal basis to address the persistent challenge in applying machine learning techniques to network infrastructure research.
The project will also have broader impacts outside of the scientific research agenda.
The tools and data the project generates will be valuable to enterprises and application developers deploying into the cloud, as well as policy-makers seeking to understand bottlenecks in U.S. Internet infrastructure.
The data, tools, and analyses can also lead to the discovery of broadband performance inequities in the U.S. and inform future public investment in infrastructure.
Experience with cloud applications and measurements will be incorporated into an undergraduate data science course and undergraduate research mentorships.
</details>

### NSF CRII: Measurement Capabilities for the Modern Internet ($175,000)
#### *Alexander Marder* (PI)
<details>
<summary><b>Project description</b></summary>

The growing deployment of low-latency and high-throughput applications, the upfront and maintenance costs of computing resources, and constantly evolving security threats make it increasingly complex and costly for organizations to host services and applications themselves.
Public cloud providers, like Amazon AWS, Microsoft Azure, and Google Cloud Platform (GCP), ease that burden by allowing organizations to build and scale their applications on networks and hardware managed by the cloud provider.
As applications shifted into the clouds, the Internet fundamentally changed from peer-to-peer to a cloud-centric model.

The importance of the clouds in the modern Internet necessitates understanding the paths between cloud applications and users to better inform public policy and network operations, and we propose an ambitious effort to directly observe and interpret these cloud application paths at the router level.
We will not attempt to guess the paths that clouds use to reach end-hosts; instead, we will observe the router paths used by public cloud wide area networks (WANs) through comprehensive probing from our virtual machines (VMs).
By extending our recent techniques to cloud networks, we can create maps containing the paths from each cloud region to every corner of the Internet, along with the network operator for every observed router IP address.
These maps can provide edge network operators with the paths that clouds use to reach their networks, helping them diagnose problems, plan network improvements, and choose primary or backup providers.
In the future, we plan to leverage the annotated topology maps that we generate to conduct thirdparty analysis of cloudWANs, such as detecting the location of congestion or packet loss between clouds and users.

We will also use the map of the topology visible from our cloud VMs to interpret paths observed in the reverse direction, from end-hosts to the cloud.
Identifying the router operators in an individual path measurement from an arbitrary end-host is notoriously difficult due to the lack of information to constrain inference, but fitting these paths to our preprocessed map can provide the constraints needed for interpretation.
Our partial solution to this decades-old problem will allow network operators to understand their paths to cloud applications, and is of particular importance when comprehensive probing is impractical, such as from mobile devices.
</details>

### Papers
#### Inferring Cloud Interconnections: Validation, Geolocation, and Routing Behavior [PAM 2021]
**Alexander Marder**, kc claffy, Alex C. Snoeren

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

### Invited Talk
EuroIX invited me to present preliminary research into how large public clouds (Amazon AWS, Microsoft Azure, and Google Cloud) use IXPs around the world.
I provided an overview of how the clouds appear to fit into the peering strategies for the different clouds.
<details>
<summary><b>Resources</b></summary>

YouTube Link: [https://www.youtube.com/watch?v=_KMiLnjFrSQ](https://www.youtube.com/watch?v=_KMiLnjFrSQ)<br />
Video Download: [How Do Clouds Use IXPs?](data/euroix/how_do_clouds_use_ixps.mkv)
</details>


# Prior Research
## Security and Resilience of U.S. Broadband Internet Access Networks
On December 25, 2020, a bomb exploded in downtown Nashville, TN that exposed critical weaknesses in U.S. Internet infrastructure deployments.
The explosion damaged a single network facility, but disconnected an entire Internet access network covering Nashville and Middle Tennessee.
The outage revealed a single point of failure for the Nashville access network, but state of the art network measurement tools were insufficient to identify other weaknesses in access network infrastructure around the country.

We independently evaluated the resilience and security of the access network infrastructure in the U.S.
First, we analyzed the resilience of the access network infrastructure to common failure modes, finding that although much of the infrastructure is robust, single points of failure exist throughout the country.
Second, we examined the potential for intentional attacks against the infrastructure, showing that an attacker can gain sufficient knowledge of the access networks to induce outages in neighborhoods, cities, or entire states without any insider information.
Finally, we presented our discussions with broadband access network operators to facilitate future research into increasing the resilience and security of these critical networks.

### Papers
#### Access Denied: Assessing Physical Risks to Internet Access Networks [Usenix Security 2023]
**Alexander Marder**, Zesen Zhang, Ricky Mok, Ramakrishna Padmanabhan, Bradley Huffaker, Matthew Luckie, Alberto Dainotti, kc claffy, Alex C. Snoeren, Aaron Schulman

<details>
<summary><b>Abstract</b></summary>

Regional access networks play an essential role in connecting both wireline and mobile users to the Internet.
Today’s access networks support 5G cellular phones, cloud services, hospital and financial services, and remote work essential to the modern economy.
Yet long-standing economic and architectural constraints produce points of limited redundancy that leave these networks exposed to targeted physical attacks resulting in widespread outages.
This risk was dramatically shown in December 2020, when a bomb destroyed part of AT&T’s regional access network in Nashville, Tennessee disabling 911 emergency dispatch, air traffic control, hospital networks, and credit card processing, among other services.

We combine new techniques for analyzing access-network infrastructure deployments with measurements of large-scale outages to demonstrate the feasibility and quantify potential impacts of targeted attacks.
Our study yields insights into physical attack surfaces and resiliency limits of regional access networks.
We analyze potential approaches to mitigate the risks we identify and discuss drawbacks identified by network operators.
We hope that our empirical evaluation will inform risk assessments and operational practices, as well as motivate further analyses of this critical infrastructure.
</details>

<details>
<summary><b>Resources</b></summary>

[USENIX Security 2023 Paper](data/usenixsec23/outagesec.pdf) <br />
</details>

#### Inferring Regional Access Network Topologies: Methods and Applications [IMC 2021]
Zesen Zhang, **Alexander Marder**, Ricky Mok, Bradley Huffaker, Matthew Luckie, kc claffy, Aaron Schulman

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
[IMC 2021 Paper](data/imc21/inferring_regional_access_network_topologies.pdf) <br />
</details>

## Interpreting Router Interface Hostnames

[//]: # (The ability to accurately geolocate network infrastructure could unlock new empirical analyses, network management approaches, and facilitate diagnostic efforts, but geolocating network infrastructure in third-party networks remains a stubborn challenge.)

DNS hostnames associated with router interfaces provide a potential goldmine for researchers, network operators, and application developers.
Until recently, the state of the art was either manual interpretation or inaccurate and incomplete automated interpretation.
None of the approaches reached the level of scale, recency, or accuracy required to provide reliable information for emirical analyses.

We applied a machine learning framework to create regular expressions capable of extracting two type of information from router interface hostnames.
First, we applied the framework to the problem of recognizing and interpreting AS numbers and names that operators embed into hostnames to signal interconnection with a neighboring network.
We trained the model using output from bdrmapIT (discussed below), and extended bdrmapIT to incorporate the output from our model into its inference engine.
Second, we used the framework to geolocate Internet routers, a much more ambitious effort since operators embed many different types of geographic codes in hostnames and we could not find reliable ground truth for training.

### Papers
#### Learning to Extract and Use ASNs in Hostnames [IMC 2020]
Matthew Luckie, **Alexander Marder**, Marianne Fletcher, Bradley Huffaker, kc claffy

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

#### Learning Regexes to Extract Network Names from Hostnames [AINTEC 2021]
Matthew Luckie, **Alexander Marder**, Bradley Huffaker, kc claffy

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

#### Learning to Extract Geographic Information from Internet Router Hostnames [CoNEXT 2021]
Matthew Luckie, Bradley Huffaker, **Alexander Marder**, Zachary Bischof, Marianne Fletcher, kc claffy

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

## Internet Cartography
Much of my research focuses on creating accurate and comprehensive maps of the Internet's router-level graph to support other analyses by myself and other researchers, with a special focus on the router-level interconnections between Internet networks.
The motivation behind this work dates back to peering wars between transit providers and eyball networks (e.g., Level3 and Comcast) and my interest in DDoS attacks against the interconnections.
Currently, this work supports nearly all of my research efforts.

### Papers

#### Alias Pruning by Path Length Estimation (APPLE) [PAM 2020]
**Alexander Marder**

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

#### vrfinder: Finding Outbound Addresses in Traceroute [SIGMETRICS 2020]
**Alexander Marder**, Matthew Luckie, Bradley Huffaker, kc claffy

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

#### Pushing the Boundaries with bdrmapIT: Mapping Router Ownership at Internet Scale [IMC 2018]
**Alexander Marder**, Matthew Luckie, Amogh Dhamdhere, Bradley Huffaker, kc claffy, Jonathan M. Smith

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

[IMC 2018 Paper](data/bdrmapit/bdrmapit_paper.pdf)<br />
[IMC 2018 Slides](data/bdrmapit/bdrmapit_slides.pdf)<br />
[Github Repository](https://github.com/alexmarder/bdrmapit)
</details>

#### MAP-IT: Multipass Accurate Passive Inferences from Traceroute [IMC 2016]
**Alexander Marder**, Jonathan M. Smith

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

# Actively Maintained Software
As part of my research efforts, I often release open-source software that I continue to maintain.

* [bdrmapIT](https://gitlab.com/alexander_marder/bdrmapit) - determines router ownership and identifies router-level interconnections between networks
* [traceutils2](https://gitlab.com/alexander_marder/traceutils2) - utilities for parsing traceroute output
* [ip2as](https://github.com/alexmarder/ip2as) - create prefix-to-AS mapping that incorporates BGP announcements, IXP prefixes, RIR delegations, and WHOIS registrations
* [cloudtrace](https://gitlab.com/alexander_marder/cloudtrace/) - modified traceroute that reduces noise in the output caused by path changes
