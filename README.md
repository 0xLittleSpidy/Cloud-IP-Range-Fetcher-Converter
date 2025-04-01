# Cloud IP Range Fetcher & Converter

This tool fetches public IPv4 ranges from major cloud providers (AWS, Azure, Google Cloud, DigitalOcean), converts CIDR ranges into individual IP addresses using `mapcidr`, and outputs the results to a file or console.

---

## Features
- **Multi-provider Support**: Fetches IP ranges from:
  - Amazon Web Services (AWS)
  - Microsoft Azure
  - Google Cloud Platform (GCP)
  - DigitalOcean
- **CIDR Conversion**: Uses `mapcidr` to expand CIDR blocks into individual IPs.
- **Flexible Output**: Save results to a file or print to console.

---

## Requirements
1. **Python 3.6+**
2. **Dependencies**:
   ```bash
   pip install requests
   ```
3. **mapcidr**: Install the CLI tool from [mapcidr GitHub](https://github.com/projectdiscovery/mapcidr).

---

## Usage
```bash
python cloud_ip_fetcher.py <provider> [--output OUTPUT_FILE]
```

### Arguments
| Argument       | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `provider`     | Cloud provider: `aws`, `azure`, `google`, or `digitalocean` (case-insensitive). |
| `--output`     | Optional output file to save IP addresses (one per line).                   |

---

## Examples
1. Fetch AWS IPs and save to `aws_ips.txt`:
   ```bash
   python cloud_ip_fetcher.py aws --output aws_ips.txt
   ```
2. Print Google Cloud IPs to console:
   ```bash
   python cloud_ip_fetcher.py google
   ```

---

## Notes
- **Azure URL**: The Azure IP range URL is hardcoded and may need updates if Microsoft changes their file naming convention.
- **IPv6 Exclusion**: Only IPv4 addresses are processed; IPv6 ranges are skipped.
- **Error Handling**: Debug logs are generated to troubleshoot issues (e.g., invalid CIDR blocks).

---

## Contributing
Contributions are welcome! If you'd like to contribute to this project, please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes.
4. Submit a pull request.

---

# **Ethical Use Only**  

This tool is intended for **legal and authorized security assessments only**. By using this software, you agree to comply with all applicable laws and regulations.  

## **Legal Disclaimer**  
The developers of this tool are **not responsible** for any misuse or illegal activities conducted with it.

**Use responsibly and ethically.** Always obtain **written permission** before scanning third-party systems.  

---  
*By using this tool, you acknowledge that you understand and agree to these terms.*
