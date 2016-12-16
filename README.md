#VimForDummies
<h2>A guide for Vim for dummies, made in Vim by a dummie.</h2><br>
<b>Why Vim</b><br>
Why not? Well, actually, there are a lot of reason for Vim and against it, I'll begin with why not. <br>
To be blunt, Vim has too much power for the average user and has a learning curve. Most people can do with your office text editor or note taking software.<br> 
Now the reasons for Vim. In my opinion, it looks cool: Matrix style editing, a dark screen with a bleeping cursor. Second, Vim frees you from the mouse, that friend during intense gaming sessions or infinite scrolling in your favorite social network. Vim is great for the non-average user, and if you found this repo, you are probably not average.
Also, it is in almost every Linux distribution, so editing directly in the server is very easy.<br>
<sub>This guide is based upon https://www.linux.com/learn/vim-101-beginners-guide-vim</sub><br>
<b>Now, down to business</b><br>
First, add vim to your machine<br>
<i>Linux</i> sudo apt-get install vim<br>
<i>Windows</i> ftp://ftp.vim.org/pub/vim/pc/gvim80-069.exe<br>
<b>Firing it up</b><br>
For now, and for learning purposes from now on I will only refer to usage in Linux, so on to business:<br>
On your terminal screen (for the hacker style) you can use $vim [filename] to fire up editing in Vim the file you set as parameter. You will still be in the same screen as Vim is integrated into your terminal. you will hopefully notice that in the bottom there is a counter, this refers to your line number and column number. If you press <b>i</b> you wil enter edit mode, and in the bottom you will see <b>-- INSERT --</b>. That corner indicates your mode. <br>
There are three main modes, Command mode, Insert mode and Last Line mode. As said before, they all work in your keyboard, so navigating between modes happens with keys. <br>
<ul>
<li><i>Command mode</i> lets you, obviously, set commands on the document, but not type. Stuff like navigating, copying, and deleting happen in this mode.</li> 
<li><i>Insert mode</i> is the usual typing mode, with a few quirks.</li>
<li><i>Last Line mode</i> is another command mode, but for document wide actions, and is used by typing.</li></ul>
