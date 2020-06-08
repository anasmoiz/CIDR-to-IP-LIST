# CIDR-to-IP-LIST

THIS SCRIPT WILL EXPAND A CIDR ADDRESS.

##### SYNOPSIS

```
./cidr-to-ip.sh [OPTION(only one)] [STRING/FILENAME]
```

##### DESCRIPTION

- -h Displays this help screen
- -f Forces a check for network boundary when given a STRING(s)
- -i Will read from an Input file (file should contain one CIDR per line) (no network boundary check)
- -b Will do the same as –i but with network boundary check

##### EXAMPLES

```
./cidr-to-ip.sh 192.168.0.1/24

./cidr-to-ip.sh 192.168.0.1/24 10.10.0.0/28

./cidr-to-ip.sh -f 192.168.0.0/16

./cidr-to-ip.sh -i inputfile.txt
```


### CIDR-to-IP-LIST Alternatives

##### USING NMAP

```
nmap -sL 10.10.64.0/27 | awk '/Nmap scan report/{print $NF}'
```

##### USING PRIPS

```
prips  10.10.64.0/27
```







