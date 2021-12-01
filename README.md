# dostackbufferoverflowgood-POC
POC exploit reverse shell code written in PowerShell targeting the dostackbufferoverflowgood.exe service

## Getting the vulnerable binary
https://github.com/justinsteven/dostackbufferoverflowgood

## Setting Up the Environment
I wrote a guide on setting up a security lab in two hypervisors
- [Proxmox](https://docs.google.com/document/d/1X7vj1WOXXssWHVfvdgrPmuJ9AgVAN8-mqGZ0eQbIevk/edit)
- [VirtualBox](https://docs.google.com/document/d/1DH-epmXJMvQtOnDQYa3zUXvq9497Mm3276K8frNz2UM/edit)

They both contain sections on creating a vulnerable Windows 7 VM on which to practice buffer overflows

## Building the POC
1. Run as administrator `dostackbufferoverflowgood.exe` on the Windows 7 VM
2. Run as administrator Immunity Debugger (make sure `mona.py` installed)
3. Attach `dostackbufferoverflowgood.exe` to the debugger
4. Run your tests
5. Every time the application crashes, restart `dostackbufferoverflowgood.exe` and reattach it to the debugger
