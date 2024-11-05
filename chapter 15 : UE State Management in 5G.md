# UE State Management :
* Now we know that 5G system provides services to the UE, in order to provide these services it need to keep track of the availability and reachability , of the UE , in order to achive this the 5G system keeps tracks of three states of UE
* The first state , called as the Radio Resource Control (RRC) state , this state indicate the RRC connection , that is there btw UE and gNB , so this state is btw these two , so on the netwrok side gNB that keeps track of the RRC state of the UE.
* Then we have the Connection Managment (CM) state, it indicate the states of the connection that is there between the UE and the AMF , and this connection is also called the Non-Accesss Stratum , on the network side AMF that keeps track of, the connection managment state
* Then we have Registration Management (RM) state , this state indicate whether the UE is registered with 5G network or not , on the network side it is the AMF that, keeps  tarck of this state.

# Radio Resource Control (RRC) State :
* This states indicate the status of RRC connection b/w UE and gNB, when we power-up the UE , it is in the RRC idle state , that means there is no RRC connection b/w the UE nd gNB, in the state the UE can monitors broadcaste info that it is reciving from the gNB , and based upon this info the power level management that are there in the signaling can be UE , idenify the gNB with the most powerful signal, and this procedur is called the Cell selection and if UE moves to another cell then this proceduer is called cell reselection.
* When the UE is in the RRC-IDLE state and want to register itself with the 5G system or this UE wants to make a voice call , in both the cases this UE needs to be in the RRC connected state , it does so , by establishing the RRC connection with the gNB and once it enter in the RRC connection State , this state the network know the location of the UE to the cell level.
* RRC-Inactive :It is the intermediate state between the RRC-IDLE and RRC-Connected state , and this state was not there in the 4G, it was introduce in the 5G in order to save the battery . When UE is tranfering data with the gNB and there is some Suspention or dely in that so , the RRC connection suspend the connective state in the RRC-Inactive state and the parameters are store in the UE and gNB, this is called as the RRC connection context .
* Now if the UE again wants to transfer , the data to gNB then it would resume the connection and enter to the RRC connection state again, but it resume this activation with the minimum signalling , this decreases the load of the signalling, and it increases the battery life of the UE   , and this state is specailly useful in the massive IOT .

# UE Mobility in RRC_Inactive State:
* Inorder to understand the UE Mobility in  RRC_Inactive state , first we have to understand the RAN area.
* RAN area are very similarl to the tarcking areas , but they are relevant to the RAN, and the min size of the RAN area is 1 cell of TA ,, max size of a RAN area is all the cells of the TA .
* RAN area do not over lap , with each other and each RAN area is identifoed using a RAN area ID.
* One or more RAN area of the same TA can be grouped as the  RAN-based Notification Area (RNAs) ,, 5G RAN assigin the RNA to a UE, when the UE is in the RRC_INACTIVE state , then RAN knows in which RNA is the UE is loacted , and when it moves from ,one cell to another RNA , the UE notifys to the RNA about it , and similarly , when RAN wants to contact the UE , it would page all th ecells that are there in the RNA  based notification area in order to contact the particular UE.
* This approach reduces the load of signaling on the network , and on thbe UE , because when UE is in the connected state and it wants to move new cell , then it has to notifys to the network , but in RRC_INACTIVE state the UE only notifies the RNA .

# Connection Management (CM) state:
* It indicates that there is a NAS connection , between the UE and the AMF or not, and this connection is also called as N1 signaling link , when CM1 is in IDLE state tyhen there is no N1 connection , and if the UE is already register and it is in the IDLE state then , it knows in which registeration area particularly AMF knows this UE is located , registeraation areas are the list of the tracking areas , that has been asigined to the UE , if teh UE wants to register itself ,or it is registered but want to tarnsfer the data , or it is register but now it is in new registeration Area and wants to register there , for all these task the UE wants to be in the CM-Connected state , it can enter into the connected state from the idle state by the RRC connection , when the UE is in the connected state the AMF knows the , in which cell this UE is currently loacted or  in other words the AMF knows in whihc gNB this UE is currenlty connected .

# Registration Management (RM) State :
* It is used to indicate the status of the regiosteration of the UE , with the 5G network .
* When the UE is in the RM-Deregistered state , that menas the UE is switched off or it aswitch on but it is deregistered with the 5G network , now the uE can move from the Deregister state to the RM-register state , by registering itself with the 5G network , more preciously this register is done with the help of AMF , once the registeration process is compelete the UE served by the AMF,this UE is assigned a tempoary ID which is calle d5G-GUTI , and in the RM-register state if the UE is roaming on moves from one registration area to another area this UE will notify to the network about the change of the registration area by perfroming the registeration update procedur .

#














