# How to Run a Filesystem Check on Windows and Repair System Files

If Windows is freezing or behaving erratically, there might be a problem with
the filesystem or system files. You can use the built-in
[Deployment Image Servicing and Management (DISM)](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/what-is-dism?view=windows-10)
and System File Checker (SFC) tools to try to fix the problem.

To use the DISM tool to fix problems with the filesystem or system files:

1. Click the Windows start button.
1. Type `cmd` and open the Command Prompt application.
1. In the Command Prompt window, run the command:
   `DISM.exe /Online /Cleanup-Image /RestoreHealth`. This command performs
   cleanup and recovery operations on the system files. For more information,
   see Microsoft's documentation on [repairing a Windows image](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/repair-a-windows-image?view=windows-10).
1. After `DISM.exe` finishes, run the following command in the Command Prompt
   window: `sfc /scannow`. This command scans all protected system files and
   replaces corrupted files. For more information, see Microsoft's documentation
   on
   [using SFC to repair missing or corrupted system files](https://support.microsoft.com/en-us/topic/use-the-system-file-checker-tool-to-repair-missing-or-corrupted-system-files-79aa86cb-ca52-166a-92a3-966e85d4094e).
1. Reboot the machine and test to see if Windows continues to freeze or behave
   erratically.
