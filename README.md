# 5G_Notes2
# CHAPTER 1: 
## Standardization of 5G :
* ITU-R ( International Telecommunication Union - Radiocommunication ) it is responsible for the developement of 5G reqirements.
* They are responsilbe for the previous Radiocommunication technology like 3G , 4G and now for 5G.
* These requirenemts are then taken by 3GPP , it is organisezation which is consortium of the major Telcom Venors and Operators.
* When technical specification are finalised then vendor makes the equipments accordingly .

## ITU-R minimal technical requirements for IMT2020:
* Like peak data rate should 20Gbps , it means like ,  there is cell an dthere is user in the cell , that a cell is using its all resources to provide data to the user cell.
* Actualy-User-experienced Data rate which is btw ( 100-1000 ) Mbps , this mean that if we are in a large cell then in that case the minimum data rate that the user must be able to experience is 100 Mbps , if we are in a building and have a cell then user will experience 1000Mbps.
* Area Traffic Capacity , in case of 5G in a area of 1m2 where it experince 10Mps/m2.
* Network Energy Efficency , this is speically use in IOT where mutliple sensors are connected and transmitted minmum data , and we want these senors to last longer in life .
* Connection Density , in case of 5G , these are also essential for the IOT like multiple sensors are connected with 1 milloions of users .
* Latency , it defines as a time taken by the device to send data to another device is called latency , which should not be greater than 1ms.
* Mobility , 5G is desgine to support high speed moving device , where speed can be 500m/h.
* Spectrum efficency , in 5G it must be 3time higher it mesare in bits/sec.Hz.

## Roadmap of 5G :
* 3GPP plays a major role in the standarziation of 5G network :
* The standardization is divided in two phase :
* 5G phase_1
* 5G phase_2

# Chapter 2:

# 5G ARCHITECTURE :
## 5G ARCHITECTURE HAS THREE MAIN COMPNENTRS:
* UE ( USER EQUIPMENT ) like , mobiles .
* NG-RAN ( NEXT GENRATION - RADIO ACCES NETWORK ) it is base upon the 5G nr ( new radio ) technology , and the main component of the NG-RAN is the gNB( next genration NodeB ) , gNB is the tower from which this UE connects , in another word these ue uses gNB to access  network that is why gNB is known as the acces netwrok .
* 5GC ( 5G CORE NETWORK ),if the ue is connected with the external network then , there will be some signaling btw the ue and the external network , and alos there will be the data communication , btw them , the roueting if tsignaling btw them is establish by the 5G core network .
* 5G is all the IP Architecture , this means even the voice and all the other services are basically carry on the packet data .

## 5G DEPLYMENT OPTIONS:
* 5G non-standalone
* 5G standalone
* ### 5G non-standalone:
* In this case we are using the evolve packet core of 4G networks and we are also using the access network of the 4G , which is E-UTRAN Access network , here we have the an enodeb of 4G which is actin as a master node and secondary node we are usnig the gnb 5G node , that means the mobile recives the control signaling form this master enb and it also reciveing data from it where in secondary gnodeb this mobile is only reciveing the data , another type  this is the one of the detail example of non-standalone.
* ## 5G standalone :
* This known as the standalone architecture because , here the core network , of 5G core and connected with the NG-RAN , here gNB is playing the master role and another eNB.gNB is playing role as the secondary .this concepts where mobile is reciving data from both these nodeBs , very much related to the concepts of dual connectivity .
* ### what is importantance of the non-standalone 5G architecture ?
* Basically  here in the above example we are using the 4G network , but many of the benifits of the 5G network can already be achive by using  5G NODEB , this mean that before the operator goes full-flege to the 5G deployment they can still get many of the 5G network benfits .

# Key Features Of NG-RAN or 5G NR :
* Small cell
* Dual connectivity
* Cloud RAN
* Beam-Forming and Steering
* Increased Specrum
* Radio Enhancements
## Dual connectivity:
* DC option  , here in this one of the nodeB is acting as a master and another is acting as a secondary . This means that this master nodeB is basically decideing , which type of data this mobile uor UE will get or what quality of services , which UE will get .
* So in order to achive that there is a connection btw master and secondary nodeB to decide upon what type of data and quality of service this UE will get that data.
* DC options:
*  LTE eNB connected to EPC
*  Enhanced eNB connected to 5G core
*  5G gNB connected to 5G core
*  Master NodeB decide data QoS a UE get and Bearer splitting can take place at either of the NodeBs , where here bearer is the channel , this means that the data channel is connected to the master nodeB and control channel is connected to the secondary nodeB , here bearer soilliting is that the data is going to the UE from master nodeB and also in secondary nodeB.,  similary the signaling comming form the 5GC ids bearer spilliting and going to master and secondary nodeB .

## Small Cells in 5G Networks:
* They are directly related to the concepts of dual connectivity in the 5G ; small cells are cell, which have a limited radius they can have radius upto , 10Km to 20 Km .
* They are used to imporve the coverage of Homes and Offices or use as a hostspots , they have the 5G air interface, that they are able to provide high data - rate , also channel impairement are also less .
* Also the channel is good because of the small cell or size .
*  By using dual - connectivity it increase the user data rate also.

## Increased Spectrum:
* 5G NR can operate into, two frequency range :
* 1. FR1 450-6000MHz
  2. FR2 24250-52600MHz
* These frequency ranges have thier own challenges
*  Below 1 Ghz : These frequency are exellent when we are desgin the cells with large radius , because these frequency rate has excellent , building pentration capacity with very small time , but there is some problem also , like there is only limited spectrum that is avilable  , because there are too many conjuncation in this frequency band as there are many services that are operating in this range .
*  1-6 Ghz : this frequency range has the advantage of good coverage as well as good spectrum avilablity as there are not too many wirless system that are alerady operating in this frequency rate .
*  6-100 Ghz : this is called as the milimeter range , so in this FR we have alot of bandwidth that is avilable because there are very fewer system almost none that currently operate , so lot of bandwidth provide alot of data rate , it is seviroly affected by the wirless channel , so this frequency rate is basically suited when we are designing small cell .

## OFDMA and flexible Numerology in 5G :
* the access technology , that is used btw the gNB and UE on the wirless or air interface it is OFDM ( Orthogonal frequency division multiple access ) and this is the same technology that was used in 4G LTE ,  but there are some significant differences , that we must understand .
* We know that in OFDM the frequency band , in a cell is divided in a into orthogonal sub carriers , when we have multiple sub-carriers , then there is a peak of any sub-carriers , other sub-carriers are at zero , and  the spacing btw two sub-carriers is called delta F , and in the case of LTE , sub-carrier spacing was 15KHz.
* 5G NR operate on wide frequency range , so as the frequency increases more interfrequency interference , that is because of the Doppler shift and Phase error, in the oscillator of the reciver .It may happenes that the orthogonalty condition is nay be disturb the other sub-carriers do not have the zero value at this point .
* In order to solve this problem , use scalable carrier spacing and the other name is flexible Numerology it is denoted as "	η " , when it is equal to 0 we have 15KHz carrier spacing btw the adjcent sub-carriers , when it is equal to 1 , the spacing is double as  the 	η increases the spacing also get double . for higher frequnecy we use higher 	η values
* There is another thing called cyclic prefix , so if we see in the time domian , the guard period btw two OFDMA sample is called cyclic prefex . and the purpose of this guard period is , that one smaple does not overlap to adjcent sample , special in the multi path enviorment.
* There are two prefix one is NORMAL and other is EXTENDED prefix , the extended one is use in  the large area , because there will be more bouncing back of the signal.
* Now in the case of 5G NR  the timw is divided into frames of 10ms then these frames are divided into subframes and one subframe has a time pf 1ms .
* the subcarriers spacing is 15 KHz then one subframe will have one slot of 14 symbols , know if we move form 15 to 30 KHz , we know  that time and frequency have inverse relation , when we are increasing the frequency of the subcarriers spacing the time slot is of time occupied by the slot will became half .
*  1 slot = 14 OFDMA symbols .

## Modulation in 5G :
* if the channel condition are favourible , if there are very low bit error on the channel , then we can use  256QAM ( Quadratual Amplitude Modulation ) in this case the number of bits/symbol = log(256) = 8bits/symbols then the data rate will be very high , if there is any obstical there btw ue and core than we have to lower the modulation as the link deteriorates upto , 64 QAM , 16 QAM etc.

## Cloud RAN :
* There are two main components of  CRAN technology :
* gNB Distributed Unit ( DU ), it is near to the base station and it only hold the transmitted/receive capability only , while all the processing gNBs is move to the gNB centralized unit and one gNB centralized unit basically handles  all the gNB which are under its judircation and  it handles computaionally demanding tasks , such as how the users are going to be schedul like what resources , in terms of resources plot allocate to the user or the secuirty of the users like thier signaling there data with the authenticator , simillary to the power control that is ugoing on to the centerface user .
* there many advantages to this approach :
* Easy scaling up of resources , as  all the processing is baiscally done in the gNB-CU , so if tehre is demand of more processing capablity it can easily be added in gNB-CU in the matter of hours , on demand we can allocate more resourvces in gNB-CU.they can also co-operate in processing and share there resources and upgradation and advancing the deployment of the techonlogies is easy in this case and the result is that due to all this factor the cost of the network in the case of the access side of the 5G reduces due to this cloud ran technology

