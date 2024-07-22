# Crowdstrike-fix

![277316894-401f5135-cf60-4708-8372-48a082dc8003](https://github.com/user-attachments/assets/57214ebe-dde8-46e1-8acb-dbaea11ef0f2)

## Description

This repository provides step-by-step instructions to fix common errors encountered with CrowdStrike, a leading cybersecurity technology company. If you are experiencing issues or errors while using CrowdStrike, this guide will assist you in resolving them.

## Table of Contents

- [Error Fixes](#error-fixes)
  - [Error 1: 19.July 2024: PAGE_FAULT_IN_NONPAGED_AREA](#error-1-19july-2024-page_fault_in_nonpaged_area)
- [Contributing](#contributing)
- [License](#license)

## Error Fixes

Here are the steps to fix common CrowdStrike errors even when you dont have the bitlocker key:

### Error 1: 19.July 2024: PAGE_FAULT_IN_NONPAGED_AREA

Error details: What failed: csagent.sys

If you encounter the PAGE_FAULT_IN_NONPAGED_AREA error, follow these steps to resolve it:

1. Cycle through BSODs until you reach the recovery screen.
2. Navigate to Troubleshoot > Advanced Options > Startup Settings.
3. Press "Restart".
4. Skip the first Bitlocker recovery key prompt by pressing Esc.
5. Skip the second Bitlocker recovery key prompt by selecting "Skip This Drive" in the bottom right corner.
6. Navigate to Troubleshoot > Advanced Options > Command Prompt.
7. Type "bcdedit /set {default} safeboot minimal" and press Enter. Then, close the Command Prompt.
8. Go back to the WinRE main menu and select "Continue". It may cycle 2-3 times.
9. If you successfully boot into safe mode, log in as usual.
10. Open Windows Explorer and navigate to C:\Windows\System32\drivers\Crowdstrike.
11. Delete the offending file (the file name starts with C-00000291* and has a .sys file extension). This step fixes the BSOD from 19.July.2024.
12. Open the command prompt as an administrator.
13. Type "bcdedit /deletevalue {default} safeboot" and press Enter.
14. Restart your computer as normal and confirm if the behavior is back to normal.

Some Users reported that fix for Error 1:
1. Restarting the PC about 15 Times to auto rollback the version automaticly


Feel free to add more error fixes as needed.

## Contributing

Contributions are welcome! If you have additional error fixes or improvements to the existing ones, please open a pull request. Ensure that you follow the existing format and provide clear instructions for the error fix.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use and modify the code as per the license terms.

---

We hope this guide helps you resolve common errors encountered with CrowdStrike. If you have any questions or need further assistance, please don't hesitate to reach out.

Happy error fixing!
