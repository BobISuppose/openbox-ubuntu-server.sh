# openbox-ubuntu-server.sh
Openbox with light desktop environment 


pull it into your server

git clone https://github.com/YOURUSERNAME/ubuntu-openbox-installer.git
cd ubuntu-openbox-installer
chmod +x openbox-ubuntu-server.sh
./openbox-ubuntu-server.sh



ubuntu-openbox-installer/
├── README.md
├── install.sh              # main entry point
├── scripts/
│   ├── base.sh             # updates, essentials
│   ├── xorg.sh             # graphics stack
│   ├── openbox.sh          # WM + config
│   ├── apps.sh             # file manager, tools
│   └── extras.sh           # optional stuff
├── config/
│   └── openbox/
│       ├── autostart
│       └── rc.xml
└── uninstall.sh            # optional later