# XLMRAT Malware Analysis

Executive Summary

This report analyzes an XLMRAT malware sample in an isolated lab environment.

The malware uses obfuscated PowerShell commands, downloads secondary payloads, and establishes persistence through Scheduled Tasks.

**Sample Information**

| Field | Value |
|---|---|
| Sample Name | XLMRAT |
| File Type | PE32 Executable|
| Malware Family | AsyncRAT |
| Hashes | SHA256 / MD5 |
| File Size | 65 KB |

**Initial Behavior**

- Source IP: 10.1.9.101
- Destination IP: 45.126.209.4
- Protocol: TCP
- HTTP requests: GET xlm.txt
- Download Payloads: the malware issued an HTTP GET request to retrieve the file `mdm.jpg`
- Suspicious PowerShell activity: ```Powershell.exe -NOP -WIND Hidden -Exec Bypass -NoNI```. The malware executes PowerShell in a hidden mode while bypassing execution policies and disabling interactive prompts.

**Network Analysis**

- IP: `45.126.209.4` / The IP host is related with the Domain name `reliablesite.net` based on EE.UU
- Port: TCP/222 was used for outbound comunnication.
- Protocol: transfer protocol TCP to confirm the availability of the port.

**Payload Analysis**

- Obfuscation: The Malware used obfuscation techniques to bypass the policies and evade detection `Fragmented strings, concatenation, hex blobs, hidden executions`.
- PowerShell Execution: `bypass execution policy, hidden windows, non-interactive-execution`.
- Persistence mechanisms: `scheduled task, bat launcher, vbs launcher`.



