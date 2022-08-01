# tp-link-tl-wn722n-monitor-mode
tp-link tl-wn722n monitor mode 
Test on kali linux 2022.2 - V - 5.16.0-kali7-amd64

sudo apt update
sudo apt install bc
sudo rmmod r8188eu.ko
git clone https://github.com/aircrack-ng/rtl8188eus
cd rtl8188eus
sudo -i
echo "blacklist r8188eu" > "/etc/modprobe.d/realtek.conf"
exit

https://http.kali.org/kali/pool/main/l/linux/

download from this site - (do "uname -r" for know your V kali).

1) linux-headers-5.16.0-kali7-amd64_5.16.18-1kali1_amd64.deb
2) linux-headers-5.16.0-kali7-common_5.16.18-1kali1_all.deb
3) linux-kbuild-5.16_5.16.18-1kali1_amd64.deb

do dpkg for all 3 deb file


move to :  rtl8188eus folder (again)

make
sudo make install
sudo modprobe 8188eu


>>>>>

ifconfig wlan0 down
iwconfig wlan0 mode monitor
ifconfig wlan up
