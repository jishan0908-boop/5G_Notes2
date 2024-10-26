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
* Handover always take place when , UE is in connected mode , that means it is in active call or PDU session with the network , if UE is moving form one cell to another cell coverage area  












 













