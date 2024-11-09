# PDU session Attributes:
* Now , in the 5G the PDU session establishement is not a part of the UE registeration procedure , it can be register but can be without the a PDU session .
* Important PDU session Attribute :
* First is the PDU session ID , where each PDU session must have a PDU session ID .
* Second , we have the PDU session type , which can be IPv4 type , in this case ,the PDU session, the 5g network assignes the IPv4 type to the UE , and more preicisouly the SMF assignes the IPv4 , IP to ue , in the cas eof IPv4v6 the SMF assignes two IP addresses  to the UE , one is the IPv4 and other is the IPv6 , the most common PDU session types are IPv4 and IPv6 .
* These PDU session types have some problem , when we are using it in the IP Header , there is the Source header and the IP destination address in the IP packes and as a result this increases the size of the IP header for the solution of this 3GPP has purposed the work round  and as the solution they purpose the ethernet PDU session type, we do not use the  IP header , rather we use the MAC addresses, as the source an dthe destination addressses, for the transfer of data through the PDU sesseion , and in the case, of ethernet PDU session , the SMF does not assign any ethernet or ,MAC address to the UE, rather it is the UE provides it own ethernet and MAC address to the SMF , then SMF uses this MAC address in order to establish the PDU session .
* Then we have the unstructured PDU session type , it is rarely used , and this type is used in the cases when network does not have knowledge , that what type of protocol is being used at the application layer of this PDU session , and this case of PDU session , SMF does not assign the IP or the MAC address to the UE, rather the transfer of data is using the local tunneling msg . This type of PDU session has a limitation where it has only one QoS flow per PDU session .
* Another important attribute , is the Data Network Name , it is the name of the data network from  which this PDU session is connected , and we have the   Network Slice also.

# QoS flows in PDU Sessions
* In a PDU session there may be one or more QoS flows present , each of these QoS flows are characterised by the QoS rules.
* QoS flow Identifier ( QFI ) , which is unique inside the PDU session, it has QoS rules Identifiers which is also unique in PDU session
* Packet Filter Set , they are installed inside the UPF , in the Core network and inside the UE , and there purpose is to bind the respective packets to there corresponding QoS flow.
* QoS parameters for the QoS rules.

# PDU session states :
* Now a PDU session can be in the two states, if the UE is in the CM-Connected state and it is in the PDU session , then this PDU session is in the active state, and if the UE enters in the CM-IDLE state, and it still has the PDU session , then this PDU session became Inactive .
*  ## Active PDU session:
*  When a PDU session is in the Active state it consist of three sub bearers,
*  1st Data Radio Bearer
*  2nd N3 Tunnel if there is only one UPF then there is only N3 Tunnel , if there is two UPF then there would be N9 Tunnel which is also present with the N3 Tunnel.
*  So the important parameters for these sub - bearer are called Beraer Context, it includes the ID of the Data Radio Bearer which is called as  the Data Radio Bearer ID (DRB-ID) , then the ID's of the N3 and N9 End points are also there and the IP address that has been assign to the UE for this PDU session .
*  These Beraer Context must be stored in the UPF, AMF , gNB and  UE for the activation of the PDU session.

* ## Inactive PDU session:
* Now if no data transfer through a PDU session for a certain time , then the Inactivity timer that is assoigned to this PDU session get expires and this PDU session enters in the Inactive state , and this is done to prolong the battery life of the UE .
* While in the Inactive PDU session , the Data Radio Bearer and N3 Tunnel is release and the N9 Tuneel deactivation is optional , now in the Inactive state PDU session there is the incomming data to the UE , that data would be store in the anchor UPF, however the Bearer Context are stored in the UE, AMF ,UPF and gNB or we can say retain there
* Whenever the UE or the AMF , requires to reactivate this PDU session , then it can easily done using the Bearer  Context .

# Two Types of QoS Flows Guaranteed Bitrate And Non-guaranteed Bitrate :
* Inside the PDU session we can have two types of qos flows,
* 1st Guaranteed Bitrat QoS flows , for eg for the VOIP (Voice Over IP), required Guaranteed Bitrat qos flows,
* 2nd type Non-guaranteed Bitrate QoS Flows , for eg when we are doing web browesing , we do not need a Guaranteed Bitrat QoS flows , rather we can easlily do it Non-guaranteed Bitrate QoS Flows.
* ## QoS Parameters
* There are some specific parameters for each type of QoS flows,
* In GBR QoS Flow we have Guaranteed Flow Bit Rate(GFBR) ,Maximum Flow Bit Rate and Notification Control that are specfic for this QoS flow
* Then we have NGBR QoS flow, we have parameter like , Per Session Aggregate Maximum Bit Rate , Per UE Aggregate Maximum Bit Rate Reflective QoS Attribute that are required for the NGBR .
* Allocation and Retention Priority (ARP) and 5G QoS Identifier (5QI) these parameter are common in both QoS type.

