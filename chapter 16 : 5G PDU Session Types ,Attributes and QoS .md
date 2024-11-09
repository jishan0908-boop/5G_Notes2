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
* In GBR QoS Flow we need Guaranteed
























