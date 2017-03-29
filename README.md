## Eclipse Template for STM32L053R8 + GCC + OpenOCD + FreeRTOS
---
### Working Environment
 - UBUNTU 16.04
 - Eclipse NEON 3 (64 bits)
 - GNU ARM Embedded Toolchain 6-2017-q1-update
 - GNU ARM Eclipse Plug-in
 - OpenOCD V0.10.0
 
### Download Links
 - [GNU ARM Binary](https://developer.arm.com/open-source/gnu-toolchain/gnu-rm/downloads)   
 - [GNU ARM Eclipse plug-in](https://marketplace.eclipse.org/content/gnu-arm-eclipse) (Or from source [here](https://github.com/gnuarmeclipse/plug-ins))   
 - [OpenOCD Binary](https://github.com/gnuarmeclipse/openocd/releases)   
 ---
### Setup
#### 1. Install ARM-Toolchain and OpenOCD
Download binary from links above, extract and put them at.
```sh
$/home/opt/
```
Note: 
 - It is not necessary to put in this location but it will be easy to eclipse to auto detect toolchain and OpenOCD
 - Detail for setup and test OpenOCD can be found [here](https://github.com/LieBtrau/Aiakos/wiki/STM32L053-Nucleo-toolchain-setup)
 - Telnet use port 4444
 - GDB use port 3333

Open other terminal, Start OpenOCD server with this command (Nucleo board must be connected).
```sh
openocd -f board/stm32l0discovery.cfg
```

#### 2. Install Eclipse and ARM-Eclipse Plugin.
 - Installl Eclipse Neon 3, Use C/C++ for default workspace.
 - Install the GNU ARM plug-in for Eclipse
 - Setup GNU ARM Plug-in
    - Detail 1
    - Detail 2
### 3. [Installing STM32CubeMX on Linux](https://gist.github.com/Lanchon/2156953d18f7534a926b)
The STM32CubeMX tool is written in portable java, but unfortunately it is distributed as a Windows executable embedded in a Windows installer.

To intall it on Linux:

1. sudo java -jar SetupSTM32CubeMX-4.11.0.exe
2. install the tool somewhere in your home, eg: /home/you/stm32/cubemx
3. sudo chown -R you:you /home/you/stm32/cubemx

To run it:

* java -jar /home/you/stm32/cubemx/STM32CubeMX.exe
* or mark that file as executable, rename it to STM32CubeMX.jar, and double click it
    
#### 4. Clone this Repo and open with eclipse.
---

## (Optional) How to set up this environmet in detail.
These are original source and tutorial.
 - Setting up a GCC/Eclipse toolchain for STM32Nucleo[Part1](http://www.carminenoviello.com/2014/12/28/setting-gcceclipse-toolchain-stm32nucleo-part-1/) [Part2](http://www.carminenoviello.com/2015/01/07/setting-gcceclipse-toolchain-stm32nucleo-part-2/) [Part3](http://www.carminenoviello.com/2015/01/16/setting-gcceclipse-toolchain-stm32nucleo-part-iii/)
 - [Running FreeRTOS on a STM32Nucleo using a free GCC/Eclipse toolchain](http://www.carminenoviello.com/2015/06/22/running-freertos-stm32nucleo-free-gcceclipse-toolchain/)
 - [mbed-os](https://github.com/ARMmbed/mbed-os)   
 - [mbed_NucleoL053R8](https://github.com/Hotboards/mbed_NucleoL053R8)
 
