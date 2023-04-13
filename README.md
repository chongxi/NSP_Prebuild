# NSP_Prebuild
================= unzip OEGUI_prebuilt.7z =================
7z x ./OpenEphysGUI/OEGUI_prebuilt.7z

================= rules for udev =================
sudo cp ./OpenEphysGUI/40-open-ephys.rules /etc/udev/rules.d
sudo cp ./FPGA_NSP/10-xillybus.rules /etc/udev/rules.d
sudo service udev restart

================= add to bash =================
export PATH="./FPGA_NSP/command:$PATH"
alias open-ephys="./open-ephys"