# AP6255 File Location

1. AP6255 BT Firmware/WiFi Firmware/NVRAM是由益登Release給我們的, 取得後, 如需更新, 則將檔案放置下列的BSP位置:  
BT Firmware:  
vendor\rockchip\common\bluetooth\lib\firmware\BCM4345C0.hcd  
WiFi Firmware:  
vendor\rockchip\common\wifi\firmware\fw\_bcm43455c0\_ag.bin  
vendor\rockchip\common\wifi\firmware\fw\_bcm43455c0\_ag\_apsta.bin  
NVRAM Location:  
vendor\rockchip\common\wifi\firmware\nvram\_ap6255.txt  
2. 當Android開機後, 這幾個檔案會放置在File System的下面位置:  
BT Firmware:  
\vendor\etc\firmware\BCM4345C0.hcd  
WiFi Firmware:  
\vendor\etc\firmware\fw_bcm43455c0_ag.bin  
\vendor\etc\firmware\fw_bcm43455c0_ag_apsta.bin  
NVRAM Location:  
\vendor\etc\firmware\nvram_ap6255.txt  
測試時, 如果Android 是user-debug版本, 可以用adb root/adb remount/adb push將檔案push至上面的位置中, 來進行快速測試

