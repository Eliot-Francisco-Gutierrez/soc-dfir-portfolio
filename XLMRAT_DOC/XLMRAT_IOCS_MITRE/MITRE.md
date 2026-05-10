# MITRE ATT\&CK Techniques

**List of techniques and description used in the attack**

**T1059.001** (Command and Scripting Interpreter: PowerShell).
Evidence:  `PowerShell.exe -NOP -WIND Hidden -Exec Bypass -NoNI`.

**T1053.005** (Scheduled Task/Job: Scheduled Task).
Evidence: `RegisterTaskDefinition("Update Edge", ...)`.

**T1027 and T1027.013** (Obfuscated Files or Information/Command Obfuscation and Encrypted/Encoded File).
Evidence: `$hexString_bbb = "4D_5A_90_00_03_00_00_00_04_00_00_00_FF_FF_00_00_B8_00_00` and `$Fu.GetType('N#ew#PE#2.P#E'-replace  '#', '')` or `$NA + 'osof#####t.NET\Fra###mework\v4.0.303###19\R##egSvc#####s.exe'-replace  '#', ''`

**T1204** (User Execution: Malicious File)
Evidence: The malware relied on the victim to execute  a disguised malicious file.

**T1105** (Ingress Tool Transfer).
Evidence: The malware retrieved additional payloads from the remote server using HTTP GET requests.
