# VOICE OVER 5G :
* In the case of the 5G the voice over service is provided based on the IMS ( IP Multimedia Subsystem ) , IMS was launched as the part of the 3G , to provide the voice over IP service .
The same IMS was used over the LTE on the VoLTE, therefore this IMS is going to use in the 5G for the voice call.
For 5G there are two major solution :
1. Voice over 5G system that means , that the core network and the acces network , of the 5G system use for a voice call , if a mobile is in the 5G call and it moves from the to non 5G network , then there is the  procedure
2. EPS Fallback procedure : that means that UE is handed over the LTE system so that it can continue the call , using that LTE system .
VoLTE supports :
1. SRVCC ( Single Radio Voice Call Continuity ), in the UE is on the active-call and if roam to the area where 4G system are not persentt then , it handed over to the 2G,3G system.
2. CSFB ( Circuit Switched Fallback ) , in this UE is not in the active-call , but the call is perivously handed to 2G,3G before the call is conected .
In 5G core , the SRVCC , CSFB are not avilable.

 # Vo5G Codecs:
 * A codecs is an algorthim that digities and comparesis the Voice at the transmitter and  reciver it decomparesis and give a analoge wave shape .
 * In the case of 5G it must work over two codecs :
 * a. Enahanced Voice Services (EVS):
   1. It supports the narrow band to wideband HD voice uptill the data rate of the ( 128 Kbps ), and it is backward compatible with WB-AMR, EVS is more Robustness to delay jitter and packet losses, dealy jitter is the random delay in the packets of voice , which may have the bad quality of voice , that is heard by the reciver
* b. Immersive Voice and Audio Services (IVAS):
  1. This codecs is underdevelopment , this codecs would be able to support the mono to stereo  to fully immersive voice for the VR application .
* Whether the Voice is coded into EVS  or IVAS , this voice is carried in the RTP packets ( RTP : Real Time Protocol ) and these packets , then carried in the UDP packets at the transport layer , and these UDP packets hen carried in the IP packets .

# SIP ( Session Initiation Protocol :
* SIP is an application layer signaling protocol , and it is important because it used in the IMS signaling , it is a simple and flexible protocol that is used to create and modifying and terminating sessions.
* The SIP packets carry the Session Description Protocol (SDP), whenever we have to setup the call we need some parameter , like we would need IP addresses , port number , use codecs and the bandwidth that is required , for that particular call , and the formation about all the parameters, is describe using the session description protocol, and the packets in the SDP are incapsulate in the SIP packets .

# IMS in 5G System :

