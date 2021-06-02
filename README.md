# randomthings
Random things that help my life easier


# Tmux 
```export session="engagement" # or experiments" or "laboratory"
mkdir -p "workspace/${session}/logs"
cd "workspace/${session}"
echo $'script -a "logs/$(tty | sed -E \'s/\\W/_/g\')-$(date -Iseconds)"' > .tmux_profile
tmux new -s "${session}"```


# hosts
echo "192.168.xx.xx kali" >> /etc/hosts