# Allocation and Retention Priority (ARP) :
* During the busy period of the day there is the competition for the resource , in such situation 5GC will use ARP , in order which QoS flows will establish with higher ARP value and which QoS flows it would not establish because of the lower ARP value .
* In the case of traffic Overload , or in network conjuaction state , if some  QoS flow need to be drop , then those QoS flow will be drop first that have lower ARP value .
* ARP value are defines by the three priority :
* 1st ARP value , that is range of the 1-15 , where 1 means higher proiorty and 15 means lower priority .
* 2nd Pre-mption Capability : which is the Yes/No parameter, it means that whether other QoS flow that have a lower ARP , they can be drop QoS flow or not .
* 3rd Pre-mption Vunerablility : it defines whether this QoS flow can be drop in favour of other QoS flow , that have a higher ARP value Yes/No
* Now the ARP parameter value for the specific subscriber is stored in the UDM , and form the UDM they are given to the SMF and how there ARP parameter  would be used are defined by the Genral ARP policy network , this policy is defined in the PCF , and SMF takes inputs form the UDM and PCF and based upon these inputs , it decides which QoS flow is to be created , and in order to create a QoS flow the SMF needs to coordinate with the AMF and the UPF.

# 5G QoS Identifier :
* There is a 5G QoS Identifer associated with each QoS flow ,and this 5G QoS Identifier is the combination of the 6 parameters ,
* 1st Resource Type: it tells that this QoS flow it GBR , or delay critical GBR or non GBR .
* 2nd Default Priority Value for a QoS flow and the lower values means the higher priority , and this priority level is different from the ARP priority level , because this priority level is concerne how UPF , handles a pratcular QoS flow and what quality this UPF gives to the QoS flow .
* 3rd Packet Delay Budget (PDB) the 98% of packest in a QoS flow must have packet delay less than PDB .
* 4th Maximum Packet Error Rate that is allowed in the QoS flow .
* 5th Default Maximum data burst volume this is the amount of data that is transmitted  through  the QoS flow in the access network during the duration of the packet delay budget this paramter is only vaild when the PDB is less than 20 milli second ,if it exceeds the 20 milli sec then this parameter is no longer .
* 6th Averaging window it is the time duration over which GFBR & MFBR are calculated .
  ![2 (1)](https://github.com/user-attachments/assets/86d4d12a-bd66-48fd-a620-770ec6912250)

# GBR QoS flow Specific Parameters GFBR , MFBR , Notification Control:
* Guaranteed Flow Bit Rate(GFBR):this is the min data rate that the QoS flow should maintain.
* Maximum Flow Bit Rate : This is the max data rate that the QoS flow is allowed to use .
* Notification Control : it is used to indicate the Radio Access Network  , that if it is not able to maintain the GFBR then it should notify the SMF , about it.

# Non-GBR QoS flow Specific Parameters session-AMBR , UE-AMBR , RQA:
* Per Session Aggregate Maximum Bit Rate : for a particular PDU sesion this is the max data rate ,that all the UE's Non-GBR QoS flow inside the PDU session .
* Per UE Aggregate Maximum Bit Rate : For a particular UE it is the max total data rate that all of its Non-GBR QoS flow can use 
* Reflective QoS Attribute : it indicate whether the it reflect the QoS is enable for a particular QoS flow or not .

# Packet Filters :
* During the establishment of the PDU session , the packet filters are installed in the UPF in the network side ,and in the UE in the UE side , once a PDU session establish then we know that the Qos flows , are setup that are mapped to the Data Radio Bearers.
* The xn of the Packets filters is to identify the incomming data , that it belongs to which PDU session , and then these packet filter mapps them to there corresponding QoS flws by marking them with there QoS flow Id .
* How do these Packets Filters Identifies the traffic of a particular PDU session , they Identify the Traffic because of the source & destination IP addresses, source & destination port Number , and the layer 4 protocol that is being used these packet whether it is TCP or UDP .

# 5G Reflective QoS(RQoS):
* The purpose of the RQoS is to reducde the load of signaling on the 5G network , in a particular QoS flow the downlink QoS rule is used to send the down link data in the RQoS UE uses same down link QoS rule in order to send its Up link data , in other words the UE mirrors the DL rule as the UL rule , so there id no signaling requied in order to send the UL QoS rule form UE , so this reduces the load on the 5G .
* During the establishment of the PDU sessionthe UE indicates that whether it supports  the  RQoS or not , if it supports RQoS then network sets the RQA for this ODU session , and the network also provides the RQoS Timer to the UE .
* In order to trigger the RQoS for a particular QoS flow  the SMF signales to the UPF , and the UPF starts labling the DL packet of the QoS flows with a New QoS flow Indicator and RQoS Indicator  in these DL packets .
* When the UE recives these DL packets it create the uplink QoS rules based upon the DL QoS rule for this Qosflow and it uses the same QoS Flow Indicator for the UL packets of this  newly created for this UL flow ,  that is Indicated in the DL .
* The UE continues to send the UL packet for the newly created QoS flow as long as it continue to recives the DL packets with RQoS indicator as set .
* Once the UE stops reciving these packets , it waits for a time equal to the RQoS Timer , and once the RQoS Timer expires the UE delete this newly created QoS flow in the UL.
 























