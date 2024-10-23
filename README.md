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
* There are two prefix one is NORMAL and other is EXTENDED prefix , the extended one is use in  the large area , because there will be more bouncing back of the signal










