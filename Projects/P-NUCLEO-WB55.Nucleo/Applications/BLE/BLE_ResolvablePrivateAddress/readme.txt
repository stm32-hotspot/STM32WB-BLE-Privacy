/**
  @page BLE_ResolvablePrivateAddress Application

  @verbatim
  ******************************************************************************
  * @file    BLE/BLE_ResolvablePrivateAddress/readme.txt 
  * @author  MCD Application Team
  * @brief   Description of the BLE_ResolvablePrivateAddress application
  ******************************************************************************
  *
  * Copyright (c) 2019-2022 STMicroelectronics.
  * All rights reserved.
  *
  * This software is licensed under terms that can be found in the LICENSE file
  * in the root directory of this software component.
  * If no LICENSE file comes with this software, it is provided AS-IS.
  *
  ******************************************************************************
  @endverbatim

@par Application Description

Demonstrates how enable Bluetooth LE Resolvable Private Address using the BLE component. 

One STM32WB55xx board is used, acting as GAP peripheral and GATT server, and an Android smartphone as the GAP Central/GATT client.
The BLE_ResolvablePrivateAddress application is downloaded in a NUCLEO-WB55RG (MB1355).
On the Android Smartphone, and app like Punchthrough LightBlue can be used.  Note that an Android device is preferred to use over iOS device for demontration purposes of this Resolvable Private Address (RPA) privacy feature because Android allows reading the MAC address from the advertising packets and can therefore display it on the scan window, while iOS does not allow this.  

	
@par Keywords

Connectivity, BLE, IPCC, HSEM, RTC, UART, PWR, BLE protocol, BLE pairing, BLE profile, Dual core

@par Directory contents 
  
  - BLE/BLE_ResolvablePrivateAddress/Core/Inc/stm32wbxx_hal_conf.h	        HAL configuration file
  - BLE/BLE_ResolvablePrivateAddress/Core/Inc/stm32wbxx_it.h          		Interrupt handlers header file
  - BLE/BLE_ResolvablePrivateAddress/Core/Inc/main.h                  		Header for main.c module
  - BLE/BLE_ResolvablePrivateAddress/STM32_WPAN/App/app_ble.h           	Header for app_ble.c module
  - BLE/BLE_ResolvablePrivateAddress/Core/Inc/app_common.h            		Header for all modules with common definition
  - BLE/BLE_ResolvablePrivateAddress/Core/Inc/app_conf.h              		Parameters configuration file of the application
  - BLE/BLE_ResolvablePrivateAddress/Core/Inc/app_entry.h            		Parameters configuration file of the application
  - BLE/BLE_ResolvablePrivateAddress/STM32_WPAN/App/ble_conf.h            	BLE Services configuration
  - BLE/BLE_ResolvablePrivateAddress/STM32_WPAN/App/ble_dbg_conf.h        	BLE Traces configuration of the BLE services
  - BLE/BLE_ResolvablePrivateAddress/STM32_WPAN/App/p2p_server_app.h      	Header for p2p_server_app.c module
  - BLE/BLE_ResolvablePrivateAddress/Core/Inc/hw_conf.h           			Configuration file of the HW
  - BLE/BLE_ResolvablePrivateAddress/Core/Inc/utilities_conf.h    			Configuration file of the utilities
  - BLE/BLE_ResolvablePrivateAddress/Core/Src/stm32wbxx_it.c          		Interrupt handlers
  - BLE/BLE_ResolvablePrivateAddress/Core/Src/main.c                  		Main program
  - BLE/BLE_ResolvablePrivateAddress/Core/Src/system_stm32wbxx.c      		stm32wbxx system source file
  - BLE/BLE_ResolvablePrivateAddress/STM32_WPAN/App/app_ble.c      			BLE Profile implementation
  - BLE/BLE_ResolvablePrivateAddress/Core/Src/app_entry.c      				Initialization of the application
  - BLE/BLE_ResolvablePrivateAddress/STM32_WPAN/App/p2p_server_app.c   		P2P Server application
  - BLE/BLE_ResolvablePrivateAddress/STM32_WPAN/Target/hw_ipcc.c      		IPCC Driver
  - BLE/BLE_ResolvablePrivateAddress/Core/Src/stm32_lpm_if.c				Low Power Manager Interface
  - BLE/BLE_ResolvablePrivateAddress/Core/Src/hw_timerserver.c 				Timer Server based on RTC
  - BLE/BLE_ResolvablePrivateAddress/Core/Src/hw_uart.c 					UART Driver
  
@par Hardware and Software environment

    - This application runs on STM32WB55xx Nucleo board (MB1355)
        
    - Nucleo board (MB1355) Set-up    
       - Connect the Nucleo Board to your PC with a USB cable type A to mini-B to ST-LINK connector (USB_STLINK).
       - Please ensure that the ST-LINK connectors and jumpers are fitted.

@par How to use it ? 

This application requires having the stm32wb5x_BLE_Stack_full_extended_fw.bin binary flashed on the Wireless Coprocessor.
If it is not the case, you need to use STM32CubeProgrammer to load the appropriate binary.
All available binaries are located under /Projects/STM32_Copro_Wireless_Binaries directory.
Refer to UM2237 to learn how to use/install STM32CubeProgrammer.
Refer to /Projects/STM32_Copro_Wireless_Binaries/ReleaseNote.html for the detailed procedure to change the
Wireless Coprocessor binary.  
   
In order to make the program work, you must do the following :
 - Open your preferred toolchain 
 - Rebuild all files and load the image into Target memory
 - OR use the BLE_ResolvablePrivateAddress_reference.hex from Binary directory
 - This must be done for BLE_ResolvablePrivateAddress (MB1355) 

On the android device, enable the Bluetooth communications, and if not done before,
 - Install the Punchthrough LightBlue application on the android device
	https://play.google.com/store/apps/details?id=com.punchthrough.lightblueexplorer&hl=en_US&gl=US

See Readme.md in the example root directory for step-by-step instructions.  

   For more details refer to the Application Note: 
  AN5289 - Building a Wireless application  
 
 * <h3><center>&copy; COPYRIGHT STMicroelectronics</center></h3>
 */
