# Brightness Control for External Monitors

* Written for easy control of Brightness for multiple monitors.  
* Uses xrandr package in linux.    
* Tested only on Ubuntu 18.04 LTS, but may work on all other Linux Destros.

# Directions

* Make the file executable by running `chmod +x path_to_b`
* Copy the file `b` to any system path. preferably to `~/bin` if you are not a sudoer
* Now you can Use it to control brightness as `b <display> <brightness>`
* For help, try `b -h` or `b --help`

#### Update
* Now you can save multiple configrations by using `b <display> <brightness> --set <mode>` and apply them again easily with `b --mode <mode>` or just `b -m <mode>` .

Display No. starts from 1 and Brightness varies from 0 to 1

# Hit star if you like it
