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














