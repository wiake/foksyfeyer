# foksyfeyer
 Add-on for visually-impaired (and fully blind) Puppy Linux and Ubuntu users. Make X apps speak text too!
 
 EDIT 15 Oct 2013: I've now uploaded some of my old project work including wiak and fokSy Eye R to website page: http://arkitektia.heliohost.org/softwaredesigns.html (currently down sorry)

Current Version: 1.0.0-1

Please uninstall any old version before installing the latest.

The program needs to be setup once the dotpet is installed. To do this, in a console enter the command:

Code:	

foksy setup


[Remember the space between foksy and setup].

You then need to reboot the machine once to have the set up changes take effect.


Please read installREADME.txt in detail before installing.


For Puppy 4.x.x series (and probably most Puppy versions higher than that) read the following post for altered installation instructions:

http://www.murga-linux.com/puppy/viewtopic.php?p=364717#364717



***NOTE WELL: For successful installation it is essential that you do not
miss out any of the following installation steps:

1. Prior to installing this latest fokSyf Eye R system you should
uninstall any previous version.
[***IMPORTANT: NOTE that I accidentally left in /usr/lib/libespeak.a in
an earlier dotpet upload. It is not required.
You SHOULD delete it manually if it remains after this new installation,
since it is from a prior version of espeak.
However, uninstalling the previous version using PETget
probably removes it anyway...]

2. Install the new dotpet in the usual way. Ignore the three or four
warnings concerning missing dependencies. The next steps sorts that out.

3. Once you have installed this new version,
you need to open a console and execute the following to set up foksy:

foksy setup

[***NOTE WELL: the space between foksy and setup]

4. Then you should reboot your system before using foksy for the first time.


Running fokSyf Eye R:

1. After rebooting, you should then open a commandline window such as
an xterm or an rxvt console,
or you can simply press ctrl alt f2 to leave X windows for a virtual terminal.
In the case of the latter,
you will be asked for a login username and password.
By default the username is root, and there is no password,
so in that case simply press enter when asked for the password.
Note that you can return to the X G U I at any time,
from the virtual console, by simply pressing ctrl alt f3.

2. Once you are ready, to start the speech system simply enter the command:

ifoksy

If you wish, you can then start a fokSyf Eye R User Interface menu program,
by entering the command:

foksy

[*NOTE WELL that you can normally only initialise the
speech system once with the command ifoksy.
If you open a different commandline console later,
and want speech activated in that too,
you will need to enter the command yasr in that new console
before running foksy in there.
However, should speech fail to initialise at any stage,
simply enter the command, foksy --kill, and then you can try ifoksy again].

A help system is provided in foksy.

You can also use one of foksy's options.
For a list of foksy's options enter: foksy -? or foksy --help

Should speech fail to initialise at any stage,
simply enter the command, foksy --kill, and then try ifoksy again.


-----

The fokSyf Eye R, Screen Environment Reader: foxyf eye r mainfeatures.txt
Author: mcewanw Dated: 2008Mar06


Some Details on the Contents of foksyf eye r CORE-x.x.x

1. The main speech interface comprises three separate applications:

Yasr, speech-dispatcher and espeak.

Yasr does the job of reading whatever data is output by the user
programs being run (e.g. edbrowse), and sending that data via a
speech system management programme called "speech-dispatcher" to the
software synthesiser "espeak" that does the actual "speaking". In
practice, speech-dispatcher allows the speech synthesiser to be
replaced by alternative software or hardware synthesisers and/or
braille capable interfaces (using, for example, the program Brltty).
I haven't yet provided a dotpet for Brltty, since I don't have any
hardware to test it on; however, it is easy enough to compile and it
is likely to be included shortly in foksyf eye r CORE.


The currently provided user applications currently include:

2. Edbrowse

