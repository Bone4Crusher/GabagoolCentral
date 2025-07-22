Playit Installation:
`
curl -SsL https://playit-cloud.github.io/ppa/key.gpg | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/playit.gpg >/dev/null
echo "deb [signed-by=/etc/apt/trusted.gpg.d/playit.gpg] https://playit-cloud.github.io/ppa/data ./" | sudo tee /etc/apt/sources.list.d/playit-cloud.list
sudo apt update
sudo apt install playit
`
There are 2 ways to make sure playit is always running, TMUX and creating a new startup script. 
TMUX Version: 
Run `tmux new -s playit`, inside the terminal window type `playit`, after the proxy connects press `Ctrl + B` then `D`
