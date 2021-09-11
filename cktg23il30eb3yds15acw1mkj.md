## An easy way to install Android Studio

#### Follow the steps below to install [Android Studio]:

1. Install Java JDK and update all.
2. Install Android libaries as: `libc6:i386`, `libncurses5:i386`, `libstdc++6:i386`, `lib32z1` and `libbz2-1.0:i386`.
3. Download Android Studio tar.gz file and extract it.
4. Make a shortcut to open it from menu.

#### Shortcut to open it from application menu:
I prefered use Sublime Text, Gedit or other visual editor `sudo subl /usr/share/applications/android-studio.desktop` but you can make it with Nano, Vim and other in terminal for example `sudo nano /usr/share/applications/android-studio.desktop`.

#### Script to copy and paste in android-studio.desktop:
```
[Desktop Entry]
Version=1.0
Type=Application
Name=Android Studio
Comment=Android Studio
Exec=bash -i "/opt/android-studio/bin/studio.sh" %f
Icon=/opt/android-studio/bin/studio.png
Categories=Development;IDE;
Terminal=false
StartupNotify=true
StartupWMClass=jetbrains-android-studio
Name[en_GB]=android-studio.desktop
```


![image](https://cdn.hashnode.com/res/hashnode/image/upload/v1631380850917/BhiAB6hjw.jpeg)

I did a simple script to make all the process a little bit easy than it is in general. Just save the script below with the extension .sh and run it in terminal as `bash android-studio.sh`.

```Bash
#!/bin/bash
echo = "Installing Android Studio completly. Press ENTER to confirm and CTRL+C to cancel."
read enter
echo "Installing Java repository"
sudo add-apt-repository ppa:webupd8team/java
echo "Update packages"
sudo apt-get update -y
echo "Installing Java"
sudo apt-get install -y oracle-java8-installer
sudo apt-get install -y oracle-java8-set-default
echo "Check Java version"
javac -version

echo "Installing Android libaries."
sudo apt-get install libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386

echo "Dowmloading Android Studio tar.gz file."
wget https://redirector.gvt1.com/edgedl/android/studio/ide-zips/2020.3.1.24/android-studio-2020.3.1.24-linux.tar.gz

echo "Extracting tar.gz file"
sudo tar -zxvf android-studio-2020.3.1.24-linux.tar.gz

echo "Moving directory with all files to path /opt"
sudo mv android-studio /opt/

echo "Creating a symlink to an existing directory"
sudo ln -sf /opt/android-studio/bin/studio.sh /bin/android-studio

echo "Creating a .desktop file in /usr/share/applications directory to start it from menu. The script below must be copy in this file:"

echo "
[Desktop Entry]
Version=1.0
Type=Application
Name=Android Studio
Comment=Android Studio
Exec=bash -i "/opt/android-studio/bin/studio.sh" %f
Icon=/opt/android-studio/bin/studio.png
Categories=Development;IDE;
Terminal=false
StartupNotify=true
StartupWMClass=jetbrains-android-studio
Name[en_GB]=android-studio.desktop
"

sudo nano /usr/share/applications/android-studio.desktop


echo "Check the news about Android Studio on https://developer.android.com/studio"
echo "Developed by Mayanna Oliveira | https://beacons.ai/mayannaoliveira"
```

*If you have doubts about it you can talk with me in comments.*
Please, before run this script check the [Android Studio] version to have the last one installed in your machine. 

##### References about Android Studio:
[Download](https://developer.android.com/studio), [User Guide](https://developer.android.com/guide), [Documentation](https://developer.android.com/docs), [NDK](https://developer.android.com/ndk), [Developer Podcasts](https://developer.android.com/podcasts) and [Android Developers](https://www.youtube.com/user/androiddevelopers)

[Android Studio]: https://developer.android.com/studio

