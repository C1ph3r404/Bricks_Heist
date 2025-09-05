# 📝 Bricks Heist – TryHackMe Writeup

---

## 🔍 Enumeration

### Nmap Scan
Pro tip: scan for all open port then to a detailed scan on open ones  
```bash
nmap -p- --min-rate=2000 -oN allport.nmap $IP
```
```bash
nmap -sC -sV -vv -p$1, $2, $3 -oN detaile.nmap $IP
```
![nmap](screenshots/nmap1.png)  
![nmap](screenshots/nmap2.png)   
Open PORTS: 22, 80, 443  

### PORT 443
![web](screenshots/web1.png)  
![web](screenshots/web2.png) 
checked a few directories/files like `/robot.txt` `wp-admin` but nothing useful

### WPSCAN
```bash
wpscan --url https://brick.thm --disable-tls-checks
```



