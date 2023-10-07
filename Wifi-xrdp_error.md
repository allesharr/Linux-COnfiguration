1. sudo apt install xrdp
2. sudo usermod -aG ssl-cert $USER
3. sudo usermod -aG xrdp $USER
4. sudo nano /etc/xrdp/xrdp.ini
check lines
    [Xorg]
    name=Xorg
    lib=libxup.so
    #username=ask
    username=allesharr
    password=Lihtenstein1
    #password=ask
    ip=127.0.0.1
    port=-1
    code=20
5. sudo nano /etc/polkit-1/localauthority/50-local.d/47-allow-wifi-scans.pkla
Add lines
    [Allow Wifi Scan]
    Identity=unix-user:*
    Action=org.freedesktop.NetworkManager.*
    ResultAny=yes
    ResultInactive=yes
    ResultActive=yes