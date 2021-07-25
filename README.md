# ChipDip-DAC-driver-Volumio

1) Install git

sudo apt install git

2) Clone git repository

git clone https://github.com/chipdipru/ChipDip-DAC-driver-Volumio

3)

sudo cp ChipDip-DAC-driver-Volumio/snd-soc-chipdip-dac-4.19.188-v7.ko /lib/modules/uname -r/kernel/sound/soc/bcm/snd-soc-chipdip-dac.ko

4)

sudo depmod

5)

sudo nano /volumio/app/plugins/system_controller/i2s_dacs/dacs.json

In the DAC list add

{"id":"chipdip-master-dac","name":"CHIPDIP Master DAC","overlay":"chipdip-dac-gpio","alsanum":"2","mixer":"","modules":"","script":"","needsreboot":"yes"},

6)

reboot
