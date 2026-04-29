## VirtualInput

A HID driver that includes a virtual mouse, keyboard, and an additional mouse with absolute coordinates, for Windows 10/11. Compiled source code from [koharubiyori-VirtualInput](https://github.com/koharubiyori/VirtualInput).

## Installation 

1. Run `bcdedit /set testsigning on` (with cmd as admin) to enable test mode, then reboot your system.
2. Download and extract the `VirtualInput-Driver_Installer.zip` file.
3. Follow the simple instructions in the `Install_Uninstall_Instructions.txt` file, in the extracted folder, to install/uninstall the driver.

## Manual Building instructions (if above fails) 

1. Open `VirtualInput.sln` in Visual Studio.
2. Create a test certificate: `Project -> Properties -> Configuration Properties (Driver Signing) -> Set: "Sign Mode = Test Sign" and "Test Certificate = <Create Test Certificate>"` (Then press Apply & Ok)
3. Build the project in Debug mode (Debug -> Rebuild Solution).
4. Copy the certificate file from `x64\Debug\VirtualInput.cer` to `x64\Debug\VirtualInput\`.
5. Copy the `VirtualInput` folder from ``x64\Debug\` into the target Windows 10/11 machine, and follow the simple instructions in the `Install_Uninstall_Instructions.txt` file, inside the `VirtualInput-Driver_Installer.zip` file, to install/uninstall the driver.

## Credits

The code is taken from [koharubiyori-VirtualInput](https://github.com/koharubiyori/VirtualInput), and I compiled the code & updated it to be compatible with the latest Windows 11 builds. Note that the Driver is not signed, and Windows might sometimes throw a warning message while installing. You can ignore it and proceed to install, using instructions provided (which is easier); or you can compile the source code yourself and sign it for your system.
