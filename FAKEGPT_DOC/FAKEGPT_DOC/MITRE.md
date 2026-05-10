# MITRE ATT&CK Techniques

**List of techniques an description used in the attack**

**T1566** (Pishing).
Evidence: The extension impersonates a legitimate ChatGPT-related browser extension in order to trick users into installing malicious code.

**T1056** (Input Capture).
Evidence: The malware captures user input from login forms and browser activity.

**T1056.001** (Keylogging).
Evidence: The extension monitors keyboard events using the `keydown` event listener to capture keystrokes. (`document.AddEventListener('keydown'),...`).

**T1027** (Obfuscated Files or Information).
Evidence: The malware uses obfuscated JavaScript code and Base64-encoded strings to hide malicious functionality.

**1041** (Exfiltration Over C2 Channel).
Evidence: The extension exfiltrates encrypted data to a remote domain using HTTP GET requests.