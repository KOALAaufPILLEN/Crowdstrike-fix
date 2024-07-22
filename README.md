# Crowdstrike-fix
Crowdstrike faulty Update fix


![277316894-401f5135-cf60-4708-8372-48a082dc8003](https://github.com/user-attachments/assets/15d27fff-c473-4110-9425-1f6977908f87)

## Description

This repository contains the necessary steps to fix common errors encountered with CrowdStrike, a leading cybersecurity technology company. If you are experiencing issues or errors while using CrowdStrike, this guide will provide you with a step-by-step solution to resolve them.

## Table of Contents

- [Error Fixes](#error-fixes)
    - [Error 1 : 19.July 2024: PAGE_FAULT_IN_NONPAGED_AREA](#Error-1-:-19.July-2024:-PAGE_FAULT_IN_NONPAGED_AREA)
- [Contributing](#contributing)
- [License](#license)

## Error Fixes

Here are the step-by-step instructions to fix common CrowdStrike errors:

### Error 1 : 19.July 2024: PAGE_FAULT_IN_NONPAGED_AREA
What failed csagent.sys

If you encounter the PAGE_FAULT_IN_NONPAGED_AREA Error, follow these steps to resolve it:

1. Cycle through BSODs until you get the recovery screen.
2. Navigate to Troubleshoot>Advanced Options>Startup Settings
3. Press "Restart"
4. Skip the first Bitlocker recovery key prompt by pressing Esc
5. Skip the second Bitlocker recovery key prompt by selecting Skip This Drive in the bottom right
6. Navigate to Troubleshoot>Advanced Options> Command Prompt
7. Type "bcdedit /set {default} safeboot minimal". then press enter and close the Command Prompt
8. Go back to the WinRE main menu and select Continue.
9. "It may cycle 2-3 times."
11. If you booted into safe mode, log in per normal.
12. Open Windows Explorer, navigate to C:\Windows\System32\drivers\Crowdstrike
13. Delete the offending file (STARTS with C-00000291*. sys file extension) (This error fixes the BSOD from 19.July.2024)
14. Open command prompt (as administrator)
15. Type "bcdedit /deletevalue {default} safeboot"., then press enter. 5. Restart as normal, confirm normal behavior.


Feel free to add more error fixes as needed.

## Contributing

Contributions are welcome! If you have any additional error fixes or improvements to the existing ones, please feel free to open a pull request. Ensure that you follow the existing format and provide clear instructions for the error fix.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use and modify the code as per the license terms.

---

We hope this guide helps you resolve common errors encountered with CrowdStrike. If you have any questions or need further assistance, please don't hesitate to reach out.

Happy error fixing!


here are the steps to fix the Crowdstrike faulty Update even when you have a Bitlocker set, without knowing the Bitlocker code
