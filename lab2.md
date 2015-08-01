#LAb2 Wireshark

##What is Wireshark?
Wireshark is a powerful Network protocol Analyzer.Wireshark is a free and open-source packet analyzer. It is used for network troubleshooting, analysis, software and communications protocol development, and education.In Kali Wireshark is pre-installed.In windows you have to install it manually.
 
##PCAP
Well known format for packet capturing.Can do analyzing.

##promiscuous
Network Interface Card(NIC) is semi autonomous.Can identify the MAC address and check whether the frame is available to me or not.Layer 2 operations are enabled.
Basically promiscuous means can capture all the packets even though it is not relevant to you.

###Plain text protocols are vulnerable.So use https rather than http.SSL(Secure Socket Layer)

###You have to install wireshark in windows before you use it.   
 
##Installing wireshark
![image1](https://fbcdn-sphotos-e-a.akamaihd.net/hphotos-ak-xta1/v/t1.0-9/11800084_756178617841865_5305243461101158545_n.jpg?oh=2b359763e6349653b7443e5303733b3b&oe=5648A7A9&__gda__=1446633504_bf3cf7d896b46cd59184ed99dc7510f1)
![image2](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xpf1/v/l/t1.0-9/11811551_756178684508525_6584857753853684637_n.jpg?oh=239bda1109402015fb705944bec30108&oe=560F0B50)
![image3](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xtp1/v/t1.0-9/11800518_756178691175191_9067173891849070257_n.jpg?oh=7c6c8a5d82a372ce30a37f24bea957d8&oe=564A00C8)

###You should install pcap for packet capturing

![image4](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xfp1/v/t1.0-9/10982092_756178701175190_265186112482920607_n.jpg?oh=58832d838e6ace54dfa90716584965ba&oe=5653880C)
![image5](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xta1/v/t1.0-9/11800175_756178831175177_3439050850833293175_n.jpg?oh=d6c590f7b3a7a8f495fbaa1ae7d10363&oe=56553D54)

###This is the main window of the wireshark

![image6](https://fbcdn-sphotos-b-a.akamaihd.net/hphotos-ak-xtp1/t31.0-8/11823057_756178894508504_6895207249417701831_o.jpg)

###You have to select the capture interface before start packet capturing.Here I have selected the Ethernet interface(NIC).Also you can select the wifi interface if you want 

![image7](https://fbcdn-sphotos-h-a.akamaihd.net/hphotos-ak-xpf1/v/t1.0-9/11836697_756178851175175_5735854279216209130_n.jpg?oh=11bd58246eb265183b24ae6652fb4b1d&oe=565CA25E&__gda__=1446519604_7f874de4f8855e3492fea7756ba46333)

###The packets which are going through selected interface will be shown as bellow
  
![image8](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xtp1/t31.0-8/11699023_756179051175155_983698609484416649_o.jpg)

###When you select interfaces you can set options according to your need.

![image9](https://fbcdn-sphotos-d-a.akamaihd.net/hphotos-ak-xtp1/t31.0-8/11705827_756178924508501_233349408826922446_o.jpg)

###Wireshark has a very powerful filter.you can even use regular expressions with that filter.Here I have used http to filter http requests.

![image10](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xaf1/t31.0-8/11807272_756179301175130_442755814482860839_o.jpg)

##Lets start a packet capture to check whether what is the vulnerable protocol from http and https

###First select the interface
 
![image11](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xtf1/v/t1.0-9/11796269_756178971175163_7024703084877762432_n.jpg?oh=ea0cd3513edd9ff5c68f0a552bf746e4&oe=56456995)

###You can see packets going through that selected interface

![image12](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xtf1/t31.0-8/11779845_756179287841798_2602405744684208851_o.jpg)

###While capturing packets log in to the sliit courseweb web site or any web site that is using http plain text protocol.Then log out from that site

![image13](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xpf1/l/t31.0-8/11791993_756179264508467_3342696809634305012_o.jpg)

###Stop the packet capture and filter for http requests.

![image14](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xpt1/t31.0-8/11262319_756179731175087_8158088162718628333_o.jpg)

###Then you can easily get the user name and password that you used to log in that particular website 

![image15](https://fbcdn-sphotos-b-a.akamaihd.net/hphotos-ak-xtp1/t31.0-8/11707908_756179551175105_255863069559015297_o.jpg)

![image16](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xft1/t31.0-8/11782481_756179637841763_5757814367067312824_o.jpg)

###Again start another packet capture for Ethernet interface

![image17](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xpf1/v/t1.0-9/11822435_756179611175099_7726902206819555783_n.jpg?oh=eb895356a46ba8540511c19ff9086a5e&oe=563B66F1)

###While packet capturing log in to any web site that use https protocol.Here I have logged in to Facebook web site

![image18](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xft1/t31.0-8/11167655_756179854508408_1749536694129761069_o.jpg)

###Then stop the packet capturing and filter the SSL(https) requests

![image19](https://fbcdn-sphotos-f-a.akamaihd.net/hphotos-ak-xfp1/t31.0-8/11816115_756180117841715_766286084272743566_o.jpg)

###Here also you can capture the username and password.but the data is encrypted.So you have to decrypt it to get the relevant data.So we can see plain text protocols are vulnerable and to get rid from that we have to use secure protocols like https
 
![image20](https://fbcdn-sphotos-g-a.akamaihd.net/hphotos-ak-xaf1/t31.0-8/11794108_756180121175048_7065888195649549131_o.jpg)

###Wireshark has a very powerful filter.you can even use regular expressions with that filter

![image21](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xta1/v/t1.0-9/11800083_756180001175060_6561142225490101531_n.jpg?oh=429282971d2b267af58f4b8bb2c43969&oe=563DF421)