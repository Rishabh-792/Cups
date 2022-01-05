#Steps taken to install cups locally

The first step is to clone the cups repository through the following command:
```
git clone https://github.com/OpenPrinting/cups.git
```

After clone was successful, I moved into the cups directory and configured CUPS for my system through the usual "configure" script in the main CUPS source directory, using the following command:
```
./configure
```

Then I wrote the make command:
```
make 
sudo make install
```

Start the CUPS service using:
```
sudo /usr/sbin/cupsd -f
```
