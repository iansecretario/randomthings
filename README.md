# randomthings
Random things that help my life easier

#Disable Defender

```reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender" /v DisableAntiSpyware /t REG_DWORD /d 1 /f
reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender\Real-Time Protection" /v DisableBehaviorMonitoring /t REG_DWORD /d 1 /f
reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender\Real-Time Protection" /v DisableOnAccessProtection /t REG_DWORD /d 1 /f
reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender\Real-Time Protection" /v DisableRealtimeMonitoring /t REG_DWORD /d 1 /f
reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender\Real-Time Protection" /v DisableScanOnRealtimeEnable /t REG_DWORD /d 1 /f
reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender\Spynet" /v SubmitSamplesConsent /t REG_DWORD /d 2 /f```
  gpupdate /force

# Tmux 
```export session="engagement" # or experiments" or "laboratory"
mkdir -p "workspace/${session}/logs"
cd "workspace/${session}"
echo $'script -a "logs/$(tty | sed -E \'s/\\W/_/g\')-$(date -Iseconds)"' > .tmux_profile
tmux new -s "${session}"```


# hosts
echo "192.168.1.xx kali" >> /etc/hosts
echo "192.168.1.xx win" >> /etc/hosts


alias l='ls -CF'
alias la='ls -A'
alias ll='ls -lah'
alias srv="python3 -m http.server 443 &"
alias srv80="python3 -m http.server 80 &"
alias srv8080="python3 -m http.server 8080 &"
alias smbsrv="sudo impacket-smbserver"
alias myip="echo;ip -c --brief addr | awk '{print \"\t\" \$1,\"\t\",\$3}';echo"
alias vs="   $1"
alias ..="cd .."
alias .="cd ."
alias /="cd /"
alias gomount="cd /mnt/hgfs/shared"
alias tcpA="nmap -sT -sC -sV -A -O -p -oA tcp_all_$1_$y$,$d-$T -nv $1"
alias udpA="nmap -sU -sC -p -oA udp_all_$1_%y%m%d-%T -nv $1"
alias udpT="nmap -sU -sC — top-ports 200 $1 -oA udp_top$1_$2_%y%m%d-%T -nv $2"
alias ge="gedit $1"
alias openport="netstat -nape --inet"
alias listenport="netstat -an | grep LISTEN | awk '{print $1}' | sort -n"


#screen
screen -S task1

#reconnect to task1
screen -S task1

#list sessions 
screen -ls

#move out of screen
ctrl + A + D

screen -dr 


#Powershell-fu
https://www.sans.org/blog/pen-test-poster-white-board-powershell-built-in-port-scanner/


