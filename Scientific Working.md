# Task: Research Existing Work
## Group
- Okpanachi Victor Fibechola (ID: 28012)
- Fatema Tuz Zuhora (ID: 27386)
- Md Samir Hossain (ID: 26770)
## Topic (Digital Voltmeter)
### 
[Link to paper]()
#### Answers:
##### Hypothesis:
##### Experiment:
##### Conclusion:

## Topic (Ethernet)
### Ethernet-Based Real-Time and Industrial Communications
[Link to paper](https://ieeexplore.ieee.org/abstract/document/1435741)
#### Answers:
##### Hypothesis:
This paper first details the requirements that an industrial network has to fulfill. It then shows how Ethernet has been enhanced to comply with the real-time requirements in particular in the industrial context. Finally, it shows how the requirements that cannot be fulfilled at layer 2 of the OSI model can be addressed in the higher layers adding functionality to existing standard protocols.
##### Experiment:
- **Modifications That Alter Compatibility**
In this paper it was focused on alterations to the IEEE 802.3 MAC that make the result incompatible with standard solutions. It was assumed that they can be implemented on off-the-shelf IEEE 802.3 compliant hardware.
Most of the modifications add a new MAC on top of CSMA/CD. All traffic, whether real time or not, is passed to the additional layer that controls the access to the medium. At a higher layer, real-time traffic is either handled by IP/UDP or by separate protocols.
Quite logically, all known types of deterministic MAC have been used. Examples are Time-Division Multiple Access (TDMA), master–slave, token passing , slot reservation , or time packet release . At the same time, some authors have suggested to reuse the MAC schemes of some fieldbuses such as PROFIBUS and WorldFIP on top of IEEE 802.3.
- **Modifications That Keep Compatibility**
Two subclasses are distinguished here 1. The homogeneous and 2. The heterogeneous one
  1. **Homogeneous Solution**
In the first approach, the network-wide limit was split statically to give limits for each individual station. Because this gives strong constraints at configuration time, the work has later been improved using adaptive schemes. The principle is to measure the workload of the network and adapt the limit accordingly. To evaluate the network load, two means have been proposed, measuring the collisions or the throughput during a given observation window. Based on this, the station limit may be increased by a fixed amount or decreased by half, harmonic increase multiply decrease (HIMD), as in. The limit may also be managed by a fuzzy controller that uses both the throughput and the collision rate as a measure. This policy gives better results than the simple HIMD scheme. This in particular due to the fact that HIMD uses only collisions as a measure and that collisions occur even in absence of overload.
  2. **Heterogenous Solution**
When a station wants to transmit real-time traffic to another one, it sets a connection via its real-time communication daemon (RTCD). A connection request with the destination node IP address is sent to the first switch. The request contains the QoS parameters (average bandwidth and maximum burst size) of the connection and a 16-bit connection identifier. If QoS can be guaranteed, the switch forwards the request to the next switch on the path and the process is repeated until the last switch (to which the destination node is directly connected) is reached. The destination node is not involved in the process, as real-time connections are simplex. If the last switch accepts the QoS requirements, it returns an acknowledgment to the previous switch. The acknowledgment propagates back to the initiating node. Each switch on the path sets up a “routing” entry with the connection identifier and the QoS needs. Note that the connection identifier is different on each point-to-point link and each switch makes a translation between the ingress identifier and the output identifier. In this way, it is easier to ensure that identifiers are unique for each link. The initiating node RTCD finally creates a proxy MAC address and a proxy IP address that contain the 16-bit connection identifier. It, then, uses the Address Resolution Protocol (ARP) cache deposit mechanism to bind the proxy MAC address to the proxy IP address.
The proxy IP address is used by the initiating node application when it wants to send a real-time packet on this connection. Real-time packets are sent using UDP. The IP layer uses ARP to find the corresponding proxy MAC address. This address is recognized by the first switch that uses its internal “routing” table to find the output link and QoS parameters. It also modifies the lower 16 bits of the proxy MAC address with the output connection identifier. The process is repeated until the destination node is reached.
Best effort traffic may use TCP or UDP. Switches will forward this traffic in a usual way (as would regular Ethernet switches do) without special guarantees. Proxy IP and Ethernet addresses are chosen carefully to avoid conflicts with existing networks.

##### Conclusion:
At the time of redaction of this paper, there are nearly a dozen proposals4 for an “industrial Ethernet” that supports real-time communications at the factory floor. Most of them are still maturing but it is likely that a number of them will coexist on the market. This paper has given the necessary background to judge and compare these proposals. The solution may come from the consumer market. With the evolution of the Internet toward higher QoS, particularly to support continuous media, voice, and images, the original 802.3 protocol has been enhanced and completed with new standards (priorities, switches, clock synchronization) that fill most of the requirements for an industrial solution. This solution has the advantage of being standard and recognized by most of the vendors. As a wireless extension with QoS is also available (IEEE802.11e), it may be the right choice.

## Topic (Light Emitting Diode)
### 
[Link to paper](https://www.researchgate.net/publication/265555804_Superconducting_Light-Emitting_Diodes)
#### Answers:
##### Hypothesis:
They proposed to clarify the concept of super conductiong LED and demonstrate how to convert Cooper pairs to entangled photon pairs via interband radiative recombination of Cooper pairs, penetrated into a semiconductor by the proximity effect. 
##### Experiment:
They fabricated a superconducting (SC)[^1] light emitting diode where a superconductor was used for the n-type electrode. luminescence in QDs was studied with photo-excited hole injection into QDs[^2]. In their experimental demonstrations, SC-LEDs (super conducting light emitting diodes with quantum well (QW) luminescent regions were employed and no signature of superconductivity was observed in their emission spectra. They studied the luminescence of Cooper pairs in InAs QDs and observed unusual “sharp edge” in the luminescence spectra, the signature of the SC density of states (DOS),for the first time.
###### Sample Preparation
For this purpose, a semiconductor heterostructure was grown on a (311)B InP substrate with molecular-beam epitaxy (MBE). The growth was initiated with 50-nm-thick In0.53Ga0.47As and 100-nm-thick In0.52Al0.48As layers for removal of the InP substrate with selective chemical etching. Then 200-nm-thick n-In0.53Ga0.25Al0.22As/ 20-nm-thick n-In0.53Ga0.35Al0.12As/ 5-monolayers (ML) of InAs QDs/ 100-nm-thick n-In0.53Ga0.35Al0.12As/ 10-nm-thickn-In0.53Ga0.47As layers were grown successively. The InAs QDs were grown at 530°C and the QD density was 3.4x1010 cm-2, and the average QD lateral size and height were 57 nm and 5.6 nm, respectively.
###### Measurement
The prepared sample was set in a liquid-helium cryostat and a He-Ne laser at the wavelength of 632.8 nm was focused on one of the pillar arrays embedded in the Nb/Ag metals with an objective lens (OL) with the numerical aperture of 0.42. Photoluminescence (PL) was collected with the same OL and was dispersed by a 50-cm double monochromator with 300-grooves-per-mm gratings and was detected with a liquid-nitrogen-cooled InGaAs-photodiode array detector. PL spectra measured on one of the pillar with the diameter of 1.5 m With the given QD density, this pillar includes ~600 QDs. Under the excitation power density of 600W/cm2, the PL spectra were measured at 4 K and 10 K, which are below and above the Nb Super Conducting Temperature of 9.0 K, respectively.
###### Observation
To examine the relation to the superconductivity, they plotted the QD luminescence intensity against the measured temperature. The Super conducting temperature (SC Tc), the luminescence intensity remained almost the same but it abruptly increased and saturated for the lower temperature. This correlation to the SC Tc also evidences the superconductivity effect. 

##### Conclusion:
They discussed the interactions of photons with superconductivity generally in relation to the photon energy  and the SC gap 2. Based on this, they clarified the concept of Super Conducting LED and demonstrated how Cooper pairs modify the photon generation processes in semiconductors.
Their measurements on Cooper-pair recombination in QDs are still preliminary, and further studies are under way. One important step is the observation of single QD luminescence to study the phenomena more in detail.