![2 2](https://github.com/user-attachments/assets/beaa40cb-e2a4-47ed-bf84-30b8c80eef84)

* The yellow once are the important components of the IMS system , as the voice services are concern , and the architecture remains unchanged , but as IMS has to interact with the 5G service based Architecture , so some interfaces need to be modify , and these interface that are need to modify are shown in the red colour , on the side of the 5G core network , we need to introduce new services that can interact with the IMS system , and these services has prefix of Ncx_IMS.

# CSCFs in IMS :
* In the case of IMS the SIP signaling , it is used in order to setup the voice calls , and the fxn of these Call Session Control Functions , that they analyz and route the SIP message so that they can be used to setup .
* There are the three CSCFs :
1. I-CSCF : Interogating Call Session Control Function
   *  When a registeration request , made up by the UE , with the IMS network, this request comes to the proxy Call Session Control Functions then this request is passed to the service Call Session Control Functions and the Interogating  Call Session Control Function checks with the UDM whether this User is register to the IMS network or not , and if it is not register with the IMS network then the I-cSCF would assign a serving Call Session Control Function, to that user , the I-CSCF will pass that request to the corresponding service call session control function , similarly the call is comming form the another IMS , that call is for the user that is in IMS network then this call will go to the I-CSCF , and then it will check to the UDM , to which serving call session control function , the call user is assigned, and after that I-CSCF would pass that SIP call to the corresponding serving call session control function ,which is assigned to the call user.
3. S-CSCF : Serving Call Session Control Function
   * Once the registeration request of a user has reached the ,S-CSCF , this function will interacte to the UDM , in order to interact with the security information of this UE , and then S-CSCF , would use that security information in order to authenticate , the UE . and ocnce the authentcity of this UE proven then in that case the serving calls S-CSCF , will register this UE with itself and sends this information to the UDM similarly when this registered UE, wants to make a call , in that case the S-CSCF , interacts with other servers in order to set-up the call .in voice call the S-CSCF it has to interact with the TAS to setup the voice call .  
5. P-CSCF : Proxy Call Sessi on Control Function
   * It sits at the beginig of the IMS , so it is the first poiny of contact to the  IMS to the network like if the UE wants to register or nmake call it has to first make contact with P-CSCF , and then the msg is routing to the appropiate node , for ef the UE wants to register itself with the IMS , then P-CSCF will forward to the I-CSCF , and this function also provides the secuirty to the IMS network, the UE is launching some flooding attacks , and also it provides the QoS  end to end IMS services .
     
# TAS in IMS :
* the CSCF provides basic call processing and routing , facilities but if we want to have supplemently voice services for eg calling lins ID hiding call divert etc , then in that case we use the Telephony Application Server (TAS) and during the call set-up process , CSCF interacts with the TAS , in order set-up a voice call that has the features of calling lins ID hiding call divert etc .

# IMS Connectivity Requirement:
* In order to use the services of the IMS , UE first needs to connect to the IMS , in order to do that the UE first establish a PDU sessions , and using that PDU session , it would connect to the Public data network or the packet netwrok since the  IMS is the part of the PDN , teh UE would connect to the , IMS system ,or more precisoulsy to the proxy-CSCF , in the IMS network.
* PDU session for the IMS connectivity , for eg the UE  wants to register itself to the IMS system so it need a PDU session , with One Qos flow , and, this QoS would have default parameters , that means that it would be set-up according to the default parameter as decided by the operator and this QoS flow used for IMS signaling , in this case it would be used to registor , this UE tp the IMS ssystem , like this UE wants to genrate the call then this UE need two QoS , the first one be the default Qos which would be used for IMS signaling and  the purpose of this IMS signaling is that would be to generate and maintain the voice call , and the actual packets of the voice would be carried on the second QoS which is also called as the  ims  media bearer , and the QoS parameter of this flow depend upon the voice call , if it is a high defination voice call or it is a standard defination voice call , according to the quality of the voice call , the parameter of second flow would bve decided by the IMS system . 

# IMS Registeration :
* In order to communicate with the IMS network , a UE must know at least one IP address of the P-CSCF, becuase it is the point of contact , of the UE with the IMS system .The process of knowing IP address of the P-CSCF is called P-CSCF Discovery ,it can be made in three ways.
* In the first method , the UE is establshing PDU session and assign a IP address by the SMF ,but at that time the SMF also, notify the UE , about the IP address of the P-CSCF .* In the second method , the IP address of the P-CSCF , is statically configured in the  UE .
* In the third method , the UE generate a DHCP query and, as a result the DHCP server then assign the IP daddress of the P-CSCF , to UE or it may assign , the Domain Name of the P-CSCF and if it is the Domain name then. in that case the UE , generate an another DNS query then the DNS server would transfer the ,  that domain name to the IP address of the, P-CSCF .
   
# IMS Registration:

![2 3](https://github.com/user-attachments/assets/f089397c-3814-4062-a134-42647db3fe24)

* In the fisrt step a UE send a registration request to the P-CSCF , and this request is the SIP messge , then P-CSCF will rely the request to the I-CSCF , now this fxn use Ncx_IMSRegistartion_Get service , in order to query the UDM , that whether , user is already register with the IMS or not , if it is not then it rely the request to the S-CSCF , it would use the Ncx_IMSRegistartion_Register service of the, service based architecture , in order to send the registeration , request to the UDM , then it tempoarory register UE to the S-CSCF , and also S-CSCF request for the Authentication Information , for this it would use Ncx_IMSAuthentication_Get sevice , after getting it the S-CSCF will challenge the UE for the authentication .
* Then the UE will respose to the challenge of the by sending the authentication response , if the authentication is successful the the S-CSCF , will inform the UDM , about the success of the authentication , and then UDM register the UE against this S-CSCF , then it notify the S-CSCF by sending the Registration complete , the the S-CSCF will send the OK msg to UE

# 3rd Party Registeration :
* We know that the S-CSCF can offer only some basic functions such as session routing and the session managemnet , but if want to have supplememtly service we need to invole the application servers eg, TAS (Telephoney Appliaction Service)
* During the third party registartion , the S-CSCF informs the TAS , that the user is now connected and ready to communicate  

# Call Setup :

![2 4](https://github.com/user-attachments/assets/1509d43d-d066-4f6d-b733-feec44b18ea6)

* In order to generate a Voice call over the 5G network , it is important  that , the calling UE , and the called UE , are register with the IMS network , that means a S-CSCF is assigned to the calling UE, and to the Called UE , To communicate with each other the calling UE will send a SIP invite msg , to called UE ,this SIP invite mesg will contain the Session Description Protocol Offer , it contain the information like , IP address , Ports , Codecs . When these information reaches to the called UE it send a msg of session progreass (SDP Answer)  , in that , there would be the IP address the called UE will use , the port and codecs that it has selected for the voice call , and once  the information is recive by the calling UE , then it acknowledege the msg by the Progress Aacknoweledge , then  the Called UE would send a 200 OK msg to acknowledeg the PRACK msg .
* Once this signaling has been establis on the bearer IMS signaling  , and once all the sufficent information are get then the IMS Media Bearer establishment take place , over it the actual voice communication will take place , once this is set-up an update SDP Offer msg will be send form the Calling UE to the Called UE, to Induicates media bearer has been established , then it will be response by the 200 OK msg , then a 180 Ringing msg would recive , by the calling UE , that the called UE is now hearing the ringing sound , and ringing tone would also be genrated to the calling ue , once Called UE picks up the phone , it send the 200 OK msg , and calling UE will acknowledege this ,and the calling is began.


































