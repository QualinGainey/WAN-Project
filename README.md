# WAN-Project
This project will consist of a WAN being created between two buildings and using a IPSec tunnel for connection between the two buildings. Each building will also provide redundancy.

I first created logins and usernames on the switches as well as created the correct VLANS and put the devices in the correct VLANS for each switch in both buildings 
<img width="1664" height="438" alt="Image" src="https://github.com/user-attachments/assets/5eef2e76-32b5-48b7-bd19-1de2c227117a" />

<img width="916" height="387" alt="Image" src="https://github.com/user-attachments/assets/7306a51e-71e4-4dd4-86ae-3e5be69ff9da" />

<img width="927" height="936" alt="Image" src="https://github.com/user-attachments/assets/af450249-38a1-45e8-ba32-64ba68095e33" />



- Then I enable portfast on all ports connected to end host for immediate connectivity as well as Port Security so that if an unknown MAC Address connects to that port then the port will shutdown. 
- Also Configured Arp inspection for each of the Vlans on each switch in both buildings
<img width="883" height="346" alt="Image" src="https://github.com/user-attachments/assets/15ad4893-aba2-422f-8517-2ddada43eff7" />

<img width="672" height="343" alt="Image" src="https://github.com/user-attachments/assets/a3d6e721-ae17-40c3-9991-02e0a0c047a7" />

<img width="879" height="407" alt="Image" src="https://github.com/user-attachments/assets/0199f409-780e-4e23-9de8-188b1ba7447d" />
 



- In this part of the project i have created a etherchannel and trunk link between each Layer 2 and Layer 3 switch
- As well as used the 'IP routing" command to ensure that they are able to preform routing 
- I Also made sure to allow the correct VLANS over each trunk/etherchannel
<img width="813" height="618" alt="Image" src="https://github.com/user-attachments/assets/137e5113-0954-4b29-94f5-e0dbc124308f" />

<img width="626" height="231" alt="Image" src="https://github.com/user-attachments/assets/ee027050-c2e9-48a2-af60-b438474471ea" />

<img width="673" height="187" alt="Image" src="https://github.com/user-attachments/assets/72f30393-6fd1-4eae-aca3-47274bfb7ef8" />

<img width="660" height="220" alt="Image" src="https://github.com/user-attachments/assets/acc66a5e-623c-45fd-984f-b6b59d7f2e53" />

<img width="637" height="248" alt="Image" src="https://github.com/user-attachments/assets/7e8d22a9-8d60-4eff-a605-ba4840acaa6e" />

<img width="665" height="272" alt="Image" src="https://github.com/user-attachments/assets/7040d9f8-b860-4c15-87ac-d5dee1a05597" />

<img width="700" height="276" alt="Image" src="https://github.com/user-attachments/assets/4c083a4f-f2e5-4bf7-9076-062571f255c7" /> 




- I have created more etherchannel and trunk links connecting all Four switches in each building for redundancy and routing/forwarding
<img width="632" height="223" alt="Image" src="https://github.com/user-attachments/assets/e29dff9c-415c-4c1c-8379-b17be05b64e4" />

<img width="655" height="628" alt="Image" src="https://github.com/user-attachments/assets/afcada98-9e14-4b1e-bb5a-a3c73bb8cd1e" />

<img width="676" height="613" alt="Image" src="https://github.com/user-attachments/assets/1dd7a66c-5acd-4f58-be70-1367aea9b94c" />

<img width="796" height="627" alt="Image" src="https://github.com/user-attachments/assets/d3c9e581-84d5-4fd4-beab-f10306426363" />

<img width="610" height="445" alt="Image" src="https://github.com/user-attachments/assets/3189a7b8-97e5-4ab7-8041-b5142b74c023" />



- Configured  both layer 3 switches with ethertchannels/trunks as well as coonfigured SVIs  so they can route 
- Confirmed the routing worked by pinging each PC
<img width="822" height="415" alt="Image" src="https://github.com/user-attachments/assets/9760c9e6-1e5c-49f6-b041-dd7c48ba3fb7" />

<img width="871" height="292" alt="Image" src="https://github.com/user-attachments/assets/77d0549c-814b-4c41-b4b4-a44b79e9905f" />

<img width="813" height="457" alt="Image" src="https://github.com/user-attachments/assets/8c65c76b-6785-4fe4-85d6-24dc7feb434e" />

<img width="864" height="527" alt="Image" src="https://github.com/user-attachments/assets/7cbe39a3-8005-40b9-96af-0cb4baeb5dae" />

<img width="885" height="431" alt="Image" src="https://github.com/user-attachments/assets/125599ea-33c6-4267-adcf-48eda18d2641" />



- Within my project i have no configured HSRP for gateway redundancy on the Layer 3 switches
- Also confirmed that the correct switches were Active/standby and confirmed connectivity of PCs
- Also changed the ips and default gateways of the pcs due to the changes i had to make for the VIP for HSRP
<img width="586" height="94" alt="Image" src="https://github.com/user-attachments/assets/449254ec-5ab3-43e2-ac88-9c1c9531d230" />

<img width="579" height="109" alt="Image" src="https://github.com/user-attachments/assets/3427caec-d5e5-46d8-9126-13f8fd85b3d4" />

<img width="676" height="573" alt="Image" src="https://github.com/user-attachments/assets/70ff6fb9-aac0-4168-b1cb-fc73626061b1" />

<img width="704" height="460" alt="Image" src="https://github.com/user-attachments/assets/cc38f049-ceb4-4f31-b168-a21808527a01" />

<img width="663" height="495" alt="Image" src="https://github.com/user-attachments/assets/4ffdce76-a15b-406a-a41d-ac51d326872a" />

<img width="846" height="490" alt="Image" src="https://github.com/user-attachments/assets/d06d2b3d-47d5-4e6f-a840-67cb989b45cb" />
