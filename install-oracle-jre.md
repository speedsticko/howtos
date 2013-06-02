put the line

deb http://www.duinsoft.nl/pkg debs all

in the file /etc/apt/sources.list, either using Software Sources from your System Menu or by editing the file in an editor (as root)
or:
put this line in a file named (e.g.) duinsoft.list in the directory /etc/apt/sources.list.d
import the gpg key with the command (all on one line)

sudo apt-key adv --keyserver keys.gnupg.net --recv-keys 5CB26B26

enter the commands (two lines)

sudo apt-get update
sudo apt-get install update-sun-jre

or use Synaptic to install the package
installation of the Runtime Environment will follow automatically

* ref: http://www.duinsoft.nl/packages.php?t=en
* ref: https://help.ubuntu.com/community/Java
