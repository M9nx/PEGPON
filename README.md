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
- Screenshots with Gowitness

## 🚀 Usage

```bash
recon -d example.com -m all          # Run all modules
recon -d example.com -m passive      # Run only passive recon
recon -d example.com -m active       # Run only active fuzzing
recon -d example.com -m httpx        # Probe live subdomains
recon -i domains.txt -m passive      # Run passive recon on list
