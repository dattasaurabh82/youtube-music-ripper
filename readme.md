#README

##About
A hypersimple Python program to facilitate ripping MP3 audio from YouTube videos (and ~150+ more supported sites as per http://rg3.github.io/youtube-dl/supportedsites.html). 

##Requirements
For this to work, you must have youtube-dl (http://youtube-dl.org) and ffmpeg installed. I'm going to provide instructions for the Mac, because that's what I and most of my friends use. 

###Install Homebrew
Hombrew is a package manager for Mac. It helps you install command line programs in a very useful manner. More info at http://brew.sh. 

If you don't already have it installed, open Terminal and copy/paste: 

`ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"`

and follow the instructions. 

###Install youtube-dl 
youtube-dl is a python library designed to interact with YouTube from the command line. More info at http://youtube-dl.org. 

You'll want to follow the download instructions on http://rg3.github.io/youtube-dl/download.html. If you don't know what any of this text means, the best solution is probably to copy/paste the following into Terminal: 

`sudo curl https://yt-dl.org/downloads/2014.02.13/youtube-dl -o /usr/local/bin/youtube-dl`

and then: 

`sudo chmod a+x /usr/local/bin/youtube-dl`

**Note: the link above is current at the date I committed this. It will almost certainly be updated when you read it, so don't copy/paste it from this page without checking to get the right one**

###Install ffmpeg 
ffmpeg is a framework to convert between media types. You can learn more at http://www.ffmpeg.org/about.html. 

Having installed Homebrew, you can easily install ffmpeg by copy/pasting: 

`brew install ffmpeg --devel` 

##How it works 
Everything in this program is run by ripper.py, which you can use in the following way: 

1. Download it to your preferred folder / directory (where all your music will appear too!)
2. Open up terminal and navigate to the directory where ripper.py is 
3. Type `python ripper.py` into terminal
4. Answer the prompts according to your fondest hopes and desires 
5. MP3 files should begin appearing where you want them to! 
6. After it runs, it will REMOVE all .M4A files in the directory you ran it in (because for some reason the --add-metadata flag breaks the automatic cleaning youtube-dl is supposed to do). This is probably desired behavior, but make sure you don't have any other M4A files in the same directory because it will nuke them too! 