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
