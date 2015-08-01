#Lab1 Nmap Vulnerability Scanner

##What is Nmap?

Nmap(Network Mapper) is a vulnebility scanner.It can identify the operating system of the target,names and versiond of the listening services,estimated uptime,type of device,and presence of a firewall.

##Nmap Features
###Host discovery - 
Identifing hosts on a network such as listing the hosts which respond to pings or have a particular port open.

###Port scanning -
Enumerating the open ports on one or more target hosts.

###Version detetion -
Determine the application name and version number 

###OS detection -
Remotely determining the operating system and hardware characteristics of network devices.

###Scriptable interaction with the target -
Using Nmap Scripting Engine(NSE) and Lua programming language,customized queries can be made.

####In addition to these,Nmap can provide further information on targets,including reverse DNS names,device types,and MAC addresses.

##What is Zenmap?
Zenmap is the official graphical user interface(GUI) for the Nmap Security Scanner

###To start Zenmap, navigate to Application->Kali Linux->Information Gathering->Network Scaners->Zenmap

####This is the main Zenmap window

![image1](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xpt1/t31.0-8/11807729_756030904523303_7247022901618886201_o.jpg)

####You can provide Target IP Address or range of IP Addresses.(Remote machines).

![image2](https://fbcdn-sphotos-g-a.akamaihd.net/hphotos-ak-xtp1/t31.0-8/11705789_756031017856625_6980307409188541758_o.jpg)

####Zenmap comes with 10 profiles that can be chosen. If the provided profiles are not suitable for our needs we cab create our own profile by creating a new profile or editing the existing ones.These tasks can be found under the Profile menu.To create a new profile,select the menu New Profile or Command or you can press the keys Ctrl+P.

![image3](https://fbcdn-sphotos-c-a.akamaihd.net/hphotos-ak-xft1/v/t1.0-9/11207274_756030997856627_5316739174118017106_n.jpg?oh=66f70657ef4090d882c1e3bdb6012f5e&oe=56537BC7&__gda__=1448016717_a21a18a186d64d8b25aee832054882b9)

####Select each tab and configure it according to your needs.

![image4](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xta1/t31.0-8/11144475_756031041189956_9201556119686915458_o.jpg)

####If you have finished configuring the profile,save the profile by clicking on the save changes button as shown in the following screenshot:

![image5](https://fbcdn-sphotos-c-a.akamaihd.net/hphotos-ak-xpt1/t31.0-8/11807644_756031131189947_6340083227695606352_o.jpg)

####Lets scan the host 192.168.56.1-254 using the Regular scan profile as shown in the following screenshot:

![image6](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xtf1/t31.0-8/11807322_756031117856615_4774114802924949262_o.jpg)

####Lets scan the host 172.16.100.216 using the Quick scan profile as shown in the following screenshot:

![image7](https://fbcdn-sphotos-b-a.akamaihd.net/hphotos-ak-xtf1/t31.0-8/11754755_756031147856612_637275708367781199_o.jpg)

####You can see the Topology as follows

![image8](https://fbcdn-sphotos-g-a.akamaihd.net/hphotos-ak-xtf1/t31.0-8/11728926_756031184523275_7617336554118155994_o.jpg)

####Lets scan the host 172.16.100.216-236(range of Ip's) using the Quick scan profile as shown in the following screenshot:

![image9](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xtf1/t31.0-8/11782442_756031217856605_7285106546897832705_o.jpg)

####After the scan completed you can go to each host and search for vulnerbilities

![image10](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xfp1/t31.0-8/11807624_756031214523272_1599706866204078289_o.jpg)
![image11](https://fbcdn-sphotos-e-a.akamaihd.net/hphotos-ak-xpt1/t31.0-8/11754288_756031267856600_3330279572619200393_o.jpg)
![image12](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xpf1/t31.0-8/11816332_756031297856597_7164007679350116198_o.jpg)
![image13](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xpt1/t31.0-8/11741310_756031294523264_7684176376722102227_o.jpg)
![image14](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xfp1/t31.0-8/11045851_756031327856594_9203555942981236992_o.jpg)
![image15](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xpf1/t31.0-8/11163968_756031371189923_1971812580308733241_o.jpg)
![image16](https://fbcdn-sphotos-g-a.akamaihd.net/hphotos-ak-xpa1/t31.0-8/11794276_756031387856588_1480455964647527294_o.jpg)

####To save Zenmap scan results,go to the scan menu and choose save scan.Zenmap will ask you where you want to save the result.The default format is xml as shown in the following screenshot

![image17](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xpt1/t31.0-8/11792017_756031404523253_4203082806273118909_o.jpg)
![image18](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xft1/t31.0-8/11037010_756031447856582_3572514036995915115_o.jpg)
![image19](https://fbcdn-sphotos-g-a.akamaihd.net/hphotos-ak-xft1/t31.0-8/11782393_756031454523248_7273306924718546632_o.jpg)

####To find the differences between the scans,perform the first scan and save the results.Then make changes to the scan targets .Next,do the second scan and save the result.Later compare the scan results by going to the Tools menu and select compare results.

![image20](https://scontent-sin1-1.xx.fbcdn.net/hphotos-xtp1/t31.0-8/11146658_756031484523245_2689906668827014639_o.jpg)

####We did this practical by using KALI LINUX os because zenmap is pre-installed inside KALI LINUX
 
![image21](https://fbcdn-sphotos-b-a.akamaihd.net/hphotos-ak-xaf1/t31.0-8/11823015_756031504523243_5158467374069286807_o.jpg)

