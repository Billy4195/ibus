In ubunut 20.04, build ibus from source follows the belows steps

# Install dependencies from apt get

`sudo apt install -y gtk-doc-tools gnome-common libgtk2.0-dev libdconf-dev valac unicode-data`

# Download emoji support file 
emoji file from http://www.unicode.org/Public/emoji/4.0/ to /usr/share/unicode/emoji/

# install cldr emoji from github

```
git clone https://github.com/fujiwarat/cldr-emoji-annotation.git
./autogen.sh
./configure --prefix=/usr
make
sudo make install
```

# Build IBus

```
./autogen.sh --prefix=/usr --sysconfdir=/etc --with-ucd-dir=/usr/share/unicode
make
sudo make install 
```
