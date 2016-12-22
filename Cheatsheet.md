<h1> CHEATSHEET </h1><br>
<sub>Notice that uppercase and lowercase letters mean different behaviors</sub>
<h3><i> Command mode</i></h3><br>
<b>Navigation</b><br>
<ul>
<li> h: left 1 column </li>
<li> j: down 1 row </li>
<li> k: up 1 row </li>
<li> l: right 1 column</li>
<li> o: beggining of line </li>
<li> $: end of line </li>
<li> w: forward one word (beggining)</li>
<li> e: forward one word (end)</li>
<li> G: end of file (last line)</li>
<li> gg: beggining of file </li>
<li> ZZ: save and quit </li>
</ul><br>

<b>Editing</b><br>
Notice that deleting combines de delete operation and movement<br>
<ul>

<li> v: starts the selection operation</li>
<li> V: selects the current line </li>
<li> vg: selects to the beggining of file </li>
<li> d: starts the delete operation </li>
<li> dw: delete a word </li>
<li> do: delete to the beggining of the line  </li>
<li> d$: delete to the end of the line</li>
<li> dgg: delete to the beggining of the file</li>
<li> dG: delete to the end of the file</li>
<li> x: delete the current character  </li>
<li> p: paste text in the buffer</li>
<li> P: paste (replace) </li>
<li> y: yank text to buffer </li>
</ul><br>


<b>Searching and Replacing</b><br>
<ul>
<li> /text: search text forward</li>
<li> n: go to the next instanceof the search </li>
<li> N: go to the previous instance of the search </li>
<li> ?text: search text backwards </li>
<li> :%s/text/replacement/g: replace in the entire document </li>
</ul><br>

<b>Saving Keystrokes</b>
<ul>
<li> Ctrl+p: complete with previous words</li>
<li> Ctrl+n: complete with next words</li>
<li> :ab wtc WordToComplete: create abbreviation on wtc to replace with WordToComplete</li>
<li> :una wtc: delete abbreviation on wtc </li>
	 
