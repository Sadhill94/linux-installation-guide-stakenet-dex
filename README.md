# Stakenet DEX Linux installation guide

###### Documentation status : **UNDER VALIDATION**

## 1. Download the dex
Please head to [this link](https://auto-updater-wallet-test.s3.us-east-2.amazonaws.com/light-wallet/staging/linux/installer/Stakenet.zip) to trigger a download.

### Optional - Download unzip if you haven't already
Open your terminal
```
sudo apt-get install unzip
```

## 2. Move the files to an appropriate folder
I like to have a my applications download on **/opt** folder on linux, if you don't want to place it there, move the dex to the folder of your choice, but don't forget to adapt the commands down below with your folder path.
Open your terminal and type
```
sudo unzip ~/Downloads/Stakenet.zip -d /opt/Stakenet
```

## 3. Launching the DEX
At this stage you can already use the dex, you can either use the raw launch via terminal 
or follow the guide down below to create a desktop icon 
### Optional - DEX Raw launch via the terminal
Run this command in the terminal :
```
/opt/Stakenet/AppRun
```

### Launch the DEX via single command or an desktop icon

##### Create a symbolic link
```
sudo ln -s /opt/Stakenet/AppRun /usr/bin/Stakenet
```
After that you can launch the dex via this simple command: `Stakenet`, then press enter.
Continue the guide if you wish to create a desktop icon.

##### Create an desktop icon
1. Copy paste this in your terminal
    ```
    cat << EOF > ~/.local/share/applications/Stakenet.desktop
    [Desktop Entry]
    Name=Stakenet DEX
    GenericName=Stakenet DEX
    X-GNOME-FullName=Stakenet DEX
    Comment=Stakenet crypto decentralized exchange
    Keywords=dex;
    Exec=/opt/Stakenet/AppRun
    Terminal=false
    Type=Application
    Icon=https://stakenet.io/favicon.ico
    Categories=Cryptocurrency;DEX;
    EOF
    ```
1. Open your Desktop menu, type Stakenet and you will see the entry Stakenet DEX (without icon currently)
1. Right click on it and select *Add to desktop*
1. Go to your desktop and right click on the new made Stakenet DEX entry
1. Heads up to the *Permissions* tab and verify that the  **Allow executing file as program** is **checked**
   ![alt text](https://imgur.com/9tJR0P3.png)
   
## 4. You're done !
Enjoy trading ! If you had a problem launching, reach out the [dex-support channel](https://discord.com/channels/374568694690611202/747528337123180615) on the Stakenet discord !
