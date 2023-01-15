<pre>                            
██████   █████  ██ ██      ██    ██          ██  █████  ██████  ███    ███ 
██   ██ ██   ██ ██ ██       ██  ██           ██ ██   ██ ██   ██ ████  ████ 
██   ██ ███████ ██ ██        ████            ██ ███████ ██████  ██ ████ ██ 
██   ██ ██   ██ ██ ██         ██        ██   ██ ██   ██ ██   ██ ██  ██  ██ 
██████  ██   ██ ██ ███████    ██         █████  ██   ██ ██   ██ ██      ██ 
                                                                           
</pre>                                                                           
                             
# FAQ

## What is this?
A repository with a daily updated list of JARM fingerprints from systems actively attempting to log in to other systems via ssh on port 22.

## Ok, what is JARM?
[Salesforce page on JARM](https://github.com/salesforce/jarm)

## What files can I find here?
A csv and a json file for whichever fits your usecase.

## What do the files contain?
Both files contain the JARM fingerprint, the source IP, the source port (only 443 and 8443 are covered currently), and the timestamp of when the fingerprint was obtained.

The csv file contains the following and is formatted as below:

<pre>
jarm,src_ip,src_port,timestamp
jarmfingerprintvalue,1.2.3.4,443,2022-09-26_19:24:57
jarmfingerprintvalue,5.6.7.8,8443,2022-11-05_09:22:53
</pre>

The json file contains the following and is formatted as seen below:

<pre>
[
    {
        "jarm": "07d10d11d21d21d07c07d10d07d21d7f94927a800698f72ad8146900120abe",
        "src_ip": "1.2.3.4",
        "src_port": "443",
        "timestamp": "2022-09-26_19:24:57"
    },
    {
        "jarm": "2ad2ad16d00000022c2ad2ad2ad2adc048c697e0d6d0c91c6bf49b0695f45c",
        "src_ip": "5.6.7.8",
        "src_port": "443",
        "timestamp": "2022-09-26_19:48:13"
    }
]
</pre>
