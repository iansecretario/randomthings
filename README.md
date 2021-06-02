# randomthings
Random things that help me



```export session="labs" # or "exercises" or "exam"
mkdir -p "workspace/${session}/logs"
cd "workspace/${session}"
echo $'script -a "logs/$(tty | sed -E \'s/\\W/_/g\')-$(date -Iseconds)"' > .tmux_profile
tmux new -s "${session}"```
