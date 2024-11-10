#  Channel Bandwidth & Maximum Transmission BW Configuration :
![3](https://github.com/user-attachments/assets/ee6eb042-c0ce-401e-b5a4-85ecf9b2df6c)

* Now we have a question that what is the BW of the Radio channel that we use in operator and regulater in a given gNB.
* It depends on two factoor , first how much total BW is assigned by this regulator to this operator , secondly how much BW is used by the operator in this gNB and that BW is called as the channel BW . This Channel BW includes the Guardband , so that the transmission that are being made in this channel do not intefer with the adjcent Freq of the channel . When we subtract the Guardband BW form the channel BW we get the Transmission BW Configuration , in other words it is the total number of available resource block that are there in the gNB that can be used for the transmission and out of the Transmission BW Configuratio at a time there be the sub-set of the resource blocks that are actually being used for the Transmission and thes Active Resource Blocks depends upon the time of the day because in the evening these active resource blocks may be more , which is load on the system due to more calls at late night this active resource blocks may decrease because of less load .   

* In the frequency range FR1 the channel BW lies b/w 5 and 100 MHz .
* ![4](https://github.com/user-attachments/assets/d8602781-2175-4749-a564-2a8de8c783bf)

*  When we move to the frequency range FR2  , we can have the channel BW 50 and 400 MHz , and we cannot use 30kHz sub -carrier spaceing rather we can use the 60 kHz sub-carrier spacing or the 120 kHz sub-carrier spacing .
*  ![5](https://github.com/user-attachments/assets/96eb0d53-31df-4d3c-a2b0-24db9efef8bd)
 
# NR-Absolute Radio Frequency Channel Number :

![1 (1)](https://github.com/user-attachments/assets/43db9497-3ded-48a8-a904-98bcf44fcda0)

* When we talk about indivdual channel , there is center frequency of this channel , and this center frequency is know as Reference Frequency . This frequency has an associated number which is know as NR-Absolute Radio Frequency Channel Number , it is used to identify the channel . 5g is quite flexible in its implementation.

* ## Reference Frequency Calculation:

![2 (2)](https://github.com/user-attachments/assets/89679f57-932c-41b9-b2a8-0e52d8bb4a61)

# Difference Between Global And Channel Raster :
* When we are considering the frequency above 3GHz then the Reference frequency can act as the center frequency of the chanel , that means that the Channel Raster and the Global Raster are same , channel Raster are the distance b/w two center frequency and is the min distance b/t two Reference frequency .
* When we go to frequency below 3GHz , then the Global Raster is 5KHz that means the distance b/w two reference frequency is 5KHz , but the Channel Raster can be 15KHz or 100KHz.
* Implication : eg if we take Channel Raster of 15KHz and Global Raster of 5KHz and we divide Channel Raster by Global Raster , 15/5 = 3, so that means , if we a taking any frequency as the center frequency then the next center frequency that we can take it would be 3 steps ahead .

 # Bandwidth Part in 5G :
 *  In the case of LTE , the radio BW that can be used by a UE is usually same as the Radio BW of the eNB . But in the case of 5G the gNB BW is much larger as compare to the Radio BW , and this is because the concept of Bandwidth Part becames Important .
 *  A Bandwidth Part is a contigous set of resource Blocks , and they are the subset of the frequecny bandwidth of the gNB , that means it is the part of the BW of the gNB .
 *  Now a UE can be assign upto 4 BWP in dowmlink and upto 4 BWP in the uplink, but at one time only one BWP can be active in the uplink and only one BWP can be active in downlink. BWP can also overlap .

![3 (1)](https://github.com/user-attachments/assets/6e502630-df3d-419f-85f0-7cbc29d2b8ff)

# Resource Grid on 5G Air Interface :
![4 (1)](https://github.com/user-attachments/assets/6054347d-15b3-4178-8bee-3b86d804f57b)

* We know that the total BW in a cell is divided into resource blocks in the frequency domain , while in the time domain we have the Frames and each frames is of 10 milisec and it has 10 subframes of 1 milisec each , and if we have the sub-carrier spacing of 60KHz we will have 4 slots per subframes , and if we take one slot we will 12 sub-carriers in the frequency domain and we are using normal cyclic prefix we would have 14 OFDM symbols in the time domain and this time , frequency arrangement is known as the Resource Grid these resource as assign between the UE and gNB for the transmission of the signaling as well as data .
* Each cell or each gNB has multiple resouce grid , eg we can have one Resource in Uplink and one in the Dowmnlink , we can have different resource grid for the different antenna ports in MIMO and for different sub-carriers spacing of different frequency we can have diferent resource grid . So the number of Resource grid that a gNB or a cell supports it is the combination of direction, antenna ports, nd the subcarrier spacing configuration .

* eg:
![5 (1)](https://github.com/user-attachments/assets/6552b392-2774-4cb5-ab13-0b98ec168dc8)
* In above image there is the a gNB that has three antenna ports in the downlink and it is using 60 KHz Subcarrier spacing , that means they have 4 slots in each subframes and for the time frequency resources that are in the white they are acting as active transmission going on these time frequency resources , the time frequency resources that are in the blue tht are not being used for the transmission currently . So in this case we have three resoruce grid in downlink in this subcarrier spacing . 
























































