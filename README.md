# **Gunbird 2 - Unlock Aine**

This patch makes Aine unlocked by default in the Gunbird 2 MAME rom. It has no other effect. The advantage to unlocking Aine in this manner, as opposed to using the built-in password, is mainly that you will be able to record and playback Gunbird 2 demos in MAME with all characters, while disabling nvram. Which will let you avoid demo desync. After patching your rom, make sure to add the following command to both your recording and playback shortcuts:  

If using Shmupmame 4.2:  -nvram_directory nul          
Example: \Shmupmameui_v42.exe gunbird2 -record gb2demo.inp -nvram_directory nul

If using regular MAME:    -nonvram_save                 
Example: \mame.exe gunbird2 -record gb2demo.inp -nonvram_save  

Before launching the patched game like this, make sure your MAME nvram directory has no "gunbird2" folder in it.

## Patching Instructions:

1 - Extract your MAME Gunbird 2 rom archive (gunbird2.zip)

2 - Using your xdelta patcher of choice, apply the gunbird2-aine.xdelta patch to the file named "eeprom-gunbird2.bin". Make sure that your patched file has the same filename as the original.

3 - Rezip the Gunbird 2 rom archive.
  
  
##### NOTE: When you start up the patched rom, MAME will complain about wrong checksum. This is expected, and can be safely ignored. If necessary, the patching process can be verified using the hashes below:
  
eeprom-gunbird2.bin

(Original) &nbsp; CRC32:&nbsp; 7ac38846  
(Original) &nbsp; MD5:  &nbsp; &nbsp;   601b25e54e95f09bcd2c028af884841e  
(Original) &nbsp; SHA-1: &nbsp; c5f4b05a94211f3c96b8c472adbe634f2e77d753  
  
(Patched) &nbsp; CRC32:&nbsp; acc93b51  
(Patched) &nbsp; MD5:  &nbsp; &nbsp;   d826969537b4a98d0ee1029b3aaf1559  
(Patched) &nbsp;  SHA-1: &nbsp; 6bb49f322d2bc9d3b1616944a45d32d0bb476e27  