# BEAMFORMING AND BEAM STEERING :
* Massive MIMO( Multiple Input Multiple Output ) is a key 5G technology , in this technology there are large numbers of antennas are installed on the base station and these antennas that are called the antenna arrays work together to improve both coverage and also increase data rate of the UE .
* In the context of 5G  the terms massive MIMO and the beamforming are often used interchangeably . to understand massive MIMO , first we have to understand SU-MIMO AND MU-MIMO.
* SU-MIMO : in this case there are 4 antennas in the transmitter and recivevr . so we call it SU-MIMO as 4X4 order , and we have one transmitter and one reciver , the transmitter can send 4 streams of data .
* MU-MIMO : here we have two or more reciver and one transmitter and here 2 or more streams are going to differnt recivers .
* these MIMO technique are specially suitable for the wireless communication enviroment , where we have lot of mutipatha and lot of scattering , max performance of MIMO can be seen in wireless channel or multiple path .
* If we are using frequency below 6Ghz for communication in that case these frequency sactter a lot & their are many multipath that are produce .
* In case of 5G we can go upto 8X8 order MIMO, that are below 6GHz .
* Wwhen using frequency abive 6ghz which is also known as millimeter wave band . so frequency are attenuated a lot, they are more directionsl which provides less sacttering & less multipaths are produces , so the max order if MIMO we can go 2X2 , on the other hand the directional quality if these frequency are suited for beamfroming .

## IMPACT ON ANTENNAS BY CHANGING THE FREQUENCY .
* we take eg , like we have an antenna of 3ghz patch of dimensissions 1000X1000mm when we increases the frequnency upto 30ghz then it dimensissions would be reduce 10 times 10X10 mm , so in 3ghz it will recives or transmitted less signals and take more energy as compared to 30ghz to solve this problem we make an antenna array containing 30ghz patch to solve the prblm .
# 3D Beamforming :
* Lets take an eg of 4D antenna array , and in this array wach antenna elements , is being fed by RF source , but before that we are actually adjusting the phase and amplitude of each of the input , in such a way that the resulting electromagnetic rays that are produce by these antenna elemnets the constructively interfrence in one direction , so that way we get a directional beam . By varying the inputs amplitude and phase we can steer hese elements in the 3D plane.
if we increase the number of antenna elements in antenna array then the gain will increase & also beam wil become more fouces or sharpe that means that the directivity of beam has increased.
# Beamforming & massive MIMO:
* In massive mimo technology we use large antemnna array & antennas elements on the basestation and the number of elements can be 16,32,or 64 or even more .
* The number of antennas array elements are muchlarger than the number of UEs.
* As in the millimeter wave band the beam that is begin produces is fouces due to high frequency , so the SNR of the UE increase & these beam interfrence very less with one and another . so we get high data rate for these UE.

# 5G ARCHITECTURE -gNB:
WC : wireless channel or wireless communication 
* Functionality of next genration gNB:
* The radio transmission/ recepition btw UE on the wireless channel , also gNB is responsible for the communication with UE in WC.
* Digital signal processing eg  voice or the signaling that is going from the gnb to the UE that needed to be encrypted in WC , that data that is coming form the UE to gNB must be decrpted , similarly the data that is going form the gNB to UE needes to be compressed so that in WC it occupy less band width .
* Access stratum signaling , is that signaling which going from the UE to gNB.
* Non - access stratum , is that signaling where the signals from UE is going to core network , so gNB does not process this NAS signaling .
* Radio resouce management , if there are many UE then gNB have to manage has to manage the radio resource that means what gNB has to decide that what resouce blocks are to be allocated to those UE in order to satisfy there demands in terms of data & QoS , it also decide at what power it is going to transfer to UE and at what power from UE to transmitted towards gNB . this is called power control.
* Communication core network , and nearby basestation : and why it is important ? There is a link btw these gNBs known as Xn interface . when mobile is moving from coverage are of one gNB to the coverage area of another gNB , then UE attaches to that gNB this known as handover , so gNB is responsible for handling that signaling .

# PDU ( Protocol data unit sessions ) :
* 5G is an all IP system that means , all the services like data , voice and multimedia , are carreied oN the IP packets . so in order to provides these serivces network need to establish PDU session in UE and each PDU session may consist of one or more Qos flow , eg like UE is surfing its data from one Qos flow and UE is also using voice call .
* Qos characterstices by: data rate of the flow and the or is guranted or non guranted
* or is their any conditions latency on these packets and what is priorty of these packets .
* if we compare the service of the voice call and data surfing service the priorty of Qos requirement , for these two services are very different form one another because we can not allow the dely of flow of the Qos of voice packet and a PDUsessions have different Qos and ach Qos is own Qos ID , and a UE establish only one PDU ession on a one network slice.

# Control plane & User Plane sepration in 5g :

* the entities that are above the dash line are control plane  and the enitites that are below the dash line are user plane , because the enity like gnb , UPF data network they are all ready include in th edata traffics forwarding data does not flow above this dash lin ebut iy is handle by th eentity which are below to the dash line ,
* While the other functionality are fall in control plane the enitiy are the nodes which are envoled in the authentication of UE wheter it is a vaild UE or not tp provide the connectivity to ue these connection mangaemnet are in Control plane , similarly how to provide qos data flow or PDU flow to ue all these fxn arein the conrol plane .
* Aadvantages of separtion :
* the main adv is saclaboilty , if ue data requirement increases than we can have more upf or we can increase the capacity of upf & increase capacity of gNB by separation we can scale the user plane and control plane as per the requirments.

# 5G core network - AMF ( Access & mobility managemengt fxn ):
*  when UE gets switch on the first time it register itself the network fxn that is responsible for the registration is AMF & whether it is in the call or not in call in idle state , in these cases the network fxn in whihc the ue directly communicates by a gNB it is the AMF.
*  before registeration ue need to be authenticated , in order to check whethere it is valid user or allo to connect woth this network or not , this authentication process is intiated by the AMF .
* Another important fxn of the AMF is mobility management, know the UE can be in the one of the two states, either it is idle, that means this UE register itself to the network but it is no in the all in that case the location of UE is known to the network at the tracking area level. The cells in 5G network are divided into tracking area. Each group of cells different tracking area numbers if the UE moves from one TA to another TA then the TA numebr needs to be updated in core network anmd this updation procedure is done by AMF.
* Similarly the UE in call in that case its location is known to the network up till cell level and when a UE moves from one cell to another its location is needed to be updated this case is also handle by AFM.

# Authentication Server Function(AUSF)
* When ever the UE wants to register it has to be first authenticated this is authentication is iniciated by AFM but inorder to complete this authentication process two other entities are also needed UDM and other is AUSF, whenever AMF iniciate the authentication process it basically sents the identity of UE to the AUSF it requests UDM to generate authentication vector based upon the secret key that is there with the UDM and then this AV is passed to AUSF and it pass the AV to the AMF now within that AV there is a random number and AMF challenges UE with that random number, UE generates the authentication response which goes to AMF and passes to AUSF and then it check that it is a valid AR or not, based upon that AUSF decide that whether this UE is authenticated or not.

# SMF (Session Mangaement Function)
* We know that when UE wants to use the data services of the 5 G network its need to establish a PDU session with the 5G network. The piupe that we talk about eg we can have a PDU session going from UE to UPF then it going to data network after going to this PDU session, so the establishment and management of this PDU session is done by SMF as a part of this PDU session SMF has to coordinate with PCF and it is the PCF which decides that under the given network circumstances of netwpork condition whether this PDU session can be establish or with what QOS the PDU session is establish it is decidee by the PCF. SMF also coordinates with the UPF, First of all its selects the UPF in which the UV establish the PDU session or there may be more than one UPF and similarly for the establishment or there PDU session.SMP actively coordinates with UPF as part of this PDU session SMF needed to allocate IP addresses to the UE

# User Plane Function(UPF)
* UPF is the very importanbt part of the 5G core network it is important because it the point of contact to the data network with the 5G core network and , whenever data packets arrives from the data networks it is the UPF that decides that where it needes to route host packets. Similarly on the other sides UPF is the anchor point for the UE , that means UE establish a PDU session with the UPF if UE is moving it may go from the coverage area of 1 GNB to another GNB but it would always be anchored to UPF , so it the PDU session establish between UE and UPF will does not get affected, whether the UE is not in GNB coverage also PCF decide that what would be the QOS of this PDU session and this decision is then taken by the SMF intimated to the UPF, so the enforcement of this QOS decision is done by the UPF , it is the UPF that implements the QOS for this PDU flow.

