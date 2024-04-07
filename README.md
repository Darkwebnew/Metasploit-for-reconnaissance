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

### Find out the ip address of the attackers system

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/7aecb6a7-dc64-41f0-9aa0-27b2efa35c9a)

### Invoke msfconsole 

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/f9c225f1-f8d1-4166-9cf4-0bd292a874e4)

### Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/cc6960c7-b86f-486a-b9a0-fa8053d477c1)

### Port Scanning:
Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000).

**msf >  nmap -sT 192.168.1810/24 -p1-1000**

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/44f9cf64-7155-4d5b-83ea-6c4e0b448e2b)

### Use the db-nmap command to scan and save the results into Metasploit's postgresql attached database. In that way, you can use those results in the exploitation stage later.

scan the targets with the command db_nmap as follows.
**msf > db_nmap 192.168.181.0/24**

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/58ad5b77-de27-4ac2-9b06-ffe12769fde5)

### Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. 
**cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l**

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/c1045991-a1e1-47f4-95cd-7daf2e6f32c0)


### Search is a powerful command in Metasploit that you can use to find what you want to locate.
**msf >search name : Microsoft type : exploit**

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/5bb981af-d434-4255-bf93-669f26290b70)

### info

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/5000e229-2fab-4c90-9dfc-7fed1821e678)

## MYSQL ENUMERATION

**db_nmap -sV -sC -p 3306 <metasploitable_ip_address>**

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/c6d1f187-7305-4bd2-a2af-4cdcbf5d5af7)

### Use the search option to look for an auxiliary module to scan and enumerate the MySQL **database. search type:auxiliary mysql**

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/6a5e0213-bc7e-4d03-9648-45bbebedf3d7)

**use 11 Or: use auxiliary/scanner/mysql/mysql_version**

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/28ed49ff-dd6d-4a08-b843-de2a7955cbb7)

**Use the set rhosts command to set the parameter and run the module, as follows **

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/826cd469-596c-4616-8e3e-2e72b92edd45)

**After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.**

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/9d89c751-660c-4474-af08-00484625a514)

**/usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt**

![image](https://github.com/Darkwebnew/Metasploit-for-reconnaissance/assets/143114486/9975b438-66c1-4727-928a-3602614825c0)

## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
