## On Steam deck
sudo systemctl start sshd
## On PC
sshfs deck@192.168.100.63:/home/deck ~/SteamDeckMount/
fusermount -u ~/SteamDeckMount/