# Instructions for building a demo in MacOS

## Prerequisites
- **Install Visual Studio Code**: [VSCode](https://code.visualstudio.com/download)
- **Download the FreeRTOS** and copy in a folder you prefer: [FreeRTOS](https://www.freertos.org/a00104.html)
- **Install brew** 

          /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
          
 - **Install [arm-none-eabi-gcc]** 
    - ```brew install --cask gcc-arm-embedded```
- **Install QEMU**
    * ```brew install qemu```
- **Install GNU make utility**
    * ```brew install cmake```
- **Ensure the required binaries are in PATH with** 
  - ```arm-none-eabi-gcc --version```, ```arm-none-eabi-gdb --version```, and ```make --version```


## Building and Running
1. Clone this repository ```git clone https://github.com/luigicappello/CA-OS-Exam-FreeRTOS.git```
2. Copy this repository in the FReeRTOS folder you downloaded prevoiusly, under the path  ```FreeRTOS/Demo/CORTEX_MPS2_QEMU_IAR_GCC``` copy and replace the folder ```CORTEX_MPS2_QEMU_IAR_GCC```
3. Open VSCode under the folder ```FreeRTOS/Demo/CORTEX_MPS2_QEMU_IAR_GCC```.
4. Open ```.vscode/launch.json```, and ensure the ```miDebuggerPath``` variable is set to the path where arm-none-eabi-gdb is on your machine. You can check typing on your terminal ```which arm-none-eabi-gdb```
5. Browse into /build/gcc and right click on Makefile, and open in a terminal. After that launch ```make clean```
6. On the VSCode left side panel, select the “Run and Debug” button. Then select “Launch QEMU RTOSDemo” from the dropdown on the top right and press the play button. This will build, run, and attach a debugger to the demo program.
