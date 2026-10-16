# Installation walkthrough

Download the prepared [v0.7 ZIP or ISO](DOWNLOADS.md), then follow the workflow below. See [tested results](TESTING.md) for validation and limitations.

The **v0.8 preview** follows the same intended workflow and adds optional Publisher and Access choices, unchecked by default. Its full installation and rollback have not yet been validated from a clean baseline. Evaluate it on a backed-up test machine or a separate VM; it is not an in-place upgrade for an existing Office installation. Keep the extracted folder for that version separate from older kits.

1. Start with Windows 7 SP1, administrator access, no existing Office installation and at least 8 GB free on the Windows drive. Back up the machine. For a VM, leave room on the host drive for disk growth.
2. Extract the complete kit ZIP to a permanent local folder, or mount its ISO as a virtual DVD. Do not run the program inside the ZIP preview.
3. Open **7Revamped.exe**, choose **Open installer**, and allow administrator permission.
4. Mount your matching English ProPlus2021Retail Office image, build **16.0.16327.20264**, so Windows can access it through a drive letter. In a VM, attach it through the virtual optical drive. Windows 7 has no built-in ISO mounting; a physical PC needs a suitable mounting utility or accessible installation media. Close the native Office AutoPlay setup if it appears.
5. Select **Detect Office drive**, choose your applications, read and accept the Office license agreement, and allow the licensing service to start when needed.
6. Select **Install Office** and follow the restart prompts. Keep the extracted kit folder and Office media available throughout setup. **Start-Installer.cmd** remains a direct entry point if you need to resume manually.
7. After completion, test each selected application: create a file, edit it, save, close and reopen. Leave Word and Excel open for several minutes, then edit or calculate again. Complete normal Office activation separately.

If a stage fails, open **Installation details** and record the error before retrying. Do not run two installation attempts at once. A window opening or an exit code of zero alone does not establish that every feature works.
