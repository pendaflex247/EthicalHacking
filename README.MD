#The Five Stages of Ethical Hacking 

1. Reconnaissance (Information Gathering)
    -Active
    -Passive
2. Scanning & Enumeration
    -Nmap
    -nessus
    -nikto etc.
3. Gaining Access ("Exploitation")
4. Maintaining Access
5. Covering Trackes (Cleaning up)

#keep your wheel spinning 


1. Reconnaissance (Information Gathering)

Physical and social:

    location information:
        Satellite images
        Drone recon
        Building layout(badges reades,break areas,security, fencing )

    Job infomation:
        Employees (name, job title, phone number, manager, etc.)
        Picture(badge photos, desk photos, computer photos, etc.)

Web/Host:
    1. Target validation:
        always make sure you validate your target before anything else
        WHOIS, nslookup, dnsrecon

    2. Finding Subdomains:
        tools; google fu, dig, Nmap, Sublist3r, bluto,crt.sh, etc.

    3. Fingerprinting:
        Nmap, Wappalyzer, Whatweb, Builtwith,Netcat

    4. Data Breaches:
        HavelBeenPwned, breach-Parse, WeleakInfo

Start:

establish a client to attack
bugcrowd
always make sure the client is still a vaild member of bugcrowd

Email gathering 
1. Bugcrowd
2. Hunter.io (domain search)
    gives a list of people in the organisation
    the most common parthern of their password

    #grab a valid list of names

Gathering Breach credentials with 
    1. Breach-Parse (https://github.com/hmaverickadams/breach-parse)
        Take a look at the tool and what it does
        Download to your opt folder (44GB) lol

    Cd /opt/breach-parse/
    ./breach-parse.sh @tesla.com tesla.txt

    2. The Harvester on kali for information gathering for domail getting email and passwords
        # theHarvester

            -d specify a domain
            -l pecify how deep you want the search to go
            -b what you want to search on
            -f Output result

            # theHarvester -d tesla.com -l 500 -b google
    
    3. Hunting subdomain
         #apt install sublist3r
         
         # sublist3r  (this will just determaine a 3 level domain unlike crt.sh)

         #sublist3r -d tesler.com -t 100

         alternative way
            https://crt.sh

            on the search bar do a certificate finger printing 
             %.tesla.com
        
            Owassp Amess: google and download from github and install

    4. Identifying website technology: what a website is built with
        google 
        
        1. builtwith
        2. wapperlyzer (this is a web plugin to be installed on you browser on kali this gives you indication right away about whats going on)

        take to CMS or the programming language and for the vunerabilities with those OS, programming anguage or database

        3.whatweb
            whatweb https://tesla.com

        4. Burp Suite