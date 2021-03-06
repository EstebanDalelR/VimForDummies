#VimForDummies
<h2>A guide for Vim for dummies, made in Vim by a dummie.</h2><br>
<h2>Part 1</h2>
<sub>This part is based upon https://www.linux.com/learn/vim-101-beginners-guide-vim</sub><br>
<b>Why Vim</b><br>
Why not? Well, actually, there are a lot of reason for Vim and against it, I'll begin with why not. <br>
To be blunt, Vim has too much power for the average user and has a learning curve. Most people can do with your office text editor or note taking software.<br> 
Now the reasons for Vim. In my opinion, it looks cool: Matrix style editing, a dark screen with a bleeping cursor. Second, Vim frees you from the mouse, that friend during intense gaming sessions or infinite scrolling in your favorite social network. Vim is great for the non-average user, and if you found this repo, you are probably not average.
Also, it is in almost every Linux distribution, so editing directly in the server is very easy.<br>

<b>Now, down to business</b><br>
First, add vim to your machine<br>
<i>Linux</i> sudo apt-get install vim<br>
<i>Windows</i> ftp://ftp.vim.org/pub/vim/pc/gvim80-069.exe<br>
<b>Firing it up</b><br>
For now, and for learning purposes from now on I will only refer to usage in Linux, so on to business:<br>
On your terminal screen (for the hacker style) you can use $vim [filename] to fire up editing in Vim the file you set as parameter. You will still be in the same screen as Vim is integrated into your terminal.<br>
<b>Using Vim</b> 
You will hopefully notice that in the bottom there is a counter, this refers to your line number and column number. If you press <b>i</b> you wil enter edit mode, and in the bottom you will see <b>-- INSERT --</b>. That corner indicates your mode. <br>
There are three main modes, Command mode, Insert mode and Last Line mode. As said before, they all work in your keyboard, so navigating between modes happens with keys. <br>
<ul>
<li><i>Command mode</i> lets you, obviously, set commands on the document, but not type. Stuff like navigating, copying, and deleting happen in this mode.</li> 
<li><i>Insert mode</i> is the usual typing mode, with a few quirks.</li>
<li><i>Last Line mode</i> is another command mode, but for document wide actions, and is used by typing.</li></ul>
You may use the Cheatsheet to view all the commands at a glance.<br>
In Command mode you may use h, j, k and l to navigate. The external keys (h and l) are the sides and the internal ones(j and l) navigate up and down. This may be a little awkward and sometimes you may want to navigate entire words, so, for that, use w and e, to jump to the beggining and end of next words, respectively. To go back a word use b (pnemotecnics back is b, forward a word is w), and to move to the end of the line use $. <br>
An interesting feature in vim is the fact that numbers modify behavior. This means that in Command mode you may use 10w to go 10 words forward. <br>
Now, on to editing a file. To copy and paste in Vim you only need a key, not two. In this case, to select some characters you use v and move until you have the right selection (V will select a whole line, ctrl+v will select a column). Now that you have selected some text, use y to "yank" text into your clipboard and p to paste. It's importatn to know that P in capital will replace text, in lowercase will add. <br>
<i>Anytime, press u to undo and ctrl+r to redo.</i><br> 
To search a document, in command mode use /text and then use n and N to move instances of the text forward and backwards, respectively. This search moves forward in the document, of course you may press g to go to the beggining and look, but that may not be the case, so ?text will search backwards. <br>
Replace search requires a little more effort, but allows you to do it for the whole document or get a confirmation on each instance. This is the first time using a full comand. So using :%s/text/replacement/g will search the entire document and replace any instance ot text for replacement, add a c at the end to get confirmation on each replacement.<br>
Now that you have edited your file, is time to exit, but, how? Well, now we make use of Last Line mode. Again, you may use Command mode to save and exit with ZZbut the usual is using :q (in Vim the : character sets the input). To save and exit type :wq. <br>
As a funny quirk of Vim, you are denied exit without editing anything, but you may override it typing :q! in Last Line mode.<br>
<h2>Part 2</h2>
<sub>This part is based upon https://www.linux.com/learn/vim-201-intermediate-guide-vim</sub><br>
<b>Making your life easier</b><br>
Vim is, by default, powerful, so word completion is included out of the box (zip?). For this in Insert mode just press ctrl+p to match any previous text (ctrl+n for text ahead).<br>
When typing strings in a repeated way, Vim helps a lot with abbreviations, so rlw can become ReallyLongWord. To use this in Last Line mode type :ab rlw ReallyLongWord (to delete it :una rlw).<br>
Now, as most modern browsers you will want to open in tabs different files, or the same one to edit different parts. Vim lets you do this and, as always, you can do this without moving your hands from the keyboard. <br>
To edit the same file, go to Last Line mode and use :split. To chage viewport, in Command mode press ctrl+w and you will cycle through. To do the same, but openening another file is :split filename. <br> 
One important thing when splitting is the fact that the files share a buffer so you may yank from one and paste to the other. <br>
To open vim in tabs, rather than viewports (split) use vim -p filename1 filename2 or, if you have Vim open already, use, in Last Line mode :tabnew filename.<br>

<h2>Part 3</h2>
<sub>This part is based upon https://www.linux.com/learn/vim-301-getting-adept-vim</sub><br>
It is time for some really nice features of vim (some more, anyways). Sometimes you may want to hide some lines for any reason. Of course Vim allows you to do so, and it is called "folding". All folding commands are preceded by z and then you will then set options for how to fold. <br>
Vim is nice enough to mark the fold points, and allows you to delete everything that was folded. Check the cheatsheet for all the fold comands.<br>
if you need to go back to the command line (hacker style), just run :sh -- to get another session.<br>

You may want scripts, but for the sake of keeping this dummie guide short I will skip it. If you want this for yourself please search onlie, there are hundreds of resources.<br>
Vim lets you use some commands that will make life easier, like finding uniques and sorting. For this, you may select some lines and use :! sort, or dictate the lines you want to sort, using :l1,l2 ! sort (replace l1 and l2 with the starting and ending line). <br>

Another time saving feature in Vim is conveniently located in the dot (.) key. Pressing this will redo your last operation, so jumping 10 words (10w) and pressing . will jump 10 words each time. <br>

<h2>Part 4</h2>
<sub> This part is base upon https://www.linux.com/learn/vim-401-extending-vim-and-more </sub><br>
 
Now, this section is all about adding features to Vim, making it your own. For more advanced users, you can write scripts, for your weirdest desires, but as Vim is very old and widespread, someone probably started writing the script you need. <br>
First, the difference between a plugin and a script is that a scrip has to be explicitly called. <br>
I shall skip this part.<br>
This is it. Have fun using Vim!<br>

