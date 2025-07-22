Playit Installation:  
`curl -SsL https://playit-cloud.github.io/ppa/key.gpg | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/playit.gpg >/dev/null`  
`echo "deb [signed-by=/etc/apt/trusted.gpg.d/playit.gpg] https://playit-cloud.github.io/ppa/data ./" | sudo tee /etc/apt/sources.list.d/playit-cloud.list`  
`sudo apt update`  
`sudo apt install playit`  

There are 2 ways to make sure playit is always running, TMUX and creating a new startup script.  
**TMUX Version:**  
Run `tmux new -s playit`, inside the terminal window type `playit`, after the proxy connects press `Ctrl + B` then `D`  
To reattach to the tmux session use `tmux attach -t playit`  
**Startup Script:**  
Create a new service file using `sudo nano /etc/systemd/system/playit.service`  
Add the following content to the file:  
`[Unit]`  
Description=Playit Tunnel`  
After=network.target`  
  
[Service]`  
ExecStart=/path/to/playit`  
Restart=always`  
User=your-username`  
WorkingDirectory=/home/your-username`  
StandardOutput=journal`  
    
[Install]  
WantedBy=multi-user.target`  
