# FakeGPT Web Extension Analysis

Executive Summary

This report analyzes the web extension FakeGPT in an isolated lab environment.

The extension is installed on a browser, capture keystrokes, stole data from the victim and send it to a remote infrastructure.

**Sample Information** 

| Field | Value |
|---|---|
| Sample Name | FakeGPT |
| File Type | Extension .CRX |
| Malware Type | Keylogger   |
| Malware Type | Infostealer |  
| File Size | 145 KB |

**Initial Behavior**

- Extension installer: loads mailicious browser extension.
- Target: capture specific websites and login forms
- Data: capture usernames, emails, passwords from submited forms
- Monitoring: record keystrokes
- Encrypting: encrypts stolen data using AES
- Exfiltration: send data to remote infrastructure
- Obfuscation: used for javascript code 

**Network Analysis**

- Send stolen data to remote domain `mo.elsaheedy.com`.
- Uses an exfiltration endpoint `/collect?data=`
- Exfiltrates data using HTTP GET requests via HTML Image objects.
- Transmition of data:
    - Encrypted credentials
    - Keystrokes
    - Victim hostname/site information

**Conclusion**

This laboratory analysis identified a malicious CRX extension designed to capture credentials, monitor keystrokes, and exfiltrate sensitive user information to a remote infrastructure.

The extension targeted login forms on specific websites and used AES encryption combined with HTTP GET requests for data exfiltration.
