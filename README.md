# `opkg` binary for Philips Hue Bridge 2.x

If you have a rooted Philips Hue Bridge Bridge 2.x you can, probably, run the package manager `opkg`


## Prerequisites
* A rooted Philips Hue Bridge 2.x For more info about to to root a Philips Hue, check out [this page](http://colinoflynn.com/2016/07/getting-root-on-philips-hue-bridge-2-0/)
* `ssh` and `scp` access to your Philips Hue Bridge

## Installation
From this Git repository, transfer (e.g. using `scp`) the contents of the `bin` and `etc` directories to the similarly named `/bin` and `/etc` folder.

`ssh` to your Philips Hue Bridge and run the following commands to properly set the permissions for the files:  
```
chmod 755 /bin/opkg /bin/wget /etc/opkg
chmod -R 644 /etc/opkg/distfeeds.conf /etc/opkg/keys
```

If everything went correctly, you can now run `opkg update` to update the list of available packages and install any package that is on the list.  
As example, to install `htop` you run `opkg instlal htop`. When finished, `htop` is installed and can be run.
  
## Binary information
### opkg
`opkg version c5dccea956b8be14eabf6ff69b331a3e9ac36749 (2021-01-31)`

### wget
For the full `wget --version` output, please check out `wget.version`.
``` 
GNU Wget 1.20.3 built on linux-gnu.

-cares +digest -gpgme +https +ipv6 -iri +large-file -metalink -nls 
+ntlm +opie -psl +ssl/openssl 
```