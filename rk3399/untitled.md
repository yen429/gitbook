# AP6255 File Location

1. AP6255 BT Firmware/WiFi Firmware/NVRAM是由益登Release給我們的，取得後，如需更新，則將檔案放置下列的BSP位置:  

   **BT Firmware:**  

   vendor\rockchip\common\bluetooth\lib\firmware\BCM4345C0.hcd  

   **WiFi Firmware:**  

   vendor\rockchip\common\wifi\firmware\fw\_bcm43455c0\_ag.bin  

   vendor\rockchip\common\wifi\firmware\fw\_bcm43455c0\_ag\_apsta.bin  

   **NVRAM Location:**  

   vendor\rockchip\common\wifi\firmware\nvram\_ap6255.txt  

2. 當Android開機後，這幾個檔案會放置在File System的下面位置:  

   **BT Firmware:**  

   \vendor\etc\firmware\BCM4345C0.hcd  

   **WiFi Firmware:**  

   \vendor\etc\firmware\fw\_bcm43455c0\_ag.bin  

   \vendor\etc\firmware\fw\_bcm43455c0\_ag\_apsta.bin  

   **NVRAM Location:**  

   \vendor\etc\firmware\nvram\_ap6255.txt  

   測試時, 如果Android 是user-debug版本, 可以用adb root/adb remount/adb push將檔案push至上面的位置中, 來進行快速測試

3. 如何確認目前WiFi Firmware & NVRAM Version?

   WiFi Firmware版本需要使用rftesttool中的wl才能看到 (執行wl需要先root)
   
   ![image](https://github.com/yen429/gitbook/blob/master/rk3399/picture/wifi_fw_version.png)
   
   要確認NVRAM版本，只要cat nvram_ap6255.txt，裡面的第一行就是版本
   
   ![image](\picture\nvram_version.png)
   
4. RF在進行發生Non-Signaling Mode測試時，5G MCS5~7 TX Power與EVM測試fail，後來更新NVRAM 就可以Pass了:
   
   \vendor\etc\firmware\nvram_ap6255.txt
    
5. 相關Girrit Link如下:
   
   http://twtps524.tpvaoc.com:1001/#/c/33960/
   
   http://twtps524.tpvaoc.com:1001/#/c/33839/


