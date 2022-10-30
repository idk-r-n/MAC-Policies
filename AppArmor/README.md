# AppArmor Profiles

AppArmor Profiles tested on Ubuntu-based distributions

Many rules can be simplified by creating files and directories specifically for the app. For example, all the rules pertaining to the home directory can be simplified by using [bubblewrap](https://github.com/containers/bubblewrap) to create a new home directory specificlly for one app with a simple bind: `bwrap --ro-bind / / --bind $HOME/new_home_folder/ $HOME /usr/bin/bash`.
