# GetChromeOSWifiPassword-
How to get wifi password of an enterprise Chromebook in plaintext

1.  Unenroll the Chromebook from the enterprise using any method
2.  Activate dev mode and set the root password
    - enter recovery using esc + power + refresh
    - ctrl + d
    - hit enter
    - hit ctrl + d
    - wait for dev mode to install or whatever
    - hit ctrl + d
    - Once you are on the welcome screen, click the enable debugging features and disable rootfs
    - Enter your desired password for root
4. Connect to wifi and re-enroll in the enterprise 
5. You can now use the VT-2 terminal for this session (until it restarts)
6. Enter the terminal(ctrl + alt + → (the one on top of keyboard))
7. Log in
   - login name: root
   - password: whatever you set, default is test00000
8. type ``cd /var/cache/shill``
9. Then type ``ls``
10. You will see two files ending in .profile, the default.profile has all the wifi info
11. type ``cat default.profile | grep Password`` to get wifi password (or any other info on the wifi) 
