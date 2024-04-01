# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:
Find out the ip address of the attackers system

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/35c9a4fe-a4f0-4c2c-b99e-828fc0836706)

Invoke msfconsole:

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/d2c7b4d5-f175-499e-82d5-a7f487139c6a)

Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/b488344c-3acc-40eb-8a09-5e72f9dc55d7)

Port Scanning:

Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000
## OUTPUT:

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/94aa88c8-7234-4c4b-a009-f71de1d1925a)

USE the db-nmap command to scan and save the results into Metasploit's postgresql attached database. In that way, you can use those results in the exploitation stage later.

scan the targets with the command db_nmap as follows. msf > db_nmap 192.168.181.0/24

## OUTPUT:

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/39b1cb26-19e7-4fa5-8497-621c873adc4e)

step4:
use the db-nmap command to scan and save the results into Metasploit's postgresql attached database. In that way, you can use those results in the exploitation stage later.

scan the targets with the command db_nmap as follows.
msf > db_nmap 192.168.181.0/24

## OUTPUT:

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/5d347630-867d-4b76-a3f1-a3d8d005aa4b)

Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules.
cd /usr/share /metasploit-framework/modules/auxiliary
kali > ls -l

## OUTPUT:

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/74ebc709-90c5-401b-b99d-73046b672d51)

Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit

The info command provides information regarding a module or platform,

## OUTPUT:

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/0bd7c1d7-a69e-46f2-a126-1815a339f0cf)

Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows: systemctl start postgresql msfdb init

## MYSQL ENUMERATION
Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/074b89e1-816f-4f7a-bb13-9126925ca69f)

Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/b5fc50f6-6059-46ed-b389-ae05d4d7e65d)

use the auxiliary/scanner/mysql/mysql_version module by typing the module name or associated number to scan MySQL version details. use 11 Or: use auxiliary/scanner/mysql/mysql_version

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/b37b3ac3-95ab-48d9-b534-04f8762b50dd)

Use the set rhosts command to set the parameter and run the module, as follows:

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/30c52f1d-dd86-4432-9154-0bc89a023da4)

After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/8361a7c6-d08d-4c7f-9e7c-753ccb271f70)

set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS Set BLANK_PASSWORDS to true in case there is no password set for the root account. set BLANK_PASSWORDS true

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/8a53b404-f34c-4cf8-aa62-006c505d54c9)

## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
