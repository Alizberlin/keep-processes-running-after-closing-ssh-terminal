# Keep processes running after ending ssh session.

1. ssh into the remote machine
2. start tmux by typing 

        § tmux
    into the shell
3. start the process you want inside the started tmux session
leave/detach the tmux session by typing "Ctrl+b" and then "d"

You can now safely log off from the remote machine, your process will keep running inside tmux. When you come back again and want to check the status of your process you can use "§ tmux attach" to attach to your tmux session.

If you want to have multiple sessions running side-by-side, you should name each session using "Ctrl+b" and "$". You can get a list of the currently running sessions using "§ tmux list-sessions" or simply "§ tmux ls", now attach to a running session with command " § tmux attach-session -t <session-name>".

tmux can do much more advanced things than handle a single window in a single session. For more information have a look in " § man tmux".