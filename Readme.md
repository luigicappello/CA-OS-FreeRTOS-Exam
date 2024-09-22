# Instructions for building a demo in MacOS

## Prerequisites
- **Install Visual Studio Code**: [VSCode](https://code.visualstudio.com/download)
- **Install brew** 

          /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
          
 - **Install [arm-none-eabi-gcc]** 
    - ```brew tap ArmMbed/homebrew-formulae``` 
    - ```brew install arm-none-eabi-gcc```
- **Install QEMU**
    * ```brew install qemu```
- **Install GNU make utility**
    * ```brew install cmake```
- **Ensure the required binaries are in PATH with** 
  - ```arm-none-eabi-gcc --version```, ```arm-none-eabi-gdb --version```, and ```make --version```

## Building and Running
1. Clone this repository ```https://github.com/luigicappello/CA-OS-Exam-FreeRTOS.git```
1. Open VSCode to the folder ```FreeRTOS/Demo/CORTEX_MPS2_QEMU_IAR_GCC```.
2. Open ```.vscode/launch.json```, and ensure the ```miDebuggerPath``` variable is set to the path where arm-none-eabi-gdb is on your machine. You can check writing on your terminal ```which arm-none-eabi-gdb```
3. On the VSCode left side panel, select the “Run and Debug” button. Then select “Launch QEMU RTOSDemo” from the dropdown on the top right and press the play button. This will build, run, and attach a debugger to the demo program.
