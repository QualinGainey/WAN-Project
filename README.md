# Redundant Multi-Site WAN Network

## Project Overview

This Cisco Packet Tracer project simulates a WAN connecting two buildings. Each building uses redundant switching, gateway redundancy, VLAN segmentation, EtherChannel, trunking, and Layer 3 switching.

The next phase will connect the two buildings through a site-to-site IPsec tunnel.
<img width="1690" height="569" alt="image" src="https://github.com/user-attachments/assets/5256ae6c-1fd2-4e97-8265-cdc21ebd7e54" />
## Packet Tracer Lab File

[Download the Redundant Multi-Site WAN lab](./Redundant-Multi-Site-WAN.pkt)

> Cisco Packet Tracer is required to open the `.pkt` file.


## Project Status

**In progress**

### Completed

* Created and assigned VLANs
* Configured local device authentication
* Enabled PortFast and port security
* Configured Dynamic ARP Inspection
* Built EtherChannel and trunk connections
* Enabled Layer 3 switching and inter-VLAN routing
* Configured redundant connections between switches
* Implemented HSRP gateway redundancy
* Verified connectivity between endpoints

### Next Phase

* Configure WAN addressing and routing
* Build the connection between both buildings
* Configure the site-to-site IPsec tunnel
* Test encrypted communication between sites
* Perform redundancy and failover testing

## Technologies and Protocols

* Cisco Packet Tracer
* Cisco IOS
* VLANs
* 802.1Q trunking
* EtherChannel
* Inter-VLAN routing
* Switch Virtual Interfaces (SVIs)
* HSRP
* PortFast
* Port security
* Dynamic ARP Inspection
* IPv4 addressing
* LAN/WAN troubleshooting

---

## 1. VLAN and Device Access Configuration

I created local usernames and passwords on the switches. I also created the required VLANs and assigned endpoint-facing switch ports to the appropriate VLANs in both buildings.

<img width="1664" height="438" alt="VLAN and switch access configuration" src="https://github.com/user-attachments/assets/5eef2e76-32b5-48b7-bd19-1de2c227117a" />

<details>
<summary>View additional VLAN configuration screenshots</summary>

<img width="916" height="387" alt="VLAN configuration details" src="https://github.com/user-attachments/assets/7306a51e-71e4-4dd4-86ae-3e5be69ff9da" />

<img width="927" height="936" alt="Switch VLAN and interface configuration" src="https://github.com/user-attachments/assets/af450249-38a1-45e8-ba32-64ba68095e33" />

</details>

---

## 2. Access-Layer Security

I enabled PortFast on ports connected to end devices to allow them to transition into a forwarding state quickly.

I also configured port security so unauthorized MAC addresses trigger a switch-port violation. Dynamic ARP Inspection was enabled for the required VLANs to help protect the network against ARP spoofing attacks.

<img width="883" height="346" alt="PortFast and port security configuration" src="https://github.com/user-attachments/assets/15ad4893-aba2-422f-8517-2ddada43eff7" />

<details>
<summary>View additional access-layer security screenshots</summary>

<img width="672" height="343" alt="Port security verification" src="https://github.com/user-attachments/assets/a3d6e721-ae17-40c3-9991-02e0a0c047a7" />

<img width="879" height="407" alt="Dynamic ARP Inspection configuration" src="https://github.com/user-attachments/assets/0199f409-780e-4e23-9de8-188b1ba7447d" />

</details>

---

## 3. EtherChannel and Trunk Configuration

I configured EtherChannel and 802.1Q trunk links between the Layer 2 and Layer 3 switches. The appropriate VLANs were permitted across each trunk and EtherChannel connection.

I also enabled `ip routing` on the multilayer switches so they could perform Layer 3 routing.

<img width="813" height="618" alt="EtherChannel and trunk configuration" src="https://github.com/user-attachments/assets/137e5113-0954-4b29-94f5-e0dbc124308f" />

<details>
<summary>View additional EtherChannel and trunk screenshots</summary>

<img width="626" height="231" alt="EtherChannel status" src="https://github.com/user-attachments/assets/ee027050-c2e9-48a2-af60-b438474471ea" />

<img width="673" height="187" alt="Trunk verification" src="https://github.com/user-attachments/assets/72f30393-6fd1-4eae-aca3-47274bfb7ef8" />

<img width="660" height="220" alt="Allowed VLAN verification" src="https://github.com/user-attachments/assets/acc66a5e-623c-45fd-984f-b6b59d7f2e53" />

<img width="637" height="248" alt="Switch trunk configuration" src="https://github.com/user-attachments/assets/7e8d22a9-8d60-4eff-a605-ba4840acaa6e" />