# UDM ( Unified Data Management ):
* It is the very important function of the 5G , because it is the centralised data base for all the subscribers , in the 5G network.
* It can has its interanl database built into it , or it can use a external database as unified data repository , it is also importanat because it stores the secuirty key base upon which the differents UE subscirbers is authenticated , whether they afre vaild or not.
* Similarly , when UE moves form one gNB to another gNB , it may go that gNB under the control of the another AMF .
* This UDM keeps track of that in which AMF , area this UE is located .
* It also holds the subscriber information , like what type of data services a subscriber can use with what QoS , also whether a user can access what type of services or what not .
* Also UDM , has information that user is alowed to roam , certain tracking area or not , that UE can be restricted to certain area or use cretain services or not .
* Also , Romaing restrictions information also present in UDM .

# Policy Charging Function ( PCF):
* It is involed in dynamic policy decision base upon network conditions like congestion , Subscriber geo-location etc .
* For Eg , a UE is loacted in the gNB , where it has bad or poor channel conditions and this UE wants to make a call,so this request of call recives PCF through the session management function , now PCF makes two decision:
* 1. to Throttle its data of that user , so that it can make video call
  2. OR Refuse the cell .
* so in above case PCF is closely intercating with the SMF .
* Similarly PCF , is also involve in management of services areas , service area for a UE is list of allowed and not allowed tracking area .if the ue is present in not allowed TA and ue wants to make a call , then PCF interact with AMF , it can refuse the call all together
* So, PCF interacts with , AMF , SMF and AF .Also PCF decides the charge of the User who is using the services of the 5G network .

# Application Function ( AF ) :
* It is an external server , and this external server communicates with the core network , and more preciously with the PCF in the core network , in order to request for new packets flow .
* For eg , AF can be an IMS Node ( IMS stands for Ip multimedai Sub-system ) , this is used to genrate voice call over the , IP . 

# Network Function Virtualizaton ( NFV ) :
*  In 2G network the BTS is connected to the BSC which is further connected with MSC , so the network nodes implemented as special-purpose hardware , as a result it was expencive in terms of buy , maintain , and replace .
* The hardware eventually needs to be replaced but , the hardware should be of same vendor also it was difficult for new hardware vendors to enter the market . Also it was difficult to upgrade thenetworkm to supoort new use cases .
* so the solution of these prblms is approach of NFV , so in this the network's functioanalities is implemented as the software , and this software is running on the Commercial Off the Shell ( COTS ) , it is the hardware like servers , storage and switches that are easily aviable in the market .
* Advantages of this approach :
* 1. The cost of both hardware and software reduces .
  2. It is easier for the new vendors to enter the market .It is easiy for new vendors to buy the COTS functionality hardware and implementing the software on the top of it .
  3. It easy to upgrade the network , that is only have to upgrade the software .
* This is the NFV architecture as given by the ETSI ( Europeain Telecommunication Standard Institute ) , and at the top there is Virtual Network Function , which are implemented on the software .
* They are running on the NFV infrastructure , that Physical hardware resources , such as computing storage and networking, and there is a virtualization layer , that is virtualizing the all these resources as a virtual computing resources , virtual storage  resources, virtual networking resources and we can make further partiation and like  virtual computing resources, It is the virtualization layer where this magic of virtualization is handle .on the top of these virtualzation resources we have the software processes that are running the functionality .
* These Hardware resources , Virtual resource and partiation and these VNF , all of these is manage by the MFV managemnt and Orchestration function , this fxn decides howmuch resources to be given to which software process or what will be the partiation in this virtual resouce.
* The advantages of NFV in 5G are :
1. 5G is a collection of network functions that are virtualized on a clod infrastructure so that it is easily access able easily and no custome hardware based on COTS
2. It easily to deploy new network function quickly , because they are implemented on the software and it shared the usages of resource .
3. Also we can scale up down the resource that are given to these virtual network function 

# 5G network slicing :
*  It is another key technology in the 5g and with the help of it , 5G operator can actually build virtual end-to-end networks on a common physical network ,these network that are called slices have different quality  of services as per requierments . eg Mobile boradband can be one of the slice ewhere some internet provider is , providing a low latency mobile broadband service, similarly massive internet of things slice can be used by some shipping industry in order to control its crians that are there on the ports that are used in loading , and similary machine critical internet of thing slice can be used by some automotive indusrty to connect there cars and the requierment for this slice are reliablity and low latency so these are the virtual networks that are separated from one and another in the control plane and in the user plane.
*  These slicing are possible because of the NFV and it allows creation of multiples virtual networks on a shared physical infrastructure , and user experience that as physically separate network although they are running on same PF .
*  It is crucial because the different services that the 5G network is providing they have different quality of services requierment and these slices optimesd for the particular services that they are providing accordingly the QoS requirements one slice is optimise for one use case .we can increase the resources of slice as per demands .

#   NRF ( Network Repsitory Function ) :
* It maintain a list or profile of network functions , that are avialbe in the core network . If any Node want to check the fxn of any other node then it sends the discovery request to NF , then it will responsed by returning the IP addresses or the domian name servers of the servers where the network function of that node are related .so all the network function havce to register themselves with th NRF , so that NRF so that is can fascletate them by discovering other network fxn .

# NSSF ( Netwok slice selection Function ) :
* For eg , a  UE is register to the AMF , that this UE wants to use a network slice that are not serve by the AMF , then this AMF invoke the NSSF , it basically return to UE about the network slice and what AMF is providing that service , so that this UE , can aviale that network services or network slice by connected to that AMF , and this NSSF is new in the 5G.

 # NEF ( Network Exposure Function ):
 * It exposes the capabilities of the network fxn that are there in the 5G core to some external AF , it is so because very often any external AF is not allowed to communicate directly with the 5G core , due the secuirty concerns.
 * the AF first communicate with the NEF , and then NEF authentiactes and authorizes this AF it is the vaild AF to communicate with the 5G core and after that it is the NEF that decides that what rate this external AF transfer information with the network fxn , of the core network and this NEF acts as the middle man for the communication between th eAF and any of the elemnets of the 5G core network .
 * So it playes very important role for the sercuirty of the core network .

# 5G UE Identifiers 
* The UE consist of the two elements , the first is device or mobile and thhe second one is the sim that is put into that mobile . The identity of the mobile is form which it is recogniseis the Permanent Equipment Identity ( PEI ), The only currently formate that supportes the PEI is IMEI this means that for th technical purposes the PEI , is same as the IMEI and we are familier with the IMEI form the devices that were used in 3G , 4G its the same IMEI number that acts the PEI .
* second is the identity of the SIM , the idenetity if the sim by which network identify the sim are the in other words that the network identify the subscriber that is using this sim is the SUPI ( Subscription Permanent Idetifier ) . lets take a eg where a RAN access 3GPP  then the sim is identify by the IMSI , but in other case when the RAN is not accessing the 3GPP then the sim is identify by the NAI ( Network Access Indentifiers ). so supi can be IMSI in 3GPP acces or NAI for non 3GPP access .
* Subscription Concealed Identifier ( SUCI ) now one of the main problems , when we talk about the 3G ,4G system was that first time we powerd up the mobile and this mobile needed to register itself with the network it uses its IMSI for that purpose , if someone is there with the IMSI catcher it catches the IMSI .
* So in the case of 5G they try to improve and solve this problem , and in case of 5G the UE first power on then it first register itself with the network , after the power up , in that case the SUPI is encrypted using the sercet key in the sim , and after the encryption it is called as SUCI .so this mobile uses this SUCI to register to the network .
* After the mobiles are register to the network ,then the key elemnts of this registeration process is AMF , so the devices is register itself to AMF to the core network , AMF assignes the TMSI (5G S Temporary Mobile Subscriber Identity ), which is often change by the network form time to time , after that the communication is done by the TMSI not by the SUCI , and this is unique in the area of AMF .
* If due to some reasons this AMF area is not known , in that case 5G Global Unique Temporary Identifier ( 5G-GUTI ), whihc identify gloably a moible is also assigned by its last AMF .

# Tracking Areas in 5G :
* Now the sevice area are divided into tracking areas and these areas does not overlap each other , and minmum it contain 1 cell or max in many cells .The mobile can be in the IDLE mode where it is not in the call or it is in the call .if the moible is in idle state then its location is known in the tracking area , but it is doesnot know in which cell the mobile is located , if in case of incoming call then all the UE in this tracking area need to be paged all the UE with the TMSI of the that device so that we get to now the laoction .
* The purpose of building TA is to reduce the signaling load when the mobile is idle because in that case we need to update the location of the mobile form one tracking area to another tracking area .
* If the mobile in a moving train then the network will assign  a list of TA to this mobile , so that we it is moving very fast in these TA then it does not needs to updates it TA .

# 5G Network Identifiers :
* The identity of a mobile which consist of RAN and code network is known as  Public Land Mobile Network Identity ( PLMN-ID )basically it is the combination of mobile country code (MCC)and the mobile network code(MNC) for this operator .
* Then we have the identity of the AMF , so this is called as AMF identifier ( AMI ) , if we add MNC|MCC to AMI this becames GUAMI ( Globally Unique AMF Identifiers )
* Each tracking area has a code that is called as tracking area code when we add MCC|MNC to TAC then it becames TAI ( Tracking area identity ) which identify this tracking area gloablly .

