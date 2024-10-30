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
   *  When a registeration request , made up by the UE , with the IMS network, this request comes to the proxy Call Session Control Functions then this request is passed to the service Call Session Control Functions and the Interogating  Call Session Control Function checks with the UDM whether this User is register to the IMS network or not , and if it is not register with the IMS network 
3. S-CSCF : Serving Call Session Control Function
4. P-CSCF : Proxy Call Session Control Function
   * It sits at the beginig of the IMS , so it is the first poiny of contact to the  IMS to the network like if the UE wants to register or nmake call it has to first make contact with P-CSCF , and then the msg is routing to the appropiate node , for ef the UE wants to register itself with the IMS , then P-CSCF will forward to the I-CSCF , and this function also provides the secuirty to the IMS network, the UE is launching some flooding attacks , and also it provides the QoS  end to end IMS services .
     











































