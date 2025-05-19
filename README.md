

# FTP Buffer Overflow Exploit Script

## Overview

This Python script demonstrates how to exploit a buffer overflow vulnerability in an FTP server by sending a specially crafted payload containing reverse shellcode. The payload is delivered in fragments to evade detection, and the script tests multiple payload sizes to identify the correct buffer length for successful exploitation.

> **Disclaimer:**  
> This script is intended **strictly for educational purposes and authorized penetration testing** in controlled environments. Unauthorized use against systems you do not own or have explicit permission to test is illegal and unethical.



## Features

- Connects to a target FTP server and port.
- Crafts and sends a buffer overflow payload with embedded reverse shellcode.
- Delivers the payload in fragments with time delays to avoid detection.
- Iterates over multiple payload sizes for effective exploitation.
- Prints server responses for monitoring exploit progress.

## Prerequisites

- Python 3.x
- Basic knowledge of networking and buffer overflow exploits
- A vulnerable FTP server (e.g., Metasploitable, lab environment)
- Reverse shellcode generated with tools like `msfvenom` (replace the sample shellcode in the script)



## Usage

1. **Edit the Script:**
   - Replace `YOUR-T4RG3T-IP` with the IP address of your target FTP server.
   - Replace the sample shellcode with your own (generated via `msfvenom` or similar tools).

2. **Run the Script:**
   ```bash
   python3 ftp_exploit.py
   ```

3. **Monitor Output:**
   - The script will attempt to exploit the FTP server using different payload sizes.
   - Server responses and exploit status will be printed to the console.



 Example

```python
target_ip = "192.168.1.100"
target_port = 21
shellcode =  b"\xdb\xc4\xd9\x74\x24..."  # Replace with your shellcode
```

---

## Legal Notice

- **This script is for authorized testing and educational research only.**
- Do **not** use this tool against any system without explicit, written permission.
- The author is not responsible for any misuse or damage caused by this script.



## References

- [OWASP: Buffer Overflow](https://owasp.org/www-community/vulnerabilities/Buffer_overflow)
- [Metasploit Unleashed: msfvenom](https://www.offensive-security.com/metasploit-unleashed/msfvenom/)
- [Python socket documentation](https://docs.python.org/3/library/socket.html)



**Stay ethical. Hack responsibly.**
