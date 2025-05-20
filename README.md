
# VirusTotal-IOC-Analyzer


This Python script analyzes IOCs (Indicators of Compromise) such as **IP addresses**, **domains**, and **file hashes** by querying the [VirusTotal](https://www.virustotal.com/) API. It classifies each IOC based on the community’s vote and exports the results to a structured CSV. This project uses libraries such as re, requests, json, pandas, dotenv, and os.
## 📌 Featuresre, 
 ✅ Automatically detects IOC type (IP, domain, or hash)
- ✅ Queries the VirusTotal API for threat intelligence
- ✅ Calculates malicious vote percentage
- ✅ Classifies IOCs as:
  - `malicious` (if >30% votes are malicious),
  - `non-malicious`, or
  - `unknown` (0 votes)
- ✅ Outputs results to `CSV` for reporting or further analysis

1. ## ⚙️ Setup

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/vt-ioc-analyzer.git
cd vt-ioc-analyzer
```
### 2. Install Requirements
```bash
pip install -r requirements.txt
```
### 3. Create a .env File
In the root directory, create a .env file with your VirusTotal API key:
```bash
API_KEY=your_virustotal_api_key_here
```
### 4. 📝 Add IOCs
Edit the inputs/iocs.txt file and add your IOCs (one per line). Examples:
```bash
8.8.8.8
example.com
275a021bbfb6489e54d471899f7db9d1663fc695ec2fe2a2c4538aabf651fd0f
```
###5. 🚀 Run the Script
```
python main.py
```
The results will be saved to:
```
outputs/output.csv
```
##6. 🛡️ Disclaimer
This project is for educational and research purposes only. VirusTotal data is community-contributed and should not be the sole source of truth. Always verify IOCs using professional threat intelligence sources.

---------------Made with ❤️ by a Security Engineer --------------------
