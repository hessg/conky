# conky
This is the conky config for my PC

The local weather is being curled from wttr.in and the info is stored in ~/.wttr.in
The service recognizes your location from your ip so you don't *have* to put your location in
Displaying the ascii art for the weather is done with a bunch of 'sed' and 'awk' commands sometimes breaks a bit
Weather info is being updated every 1h if you don't have newer data in ~/.wttr.in

It also checks some monitoring info from my raspi in my local network
the connection to the PI is done in pi_conky.sh via ssh with an ssh key
the ip address and user is configured there as well, in the variable $raspi

This runs with kde


# TODO
Put github token into ~/.config/conky/github_token    
Test if this actually still works, or find a way to make it work  
Upload screen background picture, the conky colours are matching it  
Fix the sed and awk commands to always display the weather nicely  
