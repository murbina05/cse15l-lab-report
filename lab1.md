# Hi my name is max and welcom to my first lab report for CSE 15L

In this lab report I will be going over basic some basic terminal actions such as using cd, ls, and cat



**cd**

cd is a powerfull tool and allows you to change the current working directory. This is useful when navigating a codebase or simply being in the right directory inorder to execute code.

When you run cd with not arguments you go to the home directroy
'''
[user@sahara ~/lecture1]$ cd
[user@sahara ~]$ 
'''

When you run cd followed by a directory it changes your current directory. You can tell by the second line where it now includes "~/lecture1" in the path
'''
[user@sahara ~]$ cd lecture1/
[user@sahara ~/lecture1]$ 
'''
When you run cd followed by a path to a file you will get an error. This is becuase you can not have a file as your working directory. Directories are just another name for a folder.
'''
[user@sahara ~]$ cd lecture1/Hello.java
bash: cd: lecture1/Hello.java: Not a directory
[user@sahara ~]$ 
'''
