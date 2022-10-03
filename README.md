# LyricsToFCP
Automator script in JXA to add a formatted 1/3rds lyrics overlay to a Final Cut Pro X Library.

##**Note**
This is a *very* early release—I've not put any validation or error checking in here. I'm happy to help debug any issues, but expect things to break if you try anything werid (like special characters in the title!)

## **Introduction**
This package will install a service that can run on any text selection and generate a series of 5 second titles in Final Cut Pro for every pair of lines of text.


## **Installation**
Running the installer will install the following files:

~/Library/Application Support/LyricsToFCP/FCPLyricsBlank.fcpxml <-- template file that the script modifies

~/Library/Services/Send Lyrics to Final Cut Pro.workflow <--Automator workflow containing Javascript for Automation script

~/Movies/Motion Templates/Titles/Lyrics/2 Lines <--Final Cut Pro Title used in script.


## **Usage**
With any text selected, right click -> Services -> Send Lyrics to Final Cut Pro.

Note: The first line of text will be used as the title and will not appear in the timeline in Final Cut Pro.

A double line break will indicate the start of a new section and prevent the last line of a verse running into a chorus.


My typical usage is to copy lyrics into a Note or Textedit file, and format by adding new lines after the title, and where I know I want lyrics to not be merged with the following line (e.g. verse into chorus).

When the script is executed, Final Cut Pro will open and ask you where you want your Event saved. I created a new Library called "Lyrics", and then just copy the generated storyline to my working video project. All my auto-generated lyrics live in the Lyrics library.

### **Sample Lyrics**
This is what the script expects to see:

```
Amazing grace

Amazing Grace, How sweet the sound
That saved a wretch like me
I once was lost, but now am found
T'was blind but now I see

T'was Grace that taught my heart to fear
And Grace, my fears relieved
How precious did that grace appear
The hour I first believed

Through many dangers, toils and snares
We have already come.
T'was grace that brought us safe thus far
And grace will lead us home,
And grace will lead us home

Amazing grace, Howe Sweet the sound
That saved a wretch like me
I once was lost but now am found
T'was blind but now I see
```

## **How it works**
Final Cut Pro supports importing of projects via [XML](https://developer.apple.com/library/archive/documentation/FinalCutProX/Reference/FinalCutProXXMLFormat/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011227-CH1-SW1). This workflow executes a Javascript for Automation script which produces an FCPXML file and then opens the file in Final Cut Pro. The first line of the selected text is used as the title of the file. Each subsequent pair of lines are collected into a single title in Final Cut Pro.

Once the files are installed, feel free to modify them to suit your needs and contribute any upgrades to this repo.

This has been a fun project. I hope it blesses your church.

Ben Frearson
