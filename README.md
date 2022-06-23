# Ubuntu_VirtualBox_Troubleshooting

После подключения VirtualBox Guest Additions и попытке запустить с помощью терминала:
sudo ./VBoxLinuxAdditions.run
получил ошибку:
Не удалось выполнить дочерний процесс "dbus-launch" (Нет такого файла или каталога)

Его можно установить с помощтю команды:
sudo apt install dbus-x11

После этого в окне VirtualBox Guest Additions installation возникает ошибка:
Please install the gcc make perl packages from your distribution.

Его можно установить с помощтю команды:
sudo apt-get install gcc make perl

Если Snap Store не хочет обновляться.
необходимо унитодить процесс snap-store:
  $ ps aux | grep snap
  Find <process id> for the snap-store process, which looks like this
  ... <process id> ... ... /snap/snap-store/???/usr/bin/snap-store
  
    Kill the above found process id
  $ kill <process id>
  
а затем его обновить
sudo snap refresh snap-store

https://superuser.com/a/1724268
