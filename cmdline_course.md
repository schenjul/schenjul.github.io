---
layout: default
---

## Introduction to Command Line for Linguists
<img src="assets/images/pic1.png" alt="Photo" hspace="20" width="100%" align="middle"/>

In the course 'Command Line for Linguists' we learned how to use process corpra using the UNIX command line, how to install and run useful application in UNIX and finally how to build our own web page.     

At the end of this course we should know:
1. how to navigate in the Command Line Environment
2. how to open and edit a file using a text editor
3. how to run programs in the background and how to kill them
4. how to transform text files
5. how to generate a frequency list from a text file
6. how to tramsfrom a text file into a lost of word n-grams
7. how to write simple scripts
8. how to install and running programs using sudo
9. how to set up a repository in Github
10. how to create your own web page

## Content of the single weeks

### Week 1 -- Introduction to the Command Line Environments   
In the first week of the command-line course we installed the command-line environment on our personal computer and learned the first commands:

Example:        
<pre><code>
   mv file1 file2   
      output: file2
           
   mv file2 data/    
      output: move file2 to directory 'data/'    

   emacs file2    
      output: file2 can be edited with emacs     

   less file2
      output: displayed content of file2
</code></pre>

### Week 2 -- Navigating a UNIX System
In the second week we learned more about navigatin a UNIX system. We repeat the commands of the first week and learned new commands for editing permission rights and how to pause processes and how to kill them.

Example:     
<pre><code>
   chmod a+r text.txt      
      output: a selects all users; r selcts the reading rights, + grants selected rights to
      	 	 selected users. Write and execute permissions are not affected.      

   sleep 1000     
      output: paused the programm for 1000 seconds
</code></pre>

### Week 3 -- Basic Corpus Processing
In the third week we learned about different character encodings and how to convert between different character encodings. Also, we learned about commands for processing and searching in text files. These commands help us to find relevant information in given text files without reading the whole file.

Example:
<pre><code>
   tail -n +1000 book.txt      
      output: skip the first 999 lines and print the remaining lines      

   dos2unix book.txt        
      output: convert a Windows text file into a UNIX text file      

   egrep "^.{4}ss[aä]$" book.word_list.txt | wc -l       
      output: counts all words which have exactly 7 characters and ending in "ssa" or "ssä".     
</code></pre>      

### Week 4 -- Advanced Corpus Processing
In week four we deepened the contents of week three and combined simple commands to complex commands. As second part of this week we learned to use the sed command which helps to transform text files.

Example:
<pre><code>
    cat text.txt | tr -s '\n\t\r ' '\n' | tr -dc "A-Za-z0-9'\n" | tr 'A-Z' 'a-z' | sort | uniq -c | sort -nr > text.freq     
      output: creating a frequency list. Translate all uppercase letters into lowercase letters.     

    sed s/and/AND/g text.txt       
      output: every occurence of 'and' will be replaced with 'AND'     
</code></pre>
    
### Week 5 -- Scripting and Configuration Files
In week five we learned how to put commands in tidy "scripts". So we have not to typ every single command one by one.

Example:     
<pre><code>
   List='ls$1'      
   for ITEM in $LIST      
   do      
	echo $ITEM      
   done      
      output: it takes a directory name as input, loops it through all files and directories in the that directory and prints their names in a list.      
</code></pre>

### Week 6 -- Installing and Running Programs
In the first part of the sixt week we learned about installing programs. Therefore, we learned to give commands as the root user by using sudo. In the second part we looked at the command make which is used for building other programs, libaries or other projects.     

Example:
<pre><code>
   sudo apt-get install meld     
      output: with the help of sudo we install the program meld      
</code></pre>
   
### Week 7 -- Version Control 
In the last week we looked at version control. This is an integral part of developing projects. We installed Git in our system and create a repository in Github. We learned how to work in the repository on our local computer and add it to the global repository on Github.

Example:     
<pre><code>
   git add -A      
      output: add all files (new, chnaged, deleted files)      
   git pull origin master     
   git push origin master      
      output: upload to global repository on Github
</code></pre>

           
### Emacs Commands List

| Command  | Explanation			 |
| ---------|:-----------------------------------:|
| C-x C-s  | save the file			 |
| C-x C-w  | write the text to an alternate name |
| C-s      | search forward    	  	    	 |
| C-r      | search backward			 |
| C-f      | forward char 			 |
| C-a	   | beginning of line 			 |
| C -p	   | previous line     			 |
| C -n	   | next line 				 |
| C -e	   | end of line 			 |
| C -v	   | one page up 			 |
| M-v	   | scroll down one page 		 |
| M-<	   | beginning of text 			 |
| M->	   | end of text  			 |