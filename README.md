
```
██████╗ ███████╗ ██████╗ ██████╗  ██████╗ ███╗   ██╗
██╔══██╗██╔════╝██╔════╝ ██╔══██╗██╔═══██╗████╗  ██║
██████╔╝█████╗  ██║  ███╗██████╔╝██║   ██║██╔██╗ ██║
██╔═══╝ ██╔══╝  ██║   ██║██╔═══╝ ██║   ██║██║╚██╗██║
██║     ███████╗╚██████╔╝██║     ╚██████╔╝██║ ╚████║
╚═╝     ╚══════╝ ╚═════╝ ╚═╝      ╚═════╝ ╚═╝  ╚═══╝

        [ PEGPON - v1.1   @M9nx ]
```


# PEGPON - Subdomain & Web Recon Automation

PEGPON is an advanced Bash-based automation tool for subdomain enumeration, fuzzing, and web reconnaissance.  
It leverages top-tier tools like `subfinder`, `assetfinder`, `ffuf`, `httpx`, `gau`, `waybackurls`, `dirsearch`, `katana`, and more.

>  Created by @M9nx for bug bounty & red teamers.

---

##  Features

-  Passive & Active Subdomain Enumeration
-  Multi-level subdomain fuzzing (3 levels deep)
-  HTTP probing & filtering
-  Directory brute-force with extensions
-  URL collection (Wayback, GAU, Katana)
-  URL filtering by file type (JS, PHP, JSON, etc.)
-  Fully automated per domain

---

##  Requirements

Install the following tools before using PEGPON:

```bash
sudo apt install jq curl git python3
go install -v github.com/projectdiscovery/subfinder/v2@latest
go install -v github.com/tomnomnom/assetfinder@latest
go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest
go install github.com/tomnomnom/waybackurls@latest
go install -v github.com/lc/gau@latest
go install -v github.com/projectdiscovery/katana/cmd/katana@latest
````
```bash
cd 
```
Also clone:

* [`dirsearch`](https://github.com/maurosoria/dirsearch)

Make sure all tools are in your `$PATH`.

---

##  API Keys

Set your API keys inside the script:

* Chaos
* GitHub
* SecurityTrails
* Netlas
* Zoomeye

---

## ⚙ Installation

```bash
git clone https://github.com/M9nx/pegpon
cd pegpon
chmod +x pegpon
sudo mv pegpon /usr/local/bin/
```

---

##  Usage

### Single Domain

```bash
pegpon -d example.com
```

### List of Domains

```bash
pegpon -l domains.txt
```

---

##  Output Structure

```
recon/
  └── example.com/
      ├── recon.log
      ├── passive_subdomains.txt
      ├── active_subdomains.txt
      ├── final_live_subdomains.txt
      ├── all_urls.txt
      └── urls/
          ├── js_urls.txt
          ├── auth_urls.txt
          └── ...
```

---

##  Disclaimer

This tool is for **educational and authorized testing** only.
Do not use against targets without permission.

---





