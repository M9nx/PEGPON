# Recon Script

 **Automated Reconnaissance Tool for Bug Bounty Hunting**  
Author: [M9nx](https://github.com/M9nx)

##  Features
- Passive subdomain enumeration (Subfinder, Assetfinder, Sublist3r, crt.sh, Findomain, Chaos, GitHub)
- Active subdomain fuzzing with FFUF
- Live host probing with Httpx
- Directory brute-forcing with Gobuster
- Crawling with Katana
- Historical URL fetching (Waybackurls, GAU)
- URL filtering by extension


## 🚀 Usage

```bash
recon -d example.com       
recon -l list.txt    
```
## Requirements:

bash, jq, curl

Tools installed:

subfinder, assetfinder, sublist3r, findomain, chaos, github-subdomains

ffuf, httpx, gobuster, katana, waybackurls, gau, gowitness

## Installation

```bash
git clone https://github.com/M9nx/recon-tool.git
cd recon-tool
```
and 

```bash
nano recon
```
Then set your github Token and Chaoos Token (line 58,81)

```bash
chmod +x recon
sudo mv recon /usr/local/bin/
```
