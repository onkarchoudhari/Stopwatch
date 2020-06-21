# Stopwatch

"Lost time is never found again" - Benjamin Franklin.

Time is one of the most precious gift in anyone's life. Unfortunately, the more you have it, the more you waste. 

In order to track the lost time, this simple stopwatch was designed. 

This stop watch will give show time in the system tray when you run it from terminal. This will help you to monitor how much work you did and will also remind you that the time is flowing, don't waste it!!

# Installation

The clock can be ran on Linux OS only (as of now, will soon make it possible to run on Windows and MacOS too. Just wait for it!)

Open a terminal.<br>
Clone the project in the desired directory.<br> 
To clone in the home directory:<br> 
`git clone https://github.com/onkarchoudhari/Stopwatch.git`<br>

Go to the Stopwatch Directory<br>
`cd Stopwatch`<br>

Make the files executable<br>
```
chmod a+x my_stopwatch
chmod a+x my_stopwatch_srcipt
```

Run the file<br>
`./my_stopwatch`

NOTE: In order to show the time in system tray, you need to have System Monitor installed on your system. 

# System Monitor Settings

Install Indicator System Monitor. 
```
sudo add-apt-repository ppa:fossfreedom/indicator-sysmonitor
sudo apt-get update
sudo apt-get install indicator-sysmonitor
```

Click the Super key and type Indicator System Monitor. 

In case it doesn't work properly, follow the steps mentioned below. 

To run Indicator System Monitor Properly type the following commands in the terminal
```
sudo apt install libappindicator-dev
sudo cpan -i Gtk2::AppIndicator
```

Then using the link: `https://extensions.gnome.org/`, search for `AppIndicator` and `Taskbar` Extensions and install them. 
Click the Super button and type Indicator System Monitor. 

Click on the cpu utilization mentioned in the top bar and then click Preferences.
In `General` tab check the `Run on Startup` box. 
Go to `Advanced` tab. 
Click on `New` button. In `sensor` write `custom`. In description mention
`Stopwatch`. In `command` write `~/Stopwatch/my_stopwatch_script` 
(NOTE: Here mention the path for the `my_stopwatch_script` executable)
Then click `OK`.

Now in the `Customize Output` bar, enter: 
{custom}           cpu: {cpu} mem: {mem}

In update interval, make it 1 instead of 2.

Now, open the terminal and go to the directory where stopwatch files are
present and type `./my_stopwatch`.

