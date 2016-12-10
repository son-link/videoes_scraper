#Scrap XML Gamelist for ES with video support
Attention: overwrites gamelist.xml without asking.
Without options it scrap data for mame-libretro on retropie

## Installation
```bash
git clone https://github.com/capsaicincapsicum/videoes_scraper.git
```

## Scrap NES Games on Retropie
```bash
./videoes_scraper/videoes_scraper -e nes
```

## Install ES with video support
```bash
# install packages
sudo apt-get update
sudo apt-get --yes install vim vlc libvlc-dev libvlc5

# get and compile
git clone https://github.com/fieldofcows/EmulationStation.git
cd EmulationStation/
cmake . -DFREETYPE_INCLUDE_DIRS=/usr/include/freetype2/
make clean
make

# auto start video emulatorstation
sudo sed -i 's/\/.*emulationstation\.sh/\/home\/pi\/EmulationStation\/emulationstation\.sh/' /usr/bin/emulationstation
```

## Get Theme:
http://download1336.mediafire.com/yr7ktkelzg9g/j91ai4widytm076/oldroom+1.7b+720p.zip
