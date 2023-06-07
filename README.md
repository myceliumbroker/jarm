<pre><div align="center">                            
▓█████▄  ▄▄▄       ██▓ ██▓   ▓██   ██▓    ▄▄▄██▀▀▀▄▄▄       ██▀███   ███▄ ▄███▓
▒██▀ ██▌▒████▄    ▓██▒▓██▒    ▒██  ██▒      ▒██  ▒████▄    ▓██ ▒ ██▒▓██▒▀█▀ ██▒
░██   █▌▒██  ▀█▄  ▒██▒▒██░     ▒██ ██░      ░██  ▒██  ▀█▄  ▓██ ░▄█ ▒▓██    ▓██░
░▓█▄   ▌░██▄▄▄▄██ ░██░▒██░     ░ ▐██▓░   ▓██▄██▓ ░██▄▄▄▄██ ▒██▀▀█▄  ▒██    ▒██ 
░▒████▓  ▓█   ▓██▒░██░░██████▒ ░ ██▒▓░    ▓███▒   ▓█   ▓██▒░██▓ ▒██▒▒██▒   ░██▒
 ▒▒▓  ▒  ▒▒   ▓▒█░░▓  ░ ▒░▓  ░  ██▒▒▒     ▒▓▒▒░   ▒▒   ▓▒█░░ ▒▓ ░▒▓░░ ▒░   ░  ░
 ░ ▒  ▒   ▒   ▒▒ ░ ▒ ░░ ░ ▒  ░▓██ ░▒░     ▒ ░▒░    ▒   ▒▒ ░  ░▒ ░ ▒░░  ░      ░
 ░ ░  ░   ░   ▒    ▒ ░  ░ ░   ▒ ▒ ░░      ░ ░ ░    ░   ▒     ░░   ░ ░      ░   
   ░          ░  ░ ░      ░  ░░ ░         ░   ░        ░  ░   ░            ░   
 ░                            ░ ░
</div></pre>                                                                           
                             
# FAQ

## What is this?
A repository with a daily updated list of JARM fingerprints from systems actively attempting to log in to other systems via ssh on port 22.

## Ok, what is JARM?
JARM TLS fingerprinting is a technique that can identify TLS servers based on their unique handshake characteristics. By sending different probes and analyzing the server responses, JARM can determine specific details about the server such as the SSL/TLS version, the cipher suites used, and the presence of specific extensions. 

More information @ [Salesforce page on JARM](https://github.com/salesforce/jarm)

## What files can I find here?
A csv and a json file for whichever fits your usecase.

## What do the files contain?
Both files contain the JARM fingerprint, the source IP, the source port (443, 444, 1443, 2443, 3443, 4443, 4444, 5443, 6443, 7443, 8443, and/or 9443), the country, the AS number, the known C2 platform matching the JARM fingerprint, and the timestamp of when the fingerprint was obtained. 

You think other ports should be added? Let me know. 

The csv file contains the following and is formatted as below:

<pre>
jarm,src_ip,src_port,country,asn,known_c2,timestamp
07d10d11d21d21d07c07d10d07d21d7f94927a800698f72ad8146900120abe,1.2.3.4,443,FR,12345,n/a,2022-09-26_19:24:57
2ad2ad16d00000022c2ad2ad2ad2adc048c697e0d6d0c91c6bf49b0695f45c,5.6.7.8,1443,HK,12345,n/a,2022-09-26_19:48:13
3fd3fd0003fd3fd21c42d42d000000307ee0eb468e9fdb5cfcd698a80a67ef,9.10.11.12,2443,CN,12345,n/a,2022-09-26_20:11:28
</pre>

The json file contains the following and is formatted as seen below:

<pre>
[
    {
        "jarm": "07d10d11d21d21d07c07d10d07d21d7f94927a800698f72ad8146900120abe",
        "src_ip": "1.2.3.4",
        "src_port": "443",
        "country": "FR",
        "asn": "12345",
        "known_c2": "n/a",
        "timestamp": "2022-09-26_19:24:57"
    },
    {
        "jarm": "2ad2ad16d00000022c2ad2ad2ad2adc048c697e0d6d0c91c6bf49b0695f45c",
        "src_ip": "5.6.7.8",
        "src_port": "1443",
        "country": "HK",
        "asn": "12345",
        "known_c2": "n/a",
        "timestamp": "2022-09-26_19:48:13"
    },
    {
        "jarm": "3fd3fd0003fd3fd21c42d42d000000307ee0eb468e9fdb5cfcd698a80a67ef",
        "src_ip": "9.10.11.12",
        "src_port": "2443",
        "country": "CN",
        "asn": "12345",
        "known_c2": "n/a",
        "timestamp": "2022-09-26_20:11:28"
    },
]
</pre>

## How often is this updated?

Daily. 

The list of matching C2 JARM fingerprints is updated slowly over time.

## Thanks

Thanks to [cedowens](https://github.com/cedowens) for his initial [list](https://github.com/cedowens/C2-JARM).
