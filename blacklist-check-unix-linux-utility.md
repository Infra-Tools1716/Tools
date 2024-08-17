# blacklist-check-unix-linux-utility
Blacklist check UNIX/Linux utility. I was just a bit tired of web interfaces.

### Installation

    git clone https://github.com/adionditsak/blacklist-check-unix-linux-utility.git
    cd blacklist-check-unix-linux-utility
    chmod +x ./bl
    mv ./bl /usr/local/bin

### Usage

    # Use with domains or IP addresses
    $ ./bl domain.tld
    $ ./bl 8.8.8.8 # IP
    
    # Pipe with other UNIX utils, eg. grep. Only blacklisted:
    $ ./bl domain.tld | grep "blacklisted"

### Sample output

    $ ./bl 8.8.8.8
    You entered an IP: 8.8.8.8
    8.8.8.8 name google-public-dns-a.google.com.
    15-02-17_Feb:02:1424185674_+0000 8.8.8.8.0spam.fusionzero.com.          [not listed]
    15-02-17_Feb:02:1424185674_+0000 8.8.8.8.0spam-killlist.fusionzero.com. [not listed]
    15-02-17_Feb:02:1424185674_+0000 8.8.8.8.rbl.abuse.ro.                  [not listed]
    15-02-17_Feb:02:1424185674_+0000 8.8.8.8.spam.dnsbl.anonmails.de.       [not listed]
    15-02-17_Feb:02:1424185674_+0000 8.8.8.8.dnsbl.anticaptcha.net.         [not listed]
    ...
