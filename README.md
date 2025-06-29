
```
██████╗ ███████╗ ██████╗ ██████╗  ██████╗ ███╗   ██╗
██╔══██╗██╔════╝██╔════╝ ██╔══██╗██╔═══██╗████╗  ██║
██████╔╝█████╗  ██║  ███╗██████╔╝██║   ██║██╔██╗ ██║
██╔═══╝ ██╔══╝  ██║   ██║██╔═══╝ ██║   ██║██║╚██╗██║
██║     ███████╗╚██████╔╝██║     ╚██████╔╝██║ ╚████║
╚═╝     ╚══════╝ ╚═════╝ ╚═╝      ╚═════╝ ╚═╝  ╚═══╝

        [ PEGPON - v1.2   @M9nx ]
```


# PEGPON - Subdomain & Web Recon Automation

PEGPON is an advanced Bash-based automation tool for subdomain enumeration, fuzzing, and web reconnaissance.  
It leverages top-tier tools like `subfinder`, `assetfinder`, `ffuf`, `httpx`, `gau`, `waybackurls`, `dirsearch`, `katana`, and more.

>  Created by @[M9nx](https://x.com/__M9nx) for bug bounty 

---

##  Features

-  Passive & Active Subdomain Enumeration
-  Multi-level subdomain fuzzing (3 levels deep)
-  IP Resolution from all known sources
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
go install -v github.com/Findomain/Findomain

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

* Chaos [https://chaos.projectdiscovery.io/]
* GitHub [https://github.com/settings/tokens]
* SecurityTrails [https://securitytrails.com/]
* Netlas [https://docs.netlas.io/automation/how_to_get_api_key/]
* Zoomeye [https://www.zoomeye.ai/]
* ShrewdEye [https://shrewdeye.app/search]

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
├── passive_subdomains.txt       # From passive recon tools
├── active_subdomains.txt        # From ffuf brute-force
├── final_live_subdomains.txt    # Filtered live subdomains (httpx/ping)
├── resolved_ips.txt             # Mapping: subdomain => IP
├── unique_ips.txt               # All deduplicated IPs
├── dirsearch_results/           # Directory bruteforce output
│   ├── dirsearch_domains.txt
│   ├── dirsearch_http_1.2.3.4.txt
│   └── ...
├── urls/                        # Categorized URLs from all_urls.txt
│   ├── js_urls.txt              # .js URLs
│   ├── php_urls.txt             # .php URLs
│   ├── aspx_urls.txt            # .aspx URLs
│   ├── jsp_urls.txt             # .jsp URLs
│   ├── json_urls.txt            # .json URLs
│   ├── txt_urls.txt             # .txt URLs
│   ├── html_urls.txt            # .html URLs
│   ├── css_urls.txt             # .css URLs
├── all_urls.txt                 # Aggregated URLs from gau/wayback/etc.

         
```

---

##  Disclaimer

This tool is for **educational and authorized testing** only.
Do not use against targets without permission.

---





