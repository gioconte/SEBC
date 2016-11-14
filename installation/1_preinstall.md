#Checking swappiness
cat /proc/sys/vm/swappiness

60

Temporarily setting it to value of 1.
sudo sysctl vm.swappiness=1

Set vm.swappiness to 1 in a permanet way.
sudo vi /etc/sysctl.conf and add line vm.swappiness=1