# UE Power-on Procedure :
* when we power ups the mobile it runs the accquisition procedure , if the mobile is between in the cells then mobiles reades the PSS and SSS of these basestation ,and reading this sequences is important because this mobile will decode the broadcaste information that is being broadcast by each of the cells these information tells about is the channel structure of a cell , what channel and what frequency and this base also contain information that , this base station belongs to which mobile operator , this information is broadcast on the physical broadcaste channel , and if a cell has the boradcast information it is called as primary cell.if the cell dose not have the broadcast information then this cell is ignored by the mobile.
* The UE has list of primary cells , and these mobiles cells belongs to which channels , after the cell accquistion procedure , a the mobile run the network selection , because the near-by basestation belong to other network , first of fall the mobile will try to register itself to the last registeration network if it is not avilable then it will try to cennect to the home network which this moblie belong , if this also not avilable then it will try to select the network written in the user list , then if there is not possible then it will try to select the operator list and if no netwrok form the avilable in operator list then it will select the network whose cell has the most powerful signal .
* When the network is selected , within that network the mobile has to select the cell , after the selection of cell , next step is radio connection kit make the radio connection wiith the access network, when it is done then next step is the authentication and key agreement is select.
* This is important for the security based on a process termef as 5G AKA .
* AKA is based upon the shared secret key , one side the SIM has secret key an on the other side UDM ha sthe secret key, based upon these key the mobile authenticates the network and network authenticates the mobile so that , network know that this is a geniun mobile user and mobile knows this is the geniun network.
* Signaling between th mobile between gNB access stratum siganling is encrypted , and also the signaling btw mobile and the amf which is known as non-access stratum signaling is also encrypted and data communication is also encrypted .
* In the next step the UE context installation to the AMf , then AMF request the UDM in UE context which is provision by the UE context , this is important basically thios context tells the that what type of DN can use what type of DS is used and with which QoS , what is the bandwidth and data rate is mobile usewhether this mobile has the subscriber or can roam in the area in order to use this network or not .
* In next step AMF perform a policy to check with the pCF , and the policy decision is made by the OCF , depends upon the time ofday , location of the user and network congestion .
* after that AMF assigns a TMSI to this UE and  all the signaling now between the mobile nd the network is using by the TMSI andit actually change the potenially due to an AMF change.

# UE IDLE And Connected Modes :
* IDLE mode
* 1. the location of UE is known to the TA level
  2. UE is a camping on a cell.
  3. Ue is listing to the paging channel , if there is an incoming call is coming , then
  4. That paging message will contain th eTMSI of that mobile ,and then the UE response to that network , network would know the current cell .
* Connected Mode :
* 1.UE is actively exchanging the voice or data with network and in that sutiation the UE loaction is known to cell level , and the TMSI is used for the communication between the UE and the network .

# PDU session establishment :
* After the completion of perivous steps this mobile willl genrate the estavlishment request and then AMF will  notify the SMF performe the policy check for this request PCF do the policy decision , will be based upon what are the current network condition , there is congention in the network what time is it . based upon these condition PCF  will decide the request can be enteratined or not , that this mobile can  use the network for this particular service or not , so if this decision is positive the SMF would coordinate with the   AMF abd UPF in order to establish the user data PDU session , and then this PDU session is establish between the mobile and UPF 

# Paging Procedure :
* For eg , there is a downlink data that arrives at UPF for a particular moible so ,UPF will notify the SMF about the incoming data , and then SMF will notify the AMF , to page all the mobiles that are in the tracking area where this UE is loacted , and this paging msg contains TMSI , of the mobile for which this call is incoming , when UE recives the paging msg it would respond to the network nd after that , the PDU session can be establish for this downlink data .

# Tracking Area Update procedure :
*  For eg , we an UE , which is curenntly in some TA , if the UE moves from one TA cell , to another TA cell then , then this UE will inciate the Update of TA procedure , and it would send the update request to AMF , AMF will delete the old TA and record the new TA , and then it would notify the UE about the TA update .

# Handovers in 5G :
* Handover always take place when , UE is in connected mode , that means it is in active call or PDU session with the network , if UE is moving form one cell to another cell coverage area ,this the first cell is called as the source gNB and second cell is Traget gNB .if the mobile is moving from the coverage area of the spource gNB to target gNB , then the mobile is need to be switch to the target gNB
* There are two mechanisms of the handover in 5G :
* Xn handover
* N2 handover
* ## Xn Handover:
* Xn is basically the interface between the two neighbouring gNBs , when a mobiles  moves from coverage area of the source gNB to the target gNB these two gNBs need to coordinates with each other for the neseccary information that is needed to be handover , information like secuirty info , keys info and also about the charascterstices of the PDU session ,once the handover is done and UE is connected to the new cell , then this target gNB will make a request to the AMF , that the switching of the PDU session that is going to the UPF to the source gNB so this AMF then request the SMF to genrate this switch and then , SMF will ask UPF to switch the PDU session from the source to the target gNB .
* In case of  N2 handover there is no interface between the two gNBs , so the AMF is playong more important role , so all the information that is being exchange between the source and target gNB during the handover process , it is basically AMF acts as the middle man for the exchange of this information and once the device has switc over to the next target gNB , then AMF will request SMF , to switch the PDU session fron the current UPF to the target gNB .

# Chapter 11:
# 5G Service Based Architecture :
* Service Based Architecture has been introduce in the 5G in order to increase the modularity of the sysytems .In service based architecture , the Network Function provides one or more services to other Network function in the network .
* For eg , there is two network Function , NFI and NF2 where NF1 is producer the services A1 and NF2 is reciving the services as consumer , and these services are provided by the Service Based Interface ( SBI ).

# Main Mechanisms for NF services :
* ## Request-response :
1. In this mechanism , the services consumers request from the services providers , as a result of this service request , the service provider provides the information to the services consumer or it takes some action or do both the things.
* ## Subscribe-notify :
1. In this mechanism , the service-consumer subscribes to providers services , and when ever there are events that occurr related to that services , the services provider informs the consumer about those events or another scenario that the service provider , provides periodic update to the service consumer relayed to that services.

# HTTP/2 for 5G Core Network :
* In service base architecture we are the network function communicates with each other , it is done using the   HTTP/2 protocol and the HTTP/2 is deploy widly on the internet ,using this protocl it is easy to depoly these on the cloud using the virtualization .
* Because of it widly deployed over the interent , it is well developed , security mechanism and third party application .
* If the new application are developed by the third party or the operator using the HTTP those application can easly intergrate into the 5G core network .

# HTTP/2 on Web Vs HTTP/2 in 5G Core :
* There is differnce between HTTP/2 on web and HTTP/2 5G core .
* HTTP/ ON Web :
* Eg , a laptop is acting as a client , it is sending the srequest to server , it is possible that these request may have some content , when this server response in HTTP response msg it is possible there is content in the body of the response and the response may be in the formate of the PDF , HTML OR JPG fromate .
* HTTP/2 IN 5G CORE :
* Eg , the network function , here is making a HTTP request to other network function and if there is data in the body of the HTTP request it can only be in the JSON fromate , and when this network function response to the request , and in the response if there is data then itt also onlybe in the JSON fromat.

# JSON ( JavaScrit Object Notation ) Format example :

