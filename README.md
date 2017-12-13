STM32F4 Discovery Demo Firmware for arm-none-eabi-gcc
==========================================

* Author:    Nabil Tewolde (<nabil.tewolde@gmail.com>)
* Version:   0.0.1
* Website:   <https://nabil.me/category/stm32f4/>
* GitHub:    <https://github.com/nabilt/STM32F4-Discovery-Firmware>


Version V1.0.1
<http://www.st.com/internet/com/SOFTWARE_RESOURCES/SW_COMPONENT/FIRMWARE/stm32f4discovery_fw.zip>

From ST's documentation...
The STM32F4-Discovery Board Firmware Applications Package provides ready-to-run firmware examples to support quick evaluation and development on STM32F4-Discovery board. For more information on the STM32F4-Discovery and to download the available firmware package visit www.st.com/stm32f4-discovery.

Peripheral Examples
* ADC3_DMA			
* EXTI
* IWDG
* PWR_STOP
* TIM_ComplementarySignals
* ADC_Interleaved_DMAmode2	
* FLASH_Program			
* MEMS				
* RCC				
* TIM_PWM_Input
* DAC_SignalsGeneration		
* FLASH_Write_Protection		
* PWR_CurrentConsumption		
* TIM_PWM_Output
* DMA_FLASH_RAM			
* IO_Toggle			
* PWR_STANDBY			
* SysTick				
* TIM_TimeBase

Instructions
____________
<https://nabil.me/2011/10/30/using-the-stm32f4-discovery-board-in-osx-lion/>

Usage
-----
    git clone https://github.com/nabilt/STM32F4-Discovery-Firmware.git
    cd STM32F4-Discovery_FW_V1.0.1/Project/IO_Toggle
    make && make program
    openocd -f ../../openocd_config/openocd.cfg -f ../../openocd_config/stm32f4x.cfg

In another terminal

    arm-none-eabi-gcc
    (gdb) target extended localhost:3333
    (gdb) # reset and halt the chip
    (gdb) monitor halt
    (gdb) # load symbol files
    (gdb) file demo.elf
    (gdb) # load demo.elf into RAM
    (gdb) load demo.elf
    Loading section .isr_vector, size 0x188 lma 0x8000000
    Loading section .text, size 0xc5c lma 0x8000188
    Loading section .data, size 0x38 lma 0x8000de4
    Start address 0x8000d6c, load size 3612
    Transfer rate: 6 KB/sec, 1204 bytes/write.
    (gdb) run the program. hit Control-C to stop
    (gdb) continue
 