<img width="665" height="272" alt="EtherChannel interface configuration" src="https://github.com/user-attachments/assets/7040d9f8-b860-4c15-87ac-d5dee1a05597" />

<img width="700" height="276" alt="EtherChannel verification output" src="https://github.com/user-attachments/assets/4c083a4f-f2e5-4bf7-9076-062571f255c7" />

</details>

---

## 4. Redundant Switching Links

I created additional EtherChannel and trunk connections between the four switches in each building. These connections provide redundant Layer 2 paths and help maintain network availability if an individual link fails.

<img width="632" height="223" alt="Redundant EtherChannel configuration" src="https://github.com/user-attachments/assets/e29dff9c-415c-4c1c-8379-b17be05b64e4" />

<details>
<summary>View additional redundancy screenshots</summary>

<img width="655" height="628" alt="Redundant switch connection configuration" src="https://github.com/user-attachments/assets/afcada98-9e14-4b1e-bb5a-a3c73bb8cd1e" />

<img width="676" height="613" alt="Redundant trunk configuration" src="https://github.com/user-attachments/assets/1dd7a66c-5acd-4f58-be70-1367aea9b94c" />

<img width="796" height="627" alt="Switch redundancy configuration" src="https://github.com/user-attachments/assets/d3c9e581-84d5-4fd4-beab-f10306426363" />

<img width="610" height="445" alt="Redundant switching verification" src="https://github.com/user-attachments/assets/3189a7b8-97e5-4ab7-8041-b5142b74c023" />

</details>

---

## 5. Layer 3 Switching and Inter-VLAN Routing

I configured EtherChannels and trunks on both Layer 3 switches. I then created SVIs to provide Layer 3 gateway services and route traffic between VLANs.

Connectivity was verified by sending pings between PCs in different VLANs.

<img width="822" height="415" alt="SVI and Layer 3 switching configuration" src="https://github.com/user-attachments/assets/9760c9e6-1e5c-49f6-b041-dd7c48ba3fb7" />

<details>
<summary>View routing and connectivity verification</summary>

<img width="871" height="292" alt="Inter-VLAN routing configuration" src="https://github.com/user-attachments/assets/77d0549c-814b-4c41-b4b4-a44b79e9905f" />

<img width="813" height="457" alt="SVI configuration details" src="https://github.com/user-attachments/assets/8c65c76b-6785-4fe4-85d6-24dc7feb434e" />

<img width="864" height="527" alt="Layer 3 connectivity testing" src="https://github.com/user-attachments/assets/7cbe39a3-8005-40b9-96af-0cb4baeb5dae" />

<img width="885" height="431" alt="Successful endpoint ping test" src="https://github.com/user-attachments/assets/125599ea-33c6-4267-adcf-48eda18d2641" />

</details>

---

## 6. HSRP Gateway Redundancy

I configured HSRP on both Layer 3 switches to provide redundant default gateways for the endpoint VLANs.

I verified the active and standby roles and updated the endpoint addressing so each PC used the appropriate HSRP virtual IP address as its default gateway. Connectivity was tested after the changes.

<img width="586" height="94" alt="HSRP active and standby status" src="https://github.com/user-attachments/assets/449254ec-5ab3-43e2-ac88-9c1c9531d230" />

<img width="579" height="109" alt="HSRP role verification" src="https://github.com/user-attachments/assets/3427caec-d5e5-46d8-9126-13f8fd85b3d4" />

<details>
<summary>View HSRP configuration and testing screenshots</summary>

<img width="676" height="573" alt="HSRP configuration" src="https://github.com/user-attachments/assets/70ff6fb9-aac0-4168-b1cb-fc73626061b1" />

<img width="704" height="460" alt="HSRP virtual gateway configuration" src="https://github.com/user-attachments/assets/cc38f049-ceb4-4f31-b168-a21808527a01" />

<img width="663" height="495" alt="Endpoint gateway configuration" src="https://github.com/user-attachments/assets/4ffdce76-a15b-406a-a41d-ac51d326872a" />

<img width="846" height="490" alt="Connectivity verification after HSRP configuration" src="https://github.com/user-attachments/assets/d06d2b3d-47d5-4e6f-a840-67cb989b45cb" />

</details>

---

## Skills Demonstrated

This project demonstrates hands-on experience with:

* Designing a redundant campus network
* Configuring and troubleshooting Cisco switches
* Segmenting networks with VLANs
* Building EtherChannel and trunk connections
* Implementing inter-VLAN routing with SVIs
* Securing access ports
* Implementing first-hop redundancy with HSRP
* Testing and validating end-to-end connectivity
* Documenting a network implementation in GitHub

## Planned Final Result

Once complete, the project will provide redundant LAN connectivity within both buildings and secure site-to-site communication across the WAN using an IPsec tunnel.