![json](https://github.com/user-attachments/assets/8b75a464-1db4-43c1-a400-4529efccdcb0)

*  The curly bracket at the begning represents the starting , and the json store data in Name-value pair . Also json objects are nested in to one and other .

# Concept of Resource:
* Examples of resources , when when we are creating a PDU session , then we are actually creating a resource and assocication with the PDU session , a context is created which is also a resource and QoS policy is created which is also a resource .
* The second example , registeration of network function with NRF , we know that NRF is network repository function , which is the central repository where all the network fxn in a network register themselve along with the services those network fxn provide .the registeration is also a resource .eg if there is SMF and it wants to register itself with the NRF ,then this registeration is the resource which is located in the NRF , and this resource have a URI ( Uniform Resource Identifier ) the resources that are located in the 5G core , are mainpulated with the URI , if SMF wants to register itself then it genrate HTTP request with the URI so this resource would be created , in the NRF which located by the URI .

# HTTP Methods used in 5G :
* When a service  consumer makes a HTTP request to the service provider , in this HTTP can used different Methods , These methods are the standard HTTP methods used in 5G core network , and out of different HTTP methods , are  PUT , GET , PATCH , DELETE , POST .
* PUT - It is used to create or replace a resource .
* GET - It is used to read a resource or if you want a information without modifying a resource .
* PATCH - It is used when you partially update a resource .
* DELETE -  It is used when we wants to delete a resource .
* POST - It is used to create a resource , it can also indicate to the other network function to process the enclosed information , and we can execute a remote call in the network function.

# HTTP Responses in 5G :
* A HTTP resources is defined by the three digit code .
* 2xx -Success
* 200 response means that every thing is OK ,
* 201 response ,means that the response is created ,
* 202 response , means that the request has been accepted .
* 4xx-Client ERROR
* 400 response , means that it was a bad request by the client ,
* 404 response , means that the URI has not been found .
* 5xx-Server Error
* 500 response , means that there is a interanl server error ,
* 503 response , means that server Unreachable .

# Naming Scheme for NF Services :

![2](https://github.com/user-attachments/assets/5af1dd57-29c8-4f2f-b942-03a5662b8a0f)

* Eg : Nsmf_PDUSession_CreateRequest , this a service , it provided by SMF and it is provides through Nsmf .

# "REST" Applied to 5G Services :
* "REST" stands for Representational State Transfer , and it is basically an architecural type that how software are developed , it define a set of rules for the design of distributed application .
* In the 5G services provided by the 5G core or the API , they are implemented using the REST "paradigm" more preciously in the context of 5G core network the rules of REST actually applied to the HTTP protocol in order to have this architectural style for the 5G corenetwork API's .
## Principles of RESTful Design :
1. Client Server : there is a service consumer which is the client and there is a service provicder , according to the restful principle there should be distintion of the responsiblities between the client and server .
2. Statless : the server has recive the HTTP request , this request must contain all the nesaccary infromation in order to understand this request , server does not need to kep track of the request that are send before or that would be send in future in order to understand this HTTP request .this means that no state is maintain on the server side the state of the session is only maintain by the client side .
3. Cacheable : The client recives some information form the server , the server must indicate that wheter this infromation is cacheable at the client or not , if it is cacheble then how long , that what is the validity time for this information .
4. Uniform interface : the different resources that are there in the 5G core network , they are basically Identifed and mainuplated using the URIs.
5. Layered system : if any network function is commumnicating with other NF , then each NF cannot "see"  beyond the immediate layer with which they are interacting.

# Use Case 1: Network Function Service Reqistration :
* How the Network function resgister itself with the NRF , by sending the message to the NRF , and the message consist , NF management services provided by the NRF , when registering network fxn sends this msg , it send using the HTTP PUT method , becauce PUT method is used to create new resources , , here the resource which is creating is the registeration of this network fxn , and this HTTP PUT request is send to URI .
* URI have many part :
1. API root : it interanlly have three parts :
   a. Sheme :HTTP:// OR HTTPS://
   b. Hostname : host name of NRF like , nrf.5gc.mnc015.mcc234.3gppnetwork.org
   c. Optional port number
2. API Name : like , 'nnrf-nfm'.
3. Api Version :  like ,'v1'
4. NfinstanceID : Unique ID , which is unique inside the system where it is created while the registering network function , registeration , by the NRF.

* Along with this messages there is a body which is of JSON formate :
* the parameter which consist in the json body , are
  1. nfInstanceID : it is the unique identity form the NF instance
  2. nfType : whether the registering network function , is the NRF ,UDM AMF and SMF.
  3. nfStatus :whether the registering network function , is regestered or suspended
  4. sNssais : then we have the network slices that this NF supports
  5. capacity : what is the static capacity of the NF .
  6. load:% dynamic load on the NF
  7. IP address or the domain name of the resgistering network function .
* In the next step , NRF response to the request , and it would send a msg which has same naming format , except there is change that there is response , and this message is send by the help of HTTP 201 method , it indicate that the registration has been created succesfully .In this response message there would be a heartbeat timer , it is the max number of second between heartbeat request that are send from the registering network function to the NRF , the purpose of heartbeat timer is to indicate the registering network function , is still alive in the network , and the time difference is between the RNF and NRF is also given by the NRF .
* As indicated by the NRF , the periodic heartbeat messages would be send by the registering network function to NRF ,and thesemessages also be send using the MFManagement service , but here the operation would be change like NFupdate , and this request would be send using HTTP PATCH method because , here we are performing the update and this HTTP PATCH request to the same URI , and the NRF will repsone using the same formate execpt the change that there is response instead of the request , it would be the 200 okm message , that indicate that the NRF has acknowlegde that this registering network function is alive and everything is fine .

# Use Case 2 : NF Service Discovery :
* How these services provided by the network function are dicovered by the other network function , for eg there is a requester network function that wants discovery some services in another public lan mobile network , so then is will use NFDiscovery service or the NRF , that is loacted in the serving PLMN , to send a Nfdiscover request and this request would be recived by the NRF in the serving PLMN and this request is actually send using the HTTP GET method , because this request is meant to retrive only the information , and this request is send to the URI and there is some difference at the nf-instance like ? at the end of it and the it has a query parameter , these query parameter are , names of the services that are meant to be discover , what are the network fxn types , what is the target plmn in which these servicea are need to be discover , what is the plmn requester , and what are the network slicies that supports the target services , this is request is recive by the serving plmn and then send to the target PLMN .
* the NRF in the target PLMN will then response , using the response message it has the same naming convenstion but there is a change that it is the ressponse not request,and in this response we the HTTP 200-ok that means the request is fine and then we have the JSON data body , there would be the validetity period that how much time this is vaild and then we have the Nfinstances , it are the ID of the netwrok function in the target PLMN that supports services , and the services that are being offered will be present in the NF-Profile , this infornmation would recive at the NRF serving PLMN , which then be convey to the requester network function , then it have all the necassary information , that arerequired to contact the network function that supports the services that the requester network function wants.

# What is network slice :
* There is a physical 5G network where on the top of that there is logical network called a network slice , like mobilebroadband , that servers the mobilebroadband users , and requierment is high data rate and other is massive IOT slice that is serving the machine to machine communication , requierment is the massive connectivity of the internet of thing devices , then we have mission critiacl IoT slice , that is serving the vehicle to everything to the automoives car, here the requierment is the reiliablity of the low latency , each of these slice are the seperate network itself ,  with all the necassary resources , these slices are isolated but may share resources with one and aonther , when a user is using a slice it would experience the complete separate network and the resources that allocated to a slice , they can  be increase or they can be decrease according to the demands ,also according to the users .

![1 1](https://github.com/user-attachments/assets/e11a40f1-d77c-4187-beab-9aa4db9b7a54)

The above image is the example of netwrok slicing in 5G , where user is using two slices , the first slice is the Vo5G slice , and this UE is connected to the data network , and the second slice this UE is using is the enhanced mobilebroadband slice and this UE is connect to DN through this slice , now at a time UE can olny be connected to one AMF , so thisAMF is being shared by these two slices , so and these two slices are also sharing the NRF , but each two os these slices have separte SMF , NRF , PCF,UPF . The othe UE is connected to the DN3 by the eMBB slice but in this slice the AMF is not being shared with , other slice , each of these slices are called as the Network Slice Instance ( NSI ), the network function that are used by these like SMF , NRF etc , these are virtualize network fxn , that  means that we can genarte there instances using their network fxn virtualization , and these three slices in this example have common , NSSF AND UDM .

# Single Ntework Slice Selection Assistance Information ( S-NSSAI ):
* A network slice instance is identifed by the S-NSSAI , and it has two parts ,
* the first part , is called as the slice or service type , and it is of 8bits , is its value
1 = than it is eMBB slice
2 = then means this is ultra reliable low latency communication slcie
3 = means this is Massive Internet of Thing slice
4 =  that means this is Vehical to everything slcie
5-127 = are reserved for the future use
128-255 = can be used by the operator to design it own slice types.
* The second part is called as the slice differentiator (SD) which is of 24 bits , it is used to differentiate between network slices used for different customers .

![1 3](https://github.com/user-attachments/assets/c0aac9bc-9f6d-4d19-a9d1-f3e4cc796957)

# Network Slice Subnet Instance ( NSSI ) In 5G:
* Now ,NSI it is further compose of NSSI  ,the above image is the eg , where the RAN is divided into two parts , then slice one NSSI5, and slice two NSSI6 , the NSI 1 is composed of NSSI5,NSSI2,NSSI1 , furthere NSI2 is composed of NSSI5 , NSSI1 AND NSSI3 ,and NSI3 is composed of NSSI6 AND NSSI4 .
* So the NSI is composed of one or more multiple slcie subnets instances .
* A NSSI may contain one or multiple virtualized functions, it may consist of NF and  other NSSI ,it can be shared between two or more NSIs , and it may conatin the core network function or  Access network function or both .

# Network Slice Instance ( NSI ) lige cycle :
* It can be divided into four phases :
* Phase 1 - Preparation phase , during this phase , we prepare a network slice template , that means that we decides what are the resources , that are requierd for this NSI ,
* Phase 2 - In second phase this template is instantiated , configured and activative , in other words we assign all the other network resources for this slice , then we configured it and then we activate this slice .
* Phase 3 - In third phase , the network slices run .
* Phase 4 - In fourth phase , we decommission it , that means that we deactivate it and release all the resources that had been given to this network slice
* The task that are given in NSI life cycle is managed by the Network Slice Management Function( NSMF ).

# PHASE 1 - PREPARATION :
* A NSI template or blueprint ,list all the necessaryu attribute of Network slice , like what are the resources required for the NS , and if here is an exixting network slice template , and meets the customers requierment , we can use this network slcie as it is or we can scale this network slice template according to requierments of the user , then the perparation phase can be shotern , and is if we are using this network slice template as it is then , this preparation phase can be skiped , as we do not need to make a network slice template .
* If there is no suitable network slice template that match the requirment of user then a new network slice template needs to be desgin according to the requierments of the customers , and this newly design network slice template is then added to a catalogue of the exixting network slice template , so that if a customer comes with the same requieremnt then the perparation phase can be skiped or shorten .while design the network slice template we also make the network environment preparation , so that this network slice template needs to be activated , then it can be activated easily .

# PHASE 2 - INSTANTIATION CONFIGURATION AND ACTIVATION :
* All the resources that are requied by the , NSI these resources are created and configured , and these resources may be shared or dedicated resources , and the another name of the creation of resources is the Instantiated , and then once it is done then in the next step , we need to activate the NSI , that means we need to diverte the traffic to NSI and we provide the database to this NSI , that are required for the operation of the NSI .

# Phase 3 - Runt time Phase :
* NSI  is capable for handling the active traffic , and during this phase the performance of the NSI , is monitor using the Key Performance Indicators reporting , if there is voice5G than this is monitor by the dropping of the 5G voice calls , if the dropping of the 5G voice call is low and thisi mean the performace of this NSI is bad , if the performnace is bad , then as a part of the supervision of NSI , this NSI may need to modify , eg this NSI is needed to be reconfiguered or cpacity may need to be chanege or its toplogy may need to be change , topology means how the NF is connected to each other in NSI , or as apart of the modification we ned to add or delete some NFs .

# PHASE 4 - DECOMMISSIONING PHASE :
* This means that the NSI has reached to the end of its life cycle , and it is de-activated and the dedicated resources , that had been assigned to this NSI eg , like dedicated NFs , they are now free , and  the shared resources they are now being reconfigured  for some other use after the decommissioning this NSI is terminated , that means this NSI no more exits .


# Netwrok Slicing Managemnet Model CSMF, NSMF , NSSMG :
* In thismodel at the top we have customer which is using a communication services , and this services is provider by the services provider , nd this service is based upon the network slicing and the communication service provider uses the network slice provider , it is the network operator  , this network slice provider using the services of the network slice subnet provider , it can be the same network operator , or it can be a different operator , now , the user gives it requierments in terms of the communication services that wants to use to the communication services provider , it uses the Communication Service Management Function , in order to translate these requiremnts , into the requiermnet if the network slice , in order to provide the service , , the network slice requierments are , what is the network type , network capacity and what is the QoS requirments the would be used , then these requierments are given to network slice provider , it takes these requierments and it hase the Network Slice Managemnet Function , and this fxn is used for overall the ,management of the network slice instance , and NSP , used the NSMF , in order to translate the network slice requierments , into the requierments of the , network slice subnet and then this gives these requierments about network slice subnet to the provider . Now the network slice subnet provider takes these , requierments and it uses the slice subnet fxn in order to manage the network slice subnet according to the given requierments .

# Radio Acess Network Slicing :

![1 4](https://github.com/user-attachments/assets/10148856-de88-44c4-9724-bbe77decd79f)

* In the above eg it is showing the Netwrok Slicing Managemnet Model in the Radio Acess Network , and here the customer is giving its  requierments to CSMF , it is translating those requierments , into  the requierments of the network slice and these  requierments are then given to the NSMF , it is responsible for the overall management of a, network slice instance , and this NSMF also translate it requierments which are obtain from the CSMF , into the requierments of the network slice subnet , and giving those requierments to the NSSMF  , since we are talking about the network slicing in the RAN , so this NSMF is of the RAN NSSMF , and we know that the RAN can be divided into two main parts .
* First , Central Unit
* seconf , Distributed Unit
* In the CU we are also duing these slicing , and we are dividing it into three slices , First slice is the Massive machine type communication , the second slice is the Ultra reliable low latency communication ,and the third slice is the Enhanced mobile broadband communication slice .
* In the DU side we are also doing the network slicing , and we are doing it by assiging different , physical resource block to different network slices , and we can also use AI/ML in order to make this slicing more efficent , so this RAN intelligent controller , is based upon the AI/ML techinques it is monitoring the performance of these slices and then it is taking the apporpiate action to optimise these slices , on the core network side , we also have a network slice subnet managemnet function it would of the core network to manage the core network slicing fxn.

# Slice Availability in the 5G Network :
* The Network Slice Selection Assistance Information (NSSAI) it is a set of the single - NSSAIs.
* And these NSSAIs are managed at the tracking aarea network in the 5G Access network and they are managed at the registration area level in the 5G Core network, and a registeration area is a list of the tracking areas in which the common set of slices is avilable .

# Signaling related to Slice Availabilty :
* The avialablity of these slices are exchange between the various network function , in the 5G network , these infomation exchange between the NSSF and AMF in the N22 interface and it is exchange between the AMF and gNB to the N2  interface and between the gNB on  the Xn interface
* Now we know that every wireless network has the Operation and Maintance Center , and using it , the operator can conifured and it can nmanage the wirless network , similarly in the case of the 5G network operator can use the OMC , in order to conifured the NSSF , and it stands for Network Slice Selection Function , it configured the NSSF about the avialibality of the network slices in  the 5G network , similaly the operator uses the OMC to configured gNBs and it configured the gNBs about the netwprk slices that are ,assocated with the tarcking area of the , gNBs .
* Now when every the N2 interface is set-up or it is configured or it is updated the gNB provided information to the AMF about the S-NSSAIs that are associated with the TA of the gNB and similarly the AMF provides the information to the gNB about the network slices that are avilable in the network and which are supported by the AMF
* Similarly when the Xn interface is set-up, or it is updated or reconfigured , the gNB exchange information one another , and the information provided by the one gNBs it is about the network slices which is associated with the TA of this gNB.
* Now when ever the N22 interface is change or updated the AMF provides the information to the NSSF , about the network slices that are avilable in the different tracking area that are associated with the AMF , and at the same time the NSSF , provides information to the AMF , about the network slices that are restricted in the different tracking area of the numbers .

# Network Slice Selection Function (NSSF):
* It is very important fxn of the 5G core network , and this NSSF provides the serviecs to the other AMF and to the Other NSSFs, and there are two type of services that are provided by the NSSF .
* First service is NSSAIAvailiability service that means this NSSFs updated the other AMFs and the other NSSFs about the network slices that are avilable in the network and what are the TA these slices are avilable and what are the AMFs that supports these network slices . Similarly the AMFs and NSSFs ,can query the NSSF .
* Eg , there is an AMF and it is associated with the gNB , and we have an UE , if the UE wants , to registor itself with the 5G network, then this UE make a request to the network and in that request , it would porvide the network slice that it want to use , however the information about the network slices is not provided to the UE , or that network slice can not be serve , or it cannot be supported by the AMF , then the AMF query the NSSF , and the NSSF , would then provide the information , of the network slice that should be given to this UE along with the AMF , that suppports that network slice along with network repository fxn for that slice .that supportes the network slice that is assign to this UE .   

# 5G ROAMING ARCHITECTURE :

![493bff0b-63fb-4d09-aca2-0c09683da0ec](https://github.com/user-attachments/assets/c97fc60e-4d17-4bd5-9175-5b1d1e507b72)

* The understanding of the 5G roaming architecture is important , it enables us to understand the sercuirty architecture that is there in the 5G network , In the above image the mobile has roam into a visting public lan mobile network , and on the right side of the red line is home visting public lan mobile network . The UE is currently is served by the VPLMN's AMF , we know that for the authentiaction we need three entities , AMF , AUSF AND UDM .This UE use AMF of the VPLMN and AUSF , UDM of HPLMN , this means that VPLMN , HPLMN plays the important role for theauthentication of the UE .As concern of the data traffic flow the ,between UE and gNB and from the gNB to V-UPF, then to the H-UPF and then to the Data Network.

# Logical Entities for Network Access Security :
* The purpose behind the separation of the logical entities for securiy is used to maintain a logical security architecture there in the 5G network , these entites are corelated inside the 5G core network function .
* Logical Entities:
* ARPF ( Authentication credential Repository and Processing Function ) it is located inside the UDM .
* AUSF ( Authentication Server Function ) it is also co-located inside the UDM .
* SEAF ( Secuirty Anchor Function )
* SIDF ( Subscription Identifier De-concealing Function )
* So all the network access secuirty function that are associated with the UDM, are basically handle by the SIDF and ARPF . similarly you have the , authentiaction server function it is the logical entity for sercuirty but itself a network function .
* Similarly for the AMF , secuirty function are handle by the SEAF and in the UE , the network access secuirty fxn are handle by the logical entity .

# ARPF ( Authentication credential Repository and Processing Function ):
* It is the one of the most important logical entity , that is related to the network secuirty , it is colocated inside the UDM , and it is veryimportant because , it contain the subscribesrs security credential , related to the sercurity , subscribesrs security credential it is the long term / master key , and is denoted by the K . this key is important because it is used in the mutual authentication like when a UE authenticate itself with the network or vice versa in both cases this master key is invole.
* Similarly the other keys that are used in the Ciphering and the Intergrity protection of the data as well as of the signaling are dervide form the master key , this master key is inside the ARPF , in ARPF there is the SUPI , we know that the SUPI is the permanent ID of a subscriber , the interface between the ARPF AND UDM is not defined in the 5G standard this ,means that this is not an open interface .

# SIDF ( Subscription Identifier De-concealing Function ):
* We know that when we power up the UE does not have the temparory ID of the network , and this UE needs to register itself with the network , for the registeration process This UE needs the ID and the permanent ID is SUPI , now the SUPI is not send over the it is not send over the ait interface rather it is encrypted as SUCI then it is send over the air interface , then this SUCI is send to the AMF then to AUSF then to the UDM , in UDM it comes to the SIDF , and it is responsible to dencryte the SUCI it means that it dervies the SUPI form the suci

# AUSF ( Authentication Server Function ) :
* It is a standalone network function that is loacted in the 5G core network , a UE may be in the home network, or may roamed into some other network, but the AUSF that a UE , is going to use ,for the authentication purpose , it would always be located with the home network , it function is of authentication , based upon the information that it recives , from the UE and information form the ARPF form the UDM .

# SEAF ( Secuirty Anchor Function ) :
* It is colocated inside the AMF , and it is responsible for handling the authentication fxn related to the AMF , an UE may be in the home network or it may have roam into another network , if it is in the home , it will use the AMF of the home network , if this UE is romaing in some  other network , use the AMF of that network , so UE is always attach to AMF , of the serving network , and that AMF it is the SEAF , that is responsible for the handling the authentication related fxn , so this SEAF serves as the security anchor for this network .
* Also the term Secuirty Anchor is used because this UE cannot directly communicate with the AUSF , or the UDM for the authentication , rather it would always communicate through the SEAF .

# Network Access Security:
* It comprises to all those fxn , that are related to the secuire to the UE , to the network and the most imp part of this access network secuirty is the , Muttual Authentiaction .
* When we power up the UE it need to connect itself with the network , or when this UE wants to make a call , or whn it moves from one TA to another TA , it nedd to update its loaction with the network , in all these cases , mutual  authentication required . That means that the UE is chanlleged , network in order to proof genuies , that means the UE authenticate itself with the network , and it is mutual  authentication then not only UE needs to mutual  authenticate itself with the network but the network also needs to  authenticate itself with the UE , and  for this mutual  authentication , needs to be a signaling between the UE and home 5G core network .
* The UE and network must supports two authentication method ,
* First case for the 3GPP access , eg there is the 5G UE , that is connected 5G access network ,in which we have a gNB and UE is connected with gNB , the authentication that is carried out UE and home 5G core netork is called 5G AKA ( 5G authentication and Key Agreement ) , but there can also be other scenario where we have WLAN device that is connected with the WLAN access network in that case the authentication procdure need to be carry out , it is called as the EAP-AKA( Extensible Authentication Protocol - Authentication and Key Agreement )and it is between the UE and home 5G core network .
* Once the authentiaction is compelete , the Ciphering and the intergrity protection keys are genrated ,now there are two cases ,
* First one is , the signaling that is going on between the gNB and the AMF , so this signaling needs to be ciphering , it is recommeneded by the 3GPP , that it should be ciphered whenevr the regulation is permitted and talkin abouit the intergrity protection of this signaling is mandaotry according to the 3GPP , execpte when there is any emergency calls .
* Similarly the siganling that is going on between the UE and gNB , whiich is called as the RRC ( RADIO RESOURCE CONTROL SIGNALING ) it is recommended it is ciphered whenver the regulation is permited and similarly it is mandatory that this siganling has the intergirty protection except the emergnecy calls, similarly the data that flows between the UE and gNB it is recommended that , it is ciphered whenver the regulation is permited .when the data flows from UE to gNB , then it goes to the UPF , and then data network and vice versa it falls in the domain of network domain secuirty .

# Initiation of Authentication :

![1 5](https://github.com/user-attachments/assets/94cd28c0-37c3-4b4c-a40f-343e61b2dd1b)

* In the start UE sends , the N1 msg to the AMF ,it is called N1 because it send over the N1 logical N1, this the logical interface because , actually the signaling between , UE and AMF which is passess by the RAN , if this is UE previously it was register with the network , it would have temprary identifier , 5G-GUTI , and it is not register itself , then it would use permanent SUPI , but SUPI is never sent on the air interface, it  is first encrypte as SUCI , send it the N1 interface , now the N1 recive by the AMF ,  it is the SEAF which is invole in the security function  in the AMF , so then msg go to the SEAF then it genrate , another msg for the AUSF , in this msg eithere there will be SUPI or SUCI , another parameter will be the sending  seving network name which is in the form , it contain MNC , MCC .
* Onec AUSF recives this msg it would genrate , another msg , and this msg is genrated by the UDM , it recive the msg and if it recives the SUCI then it need to deconseale the SUCI to determin the SUPI , if it recives the SUPI then it does not need to deconseale .So based upon the SUPI , UDM would detrimine that which type of authentiaction method need to be used , as we know for 5G devices we use 5G-AKA , and for the non 5G devices we use EAP-AKA , when UDM genrate the the response of the Numdrequest msg , then the response would have  the same formate , execpt of request there will be the response .

# Concealement Deconcealement of SUPI :
* So at the start of the authentication procedure the UE , sends the 5G-GUTI if the UE has previously register itself with the network , but if not , then the 5G-GUTI is not avilable , 5G-GUTI is the temporaly ID which is much safer to use , it is not avilable then SUPI needs to be used , but it is permanenet ID of the subscriber , and it is never send on the air interface because it can be catch by the emzycatcher , so this SUPI is encrypted by the UE , as SUCI then it is end over the air inetrface .
* When we talk about the formate of the SUPI , we have SUPI type , MCC , MNC and  MSIN .
* SUPI type indicates wheter the 3GPP , SUPI or non 3GPP SUPI , because in the 3GPP we use emzy but in not 3GPP SUPI we use other identifiers, so it is actually mobile subscriber identification number , that is encrypted , by the home network public key , and after the encryption the MSIN is conceale ,and also the ID of the key is end in the SUCI , the type of encryption was use then in the schem ID and then we have the routing, indicator which is the identifier , and MCC ,MNC are send as the Home network ID and supi type is send as it is .
* When this SUCI is reaches the UDM , it needs to extract the SUPI , form the SUCI , an dthis extraction is carried out using the private key that is only avilable with the network , but it can decrpte the public key , which is easily avilable , but private key only with the network and it can decrypte the public key , so this private key along with the scheme id is use to  decrypte the MSIN , after decryption we get the mcc,mnc aupi type so that will the complete supi that has been deconceale

# 5G AKA Procedure :

![1 6](https://github.com/user-attachments/assets/73c93d61-2a44-40bd-9468-bff874418df1)

* Once the authentication has been intiated , then the UDM has the SUPI , based upon SUPI the UDM decides that it has to use the 5G AKA procedure , or  5G EAP-AKA procedure .
* Here we are talking about 5G AKA Procedure , in this procedure the ARPF genrates the , 5G home enviorment authentication vector , it is called so because the AUSF and the UDM  are in the home network , and the indication have the four parameter , AUTN which is the authentication token it is send to UE and using this the UE would verify that this is the genuin mobile network that this UE is connected that means this AUTN is used for the authentication of the mobile network ,RAND Random number that is genrated by the ARPF , XRES* we have respose to the random number the response number is calculated using the Milenage function and the inputs to the milenage fxn are the sequence number , random number the suthentication management field and the master keythat is used to derive other keys this fxn has five sub fxn first one genrates the MAC message authentiaction code , then the response to the random number then the CK key , then the IK key and AK then we take exclusive of the SQN with the AK an then we concatinate with the AMF and MAC to genrate the AUTN ,here we have genrated the XERS , AUTN , biut we have XRES* , that means we have to genrate it from the XRES this is done using the key derviation fxn and this fxn is the  ash fxn which is  HMAC-SHA-256 KDF fxn and the inputs to this hash fxn , are K which is the concatination of CK || IK the hexadecimal number is the 6B the P0 which is the name of the serving network , L0 which is the length of the name of the serving network , P1 which is the RAND ,L1 which is the length of the RAND , P2 which is the XRES which has been genrated by the milenage fxn and L2 ehich is the length of the XRES , so using all these inputs we calculate the XRES* ,K_AUSF it is genrated which is then used to genrate the other keys down in the heriachy and this key is genrated using the hash fxn HMAC-SHA-256(K,S) KDF(Key Derivation Function) it has the inputs of the concatination of CK || IK the hexadecimal number is the 6B the P0 which is the name of the serving network , L0 which is the length of the name of the serving network P1 which is the exclusive OR of SQN and AK and L1  which is the length of P1 .
* Once this authentication vectore has been genrated and goes to AUSF , it use K_AUSF key KSEAF key an dthe AUSF stores this with itself for the , time being , this KSEAF key is genrated , using the key derviation fxn which has its inputs as the hexadecimal number 6C , serving network name oand its length , and K_AUSF key is the input and so we get the K_SEAF key , the AUSF uses the XRES* to calculate the hash of XERS* and this HXRES* is calculated using the hash fxn , and the inputs of the SHA-256 hash is concatenation of the RAND || XRES* as a we get the HXRES* by taking the 126  most signifcant bits of the results we keeps the result .
* Now the AUSF sends the 5G serving enviorment authentication vector to the AMF , it is called so because the AMF is located in the serving area of UE and this AV has thre parameters  , AUTN ,RAND , HXRES* so SEAF stores the HXRES* itself and sends the RAND ,AUTN  to the uE and it comes into the ME and then from the ME these two parameters RAND ,AUTN are send to the sim and inside the sim the AUTN is used to verify that this is the genuin mobile network and at the same time the RES ,CK,IK keys are also genrated and they are genrated using same Milenage fxn . and here it is used in the sim , here AUTN has the MAC ,AMF ,exclusive or of SQN and AK we take is to calculate the sequence number similarly we used the random number input in the f5 fxn to get the AK and this AK is used to genrate the SQN , and here we calculate the XMAC using the f1 , then we compare it with the MAC if they both are the same then this means it is the genuin mobile network to which this UE is connected , similarly  this is also verfied that the SQNs lay  in the vaild range and here we get the response to the RES, CK , IK keys as vaild .
* So this response to the RAND , CK ,IK are then send to the ME and then ME calculates the RES* and then we dreived the K_AUSF key and it is dervide to genrate the KSEAF key and it is used to dervide the KAMF key  and using the KAMF key the ME dervies the lower level key that are used in the ciphering and the intergrity protection , and then the ME send the RES* in MAC to the AMF and inside SEAF the AMF actually calculates the HRES* from RES* and HRES* form the stored HRES* and if they are same thenthat means that it is good so the AMF power the RES* to the AUSF ,and it compares the RES* with the HRES* and if this comparision is good then it means the authentication is successful , and after that AUSF send the K_SEAF KEY TO AMF then it genrates the KAMF key and form the KAMF key the lower level keys are genrated that are used for the ciphering and the intergirty protection on the network side and so after the 5G AKA procedure which stands for Authentication and the key Agreements that means not only there has been mutual authentication the network has authenticated with itself to the UE and  the UE has authenticate itself with the network, authentication has been conmplete also the lower level key have been genrated that are used for the ciphering and the intergirty protection .    

# 5G Security Key Hierarchy :

![1 7](https://github.com/user-attachments/assets/bc021210-3238-48c1-8f58-5a93150a89a5)

* On the Network side , master key denoted by K , located in the ARPF , and it is used to dervie CK, IK keys and these CK and IK then used to dervie the KAUSF in  the ARPF this key then pass to the UDM and and from UDM it is passes to the AUSF , and in the AUSF , the KSEAF is dervied and this key is then passed to the SEAF , then we dreived KAMF from that key then pass to the AMF , then KAMF is used to derive the KNASint ( KNAS intergrited protection ) and KNASenc ( KNAS encrypted ) it is used for the encryption for the signaling there between AMF and UE , and here we also derived the Kgnb key it is then handed over to the gNB and it resides in the gNB till UE is in connected state and this kgnb key is used to dervie the Krrcint or Krrc intergrity protection , that menas that the signaling going on between the UE and the gNB , it is called as the RRC siganling ans this key is used for the intergrity proctection , and for the encryption for this signaling , Krrcenc key is used , and for the data that is flowing form the uE to gNB the Kupint ( K user plane intergrityprotection key )for the intergrity protection of the data Kupenc key used for the encryption data  .
* Obiviously when we have this key on thge network side we need this key on the UE side , on the Ue side this master key K , is in theUSIM an dthen from it we derived the CK,IK in the USIM and   it is given to the ME then we derived it to kausf key form it we derived Kseaf then Kamf key then to  derive the KNASint ( KNAS intergrited protection ) and KNASenc ( KNAS encrypted ) it is used for the encryption for the signaling there between AMF and UE , and here we also derived the Kgnb key it is then handed over to the gNB and it resides in the gNB till UE is in connected state and this kgnb key is used to dervie the Krrcint or Krrc intergrity protection , that menas that the signaling going on between the UE and the gNB , it is called as the RRC siganling ans this key is used for the intergrity proctection , and for the encryption for this signaling , Krrcenc key is used , and for the data that is flowing form the uE to gNB the Kupint ( K user plane intergrityprotection key )for the intergrity protection of the data Kupenc key used for the encryption data  .
* K_hNB is then passed to the eNB/gNB and this key is stored thre till the UE is in CM-Connected mode once it is over then that key is no longer provided .
* Like in LTE the encryption and intergrity keys are 256 bits long in the 5G but then these keys are truncated to 128 bits for use , future there is the provision 256 bits key the lower level keys are called so because if we see the OSI model these keys are used just above the Physical layer , that means the data link layer and physical layer these keys are used to encrypted the data , of all the upper layers knowing in these respected entity .
* Ciphering / Intergrity Algorithms in 5G :
* Like in lte we have  128-NEA1 called Snow 3G , we have 128-NEA2 as AES , we habe 128-NEA3as ZUC.

# 5G EAP-AKA for non-3GPP Access Architecture :

![1 8](https://github.com/user-attachments/assets/60a9123b-2241-460d-bd7c-bf884b318363)

* It is used for the authentication of the non-3GPP devices when they want to connect to the core network , if the UE is the non-3GPP , it would connect to the access point to the WLAN and this Acces network which is non-3GPP in order to connect to the network it would need the protocol convertion it adoptation , this protocl converstion , provided by N3IWF and this stands for Non-3GPP access InterWworking Function as it always interworking of the Untrusted Non-3GPP Access , which works with the 5G core network and the authentication is carried out with the core network then this non-3GPP device which is WLAN in this case is carried out using the 5G EAP-AKA.
* It stands for Extensible Authentication Protocol-Aauthentication and Key Agreement , it is defined in the IETF , in RFC 3748 , it is an organization , which makes the standard for the internet protocol , and standardises them as RFC-3748 , it is the protocol that is used for the authentication , typically between an end-user device and a network it was also used for the PPP , EAP is not itself is an authentication method , but rather a common authentication framework to implement specific authentication methods . Also new methods can be implement so EAP is therefore known as "extensible" as it supports for different authentication methods , also new authentication methods can be added .
* ## 5G EAP-AKA':
* EAP-AKA' is an EAP method defined by IETF in RFC 5448 for performing authentication based on USIM card , in this case we generate a transfromed Authentication Vector (AV'), it is called so , because it consists of five parameters:
* random Number (RAND)
* respond to that random number
* AUTN
* CK'
* IK'

![1 9](https://github.com/user-attachments/assets/58c8f1c3-0924-463e-a529-47379c59a6ee)

* The UDM would genrate the transform authentication vector in ARPF , and would concict of 5 parameter , these AV is then given to the AUSF , keep XRES, CK', IK' with itself, and it would calculate the message aythentication code and it would genrate the key KAUSF and form it , it will generate the KSEAF , and it will keep the KSEAF with itself , but it forward the RAND , AUTN and the message authentication code , the the EAP-request / AKA challenege to the AMF , and AMF would challenge the UE using these three parameter , and UE consist of the ME and USIM , and ME will keep the MAC with itself and forward the RAND , AUTN , to the USIM , and using the AUTN , the USIM will verify that this is the genuin 5g network to which it is connected , and then it would use the RAND and the ciphering key that is there in the USIM , to calculate the response to the RAND the keys CK,IK and this response would be given to UE , it verify the MAC which is recived from the UDM , is a valid MAC or not by calculating the MAC itself also and then it would genrate the KAUSF key from this it would generate the Kseaf key from this it would generate the Kamf key and the response to that challenge UE send the RES and the MAC key to the AMF and the AMF would then forward the RES , MAC to the AUSF , here one important point is that , AMF is just forwarding the msg ,it is not calculating any hashes or doing any comparison , so this is the main differnce between 5G AKA and the 5G EAP-AKA , once the RES response the RAND, the MAC reach to the AUSF , the AUSF will compare the RES with the, XRES and check with it is a valid response or not , also it would verify the MAC that it has recive and if the comparision is good that means two parameter are correct the AUSF would send the KSEAF key to AMF would then derive the AMF key from the KSEAF key and it will keep the AMF key itself .then it will informs the UE that authentication is the success

# 5G Secuirty Key Hierarchy for the EAP-AKA':

![2 1](https://github.com/user-attachments/assets/86199f5d-b38c-442e-a1c7-05c24c07a7b9)

* Network side the master key is the K , and which from all those keys are genearated is actually in the UDM more precisouly ARPF, this key is located , and from thiskey we dervie , CK ,IK keys and from these keys we get the CK', IK' keys and these keys are then pass to the, AUSF and AUSF derives the Kausf key , this key then pass to the SEAF , and it generates the Kamf key from the Kseaf , and from this Kamf we derive the Kmnsiwf ,key , then this key is then pass to the N3IWF that is connected to the non -3GPP access network , and this communication that is , between the UE and the N3IWF , it is encrypted using the IPsec protocol we need the security association , for the establish of the secuirty association ,between the UE and N3IWF we use the key.
* UE side , the master key is in the USIM and we generate theCK,IK in USIM then we gave the keys to ME , which generate the CK',IK' and within the ME then we derive the Kseaf key from Kausf and then we generate Kamf key then we derive the Kn3wif key which is located in the ME and it used from the UE side to establish the IPsec security association . 



























