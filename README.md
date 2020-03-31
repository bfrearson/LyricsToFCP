# LyricsToFTP
Automator script in JXA to add lyrics to a Final Cut Pro X Library.

## **Introduction**
This installer will install a service that can run on any text selection and generate a series of 5s titles in Final Cut Pro for every pair of lines of text.


## **Installation**
For clarity, this will install the following files:

~/Library/Application Support/LyricsToFCP/FCPLyricsBlank.fcpxml <-- template file that the script modifies

~/Library/Services/Send Lyrics to Final Cut Pro.workflow <--Automator workflow containing Javascript for Automation script

~/Movies/Motion Templates/Titles/Lyrics/2 Lines <--Final Cut Pro Title used in script.


## **Usage**
With any text selected, right click -> Services -> Send Lyrics to Final Cut Pro.

Note: The first line of text will be used as the title and will not appear in the timeline in Final Cut Pro.

A double line break will indicate the start of a new section and prevent the last line of a verse running into a chorus.


### **Sample Lyrics**

>Amazing grace

>Amazing Grace, How sweet the sound
That saved a wretch like me
I once was lost, but now am found
T'was blind but now I see

>T'was Grace that taught my heart to fear
And Grace, my fears relieved
How precious did that grace appear
The hour I first believed

>Through many dangers, toils and snares
We have already come.
T'was grace that brought us safe thus far
And grace will lead us home,
And grace will lead us home

>Amazing grace, Howe Sweet the sound
That saved a wretch like me
I once was lost but now am found
T'was blind but now I see
