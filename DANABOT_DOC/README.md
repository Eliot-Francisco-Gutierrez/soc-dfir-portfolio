# DANABOT Malware Analysis

Executive Summary

This report analyzes the DANABOT malware sample in an isolated lab environment.

The malware establishes a connection, download two files and execute a payload.

**Sample Information**

| Field | Value |
|---|---|
| Sample Name | DANABOT |
| File Type | JavaScript|
| Malware Family | Troja.Downloader.Script.gen |
| Hashes | SHA256 / MD5 |
| File Size | 5.43 KB |

**Initial Behavior**

- Source IP: 10.2.14.101
- Destination IP: 62.173.142.148
- Protocol: TCP
- HTTP requests: GET /login.php
- Download Payloads: login.php
- File detected as `malicious/downloader, JavaScript obfuscated, download via HTTP (GET/login.php), WndResizerApp.dll, suspicious with posterior activity, probably secondary payload or aditional component`.


**Network Analysis**
- IP: `62.173.142.148` / The IP host is related with the Domain name `spacenet.ru`.
- Port: TCP/80
- Protocol: transfer protocol TCP to confirm the availability of the port.

**Payload Analysis**

- Extracted file: `login.php`
- File Type: Obfuscated Javascript
- Behavior: 
    - Downloads additional payloads.
    - Uses obfuscation techniques.
    - Acts as downloader/dropper.

- Additional payload detected:
    - `WndResizerApp.dll`
    - MD5: `e758e07113016aca55d9eda2b0ffeebe`

- Hashes generated for IOC tracking:
  - SHA256
  - MD5

**Conclusion**

This laboratory analysis identified malicious HTTP traffic, payload delivery activity, and suspicious infrastructure associated with DanaBot-related malware behavior.

The analysis also demonstrated the use of Wireshark, VirusTotal, IOC Extraction, and basic defensive controls for malware investigation.
