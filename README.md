Kali Tools Collection 🔥🛠️

A curated collection of Kali / offensive security tools I've collected and developed over the years.
This repo is a personal toolbox — scripts, exploits, and automation I use for lab work, CTFs, and authorized penetration tests.

Owner: stux
Purpose: Portable collection of useful tools and scripts for reconnaissance, exploitation, post-exploitation, and automation.

Contents (what's in this repo)

Each folder contains the tool or script set — see each folder for usage and examples.

AutoRecon-main — automated reconnaissance pipeline (multi-tool scanning + enumeration).

MSSqlPwner-main — tools / scripts for attacking MS SQL instances.

PowerShell Scripts — assorted PowerShell scripts for Windows enumeration & automation.

Python Scripts — small Python utilities and helpers (scanners, parsers, helpers).

Sublist3r — subdomain enumeration tool (copy of Sublist3r).

cve-2022-23940 — exploit PoC / proof of concept for CVE-2022-23940 (for research/testing).

enum4linux — Linux SMB/NetBIOS enumeration utilities.

ligolo — reverse proxy / relay tools (for pivoting / lab tunneling).

mimikatz — credential extraction and Windows post-exploitation binary/scripts.

pspy-master — Linux process / cron/cronjob discovery tool (useful for privilege escalation).

secretfinder — passive secret/API-key finder from public sources.

PowerSploit.tar.gz — PowerShell post-exploitation toolkit archive.

linpeas.sh — Linux local privilege escalation enumeration script.

Quickstart — common commands

Clone the repo:

git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>


Run linPEAS (example):

# from your Kali machine (copy linpeas.sh to target or run in a lab environment)
chmod +x linpeas.sh
./linpeas.sh


Run AutoRecon (example):

# inside AutoRecon-main, read its README for flags; common usage:
python3 autorecon.py -t example.com


Run Sublist3r:

cd Sublist3r
python3 sublist3r.py -d example.com -o subdomains.txt


Serve a folder for quick download on a target:

# from Kali (use only in authorized labs)
cd <folder-with-binaries>
sudo python3 -m http.server 80
# then download from target with certutil / powershell


Tip: Always read the individual tool folder README or usage notes — many tools have specific dependencies and runtime flags.

Safety, Legal & Responsible Use ⚖️

These tools are dual-use and can cause harm if used against systems you do not own or are not explicitly authorized to test.

DO NOT use these tools on production systems or systems you don't have written permission to test.

Use these only in lab environments, CTFs, or under a signed Rules of Engagement (RoE) / authorization.

The author accepts no responsibility for misuse of these tools.

By using anything in this repo you confirm you have proper authorization to do so.

Dependencies & Notes

Many tools require Python 3.x, specific pip modules, or system packages (e.g., nmap, impacket, mono for some Windows binaries).

Windows utilities (e.g., mimikatz, PowerSploit) may be flagged by antivirus and are often blocked by EDR. Use in isolated lab environments.

Read each tool's individual folder for dependency installation and build steps.

Example install step for common deps:

sudo apt update && sudo apt install -y git python3 python3-pip nmap
pip3 install -r requirements.txt   # when present

Contributing

Want to add a tool or improvement?

Open a PR with a clear description and usage notes.

Add a short README in the tool folder describing usage, dependencies, and a responsible-use note.

Keep commits focused and include references for any third-party code.

Example folder README template

Use this for any new tool you add:

# ToolName

Short description.

## Usage
Example command(s).

## Dependencies
- python3
- pip packages: x,y,z

## Notes
Responsible use reminder; attribution; reference links.

License

I recommend MIT for personal tool collections. If you want, I can add a LICENSE file (MIT) to this repo.

Contact / Attribution

Owner: stux
If you spot an issue or have an update, open an issue or PR.