This program is created by Karl Dahlke, who is himself blind from a
very early age. Karl has consequently written edbrowse in such a way
that it is specially tailored for the needs of the visually impaired.
It combines the functions of a text editor, web browser (with secure
certificates ssl support and limited javascript), email (both smtp
send and pop3 receive), ftp, and file management. Edbrowse has a
steep learning curve, but it a great program to use once you have
mastered it. Note that, whilst browsing, edbrowse (version >= 3.3.3)
is now able to read and view many pdf files directly by automatically
converting them to html with the installed pdftohtml converter
utility.

2. Lynx.

This is a more conventional, albeit limited, screen-oriented web
browser. It also includes ssl support, but no javascript. Lynx is
easy to learn though, and it is well-known and respected in the
visually impaired community. Some users may prefer this to edbrowse,
despite its limitations.

3. The vi text editor

This is the classic ex/vi text editor. Unlike edbrowse, which is a
single-line oriented editor partly based on the classic UNIX text
editor ed, vi is a very powerful full-screen editor. However, its
"mode-oriented" nature, makes it difficult for some users to learn.
Nevertheless, there are many good reasons to learn the use of vi: not
only is it available by default on most UNIX/Linux systems, and
extremely flexible, many other applications can also be configured to
use vi keybindings.

4. The sc spreadsheet

This text-console spreadsheet uses vi keybindings for many of its
tasks. Though it is screen-based, the method it uses to write data to
the screen appears to be reasonably compatible with the "speaking
interface" provided by yasr, speech-dispatcher and espeak. It uses
much the same syntax as Excel for its functions, and appears to be
quite fully functioned.

5. krecspk

Krecspk is a hotkey-driven, console-oriented, audio recording program
for producing audio clips or podcasts in a variety of audio formats
such as Ogg Vorbis, mp3, and wav. It relies on the underlying "sox"
commandline utility for its audio recording and playback
functionality. Krecspk has also been specially written with the
visually impaired in mind, and to make it work seamlessly with the
yasr/speech-dispatcher/espeak combination. A "speaking" GUI frontend
for krecspk (called wrecspk) is also available.

6. foksy

This is a simple console-oriented menu system, which can be used to
provide convenient access to the foksyf eye r applications and help files. It
is not particularly sophisticated in its present form, but is
nevertheless quite functional. It also provides a simple help system,
allowing the user immediate access, both spoken and in text form, to
all the help files, tutorials, and readme files associated with the
above applications.

7. Commandline file converter utilities

These include

catdoc, for converting Microsoft doc and rtf files to txt format;
rtf2html, for converting Rich Text Format files to html format;
xls3csv, for converting Excel (TM) spreadsheets to csv format;
catppt, for extracting data from MS-Powerpoints;
pdftohtml, for converting Adobe pdf files to html format;
pdftotxt, for converting Adobe pdf files to txt format.

8. xsel

This utility allows foksy to almost seamlessly paste from text
highlighted selections in X, and from the X clipboard. fokSyf Eye R can thus
provide a truly hybrid screen reader experience when used alongside
X applications such as Opera, Seamonkey or Firefox, and X screen magnifiers.

Summary:

One of the major advantages of the fokSyfy Eye R, Screen Environment Reader
is that it is easy to install on various Linux distributions. For
example, it has been tested as working well on Puppy Linux
2.14R, 2.15.1, 3.01and 4.3.1 distributions. It is also extremely resource
efficient and small, being only a few Mbytes in download size.

Once foksyf eye r CORE has been installed, the system is immediately
available from any commandline window on execution of the startup
command: initsp

The user can then either simply use applications directly from the
commandline, or start up the menu/help system environment by
executing: menusp

[Note that the help system files are far from perfect in their
current form, since much of their content is simply rehashed forum
posts].

In summary, I wish to state my appreciation of the help I have been
receiving from Karl Dahlke, with regard to edbrowse usage and
functionality. Karl is in regular email touch with me and has gone
out of his way to patch edbrowse in such a way that it is more
functional for the Puppy Linux community in general. 
