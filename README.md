# GNU SCREEN ----- awwww yeahhh!

## Commands from a terminal on your remote server:

	screen -s <name of screen>	# start new screen
	screen -ls 					# list current screens
	screen -D -RR				# reattach here and now
	screen -r <pid from screen -ls command>		# reattach to screen by pid

## Commands in screen:

	C-a = Control + a

	C-a c 	# Create a new window
	C-a A		# Rename the current window
	C-a k		# Kill a window
	C-a n		# Go to next window
	C-a p		# Go to previous window
	C-a a		# Go to start of command line

	C-a :number <number> 	# Move current window to index <number>
	C-a <doublequotes> 		# List all windows
	C-a <singlequote> 		# Give prompt for name or number of window

## My method: 
I just use one screen with a slew of windows, so when I log in to my dev box it's just *screen -D -RR* and I am back where I left off.  

If you have the VPN running then from Mac Terminal you can do *ssh dev -t screen -D -RR* where *dev* is the SSH alias of your remote server.  Booyakasha.

Another handy trick is to remap Caps Lock to Control, which can be done in system preferences on your Mac.  This makes the *C-a* gesture a lot faster.

## How to use SSH Agent and Screen
Read [Managing SSH Sockets in GNU Screen](http://techblog.appnexus.com/?p=78)
