hdmi_vdma_passthrough_aud project 
this version : support up to 3840x2160@30fhz resolution's video  and support 32 bit 2 channel with 48k sample rate for passsthrough AES3 foramt audio data  

to be updated:
4k@60hz repulicate hpd issue  
dynmaic_config_VDMA(): to be support rx timing custom mode  
to be support DRU function


hardware setup:   
1 hdmi_mgb2_v11 at ht3_a24, ddr_ht3 8g at ht3_a15,a16,a17  
hdmi_mgb2 j1 connect to mgb2 am221  

program process:  
open hasp100-runtime bat: drives/C/Synopsys/protocomp-rtR-2020.12-SP1/bin/confprosh.bat  
cd C:\HAPS100_1F\02_confpro_scripts  
confprosh  
source 00_configure.tcl  
source 01_jtag_start.tcl  
connect_hw_server  
open_hw_target -xvc_url localhost:65137  

source 02_jtag_close.tcl

