# randomthings
Random things that help me



```export session="engagement" # or experiments" or "laboratory"
mkdir -p "workspace/${session}/logs"
cd "workspace/${session}"
echo $'script -a "logs/$(tty | sed -E \'s/\\W/_/g\')-$(date -Iseconds)"' > .tmux_profile
tmux new -s "${session}"```
