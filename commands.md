create new file in CWD

copy con myfile.txt <press enter>
can add lines of text manually, but is difficult to make complex entries
press and hold Ctrl, press Z, and then let go of both keys. Once ^Z is shown on the screen press Enter to save the file and exit.

starts program to edit file in CWD

start notepad myfile.txt <press enter>

References: https://www.computerhope.com/issues/ch000398.htm




Cheat sheet of basic windows command line commands

Basic Command Prompt Commands
x /? = provides syntax info and complete list of all parameters for x (a command, like “cd”)
cd = change directory
cd .. = move to the parent directory
cd\ = move to the root of current drive
cd x = move to the current\x directory
cd z: = change to the z root directory (as opposed to c:)
copy x y = copy file x to directory y (Ex: D:\games\galaga.exe C:\programs[\awesome.exe]), [] = optional
copy file con = display file contents in console
copy con file.txt = create text file in the console window, end with ctrl+z (^z or F6)
date = change the date
del = delete/erase
del x = deletes all files/folders fitting x
del . = deletes all files within current directory
del *.* = deletes all files within current directory
dir = display contents of current directory (Ex: dir [c:][\programs]), [] = optional
dir *.txt = list all .txt files in current directory
dir *.? = list all files with extensions one character in length in current directory
dir /w /p *.* = display all contents one screen at a time
dir | more = display all contents one line at a time
dir /? = provides syntax info and complete list of all dir parameters
echo = send command line input to display (by default)
echo sometext » somefile.txt = append line(s) of text to any file
echo sometext > somefile.txt = overwrites file with sometext
erase = delete/erase
exit = exit the command prompt
filename.txt = opens filename.txt in current directory in Notepad (or default .txt program)
format z: = format z drive [Ex: use to format a disc or flash drive]
mkdir x = make directory x in current directory
move x y = more or rename x to y
q = escapes sequential display of contents (i.e. the more parameter)
rd x = remove/delete directory x if it’s empty
ren x y = rename file x to y
time = change the time
type file = display the contents of the file ‘file’ (displays file contents in console)
type file |more = display the contents one line at a time

Advanced Command Prompt Commands
ipconfig [/all] = display network adapter information (advanced)
netstat –n = display local address and addresses you are connected to (advanced)
netstat –nb = above with name of foreign addresses (advanced) (this shows your private IP, if you are behind a router or proxy, then your public IP address will be different)
ping google.com = how long it takes for your computer to talk to google.com
**

Convert output of one process into the input of another process
Send contents of script.js to the system debug.exe file:
type script.js | c:\programs]debug.exe
programs\debug.exe < script.js

Send directory listing to a printer or file
dir > prn (theoretically to a printer)
dir > somefile.txt
dir *.mp3 > c:\Users\Dan\Desktop\musiclist.txt = print all .mp3 files in current directory to musiclist.txt

Customize the DOS command prompt
prompt /? = display prompt options
prompt $p$g = display current directory followed by a greater-than symbol (Windows default)
prompt $p$g$t = display time after the default prompt
prompt [%computername%][%username%] $g = display computer name followed by username
prompt = reset prompt to default

color 0a = change prompt color to matrix green and screen color to black
color 84 = change colors to red on grey
0 = black
1 = blue
2 = green
3 = cyan
4 = red
5 = magenta
6 = yellow
7 = white
8 = grey
9 = bright blue
a = bright green
b = bright cyan
c = bright red
d = bright magenta
e = bright yellow
f = bright white

Modify any file extension associations
[assoc .extension=fileType]
assoc /? = prints this information
assoc = display list of current file extensions recognized by your computer (any fileType value may be used)
assoc > fileextensions.txt = print list to somefile.txt in current directory
assoc .txt = displays current file association of .txt (.docx, .html, .zip, .htaccess, assoc textfile, et cetera)
assoc .txt= = will delete the association for the given file extension

File Extension Tips/Ideas:
- Windows by default doesn’t know the following extensions, but check anyways with “assoc .”, “assoc .htaccess” and “assoc .xml” anyways just to be sure. If the extension is defined already, then you may not need to change it.
assoc .=txtfile = associate extensionless files with Notepad
assoc .htaccess=txtfile = associate nameless .htaccess files with Notepad
assoc .xml=txtfile = associate XML files with Notepad

Miscellaneous
Acceptable characters: A-Z a-z 0-9 $ # & @ ! ( ) – { } ‘ ` _ ~
Unacceptable characters: | < > \ ^ + = ? / [ ] ” ; , * : %

? = wildcard for any single character
* = wildcard for any/all characters/files
> = redirects output to (overwrite) a file or device
» = redirects output to (append to) a file or device
< = directs data from a file or device to a program or device
« = directs additional data from a file or device to a program or device
nul = black hole

Environmental Variables via the DOS command prompt

System-generated upon Windows startup:
%DATE% = Tue 08/02/2011
%TIME% = 14:23:33.37
%SYSTEMROOT% = C:\Windows
%COMPUTERNAME% = DAN-PC
System-generated upon user login:
%USERNAME% = Dan
%USERDOMAIN% = Dan-PC
Local machine variables for all users:
%PATH% = C:\Windows\system32
%HOMEPATH% = \Users\Dan
%HOMEDRIVE% = C:
(Hint: Use echo)
Function Keys

F1 = Sequential, individual repeat of previously entered characters
F2 = Copies any number of characters from the previous command line
F3 = Repeats the contents of the previous command line
F4 = Deletes any number of characters from the previous command line
F5 = Return to the previous command line
F6 = Enters the characters ^z (CTRL+z), indicating “end of file”
F7 = Displays a history of command-line entries for the current session (50-line cache)
F8 = Sequentially displays previous command-line entries
F9 = Enables user to recall previous command lines by number (0 = first line)

direct download from known url

curl -LOk <url>