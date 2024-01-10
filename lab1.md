# Hi my name is max and welcom to my first lab report for CSE 15L

In this lab report I will be going over basic some basic terminal actions such as using cd, ls, and cat



## cd

cd is a powerfull tool and allows you to change the current working directory. This is useful when navigating a codebase or simply being in the right directory inorder to execute code.

When you run cd with not arguments you go to the home directroy


```
[user@sahara ~/lecture1]$ cd
[user@sahara ~]$ 
```

When you run cd followed by a directory it changes your current directory. You can tell by the second line where it now includes "~/lecture1" in the path

```
[user@sahara ~]$ cd lecture1/
[user@sahara ~/lecture1]$ 
```
When you run cd followed by a path to a file you will get an error. This is becuase you can not have a file as your working directory. Directories are just another name for a folder.

```
[user@sahara ~]$ cd lecture1/Hello.java
bash: cd: lecture1/Hello.java: Not a directory
[user@sahara ~]$ 
```

## ls

ls is another tool that is crucal when using a terminal. ls tells you all the files and directories that are in your current working directory. I know a little confusing, but in a second you will see what I mean.

When you run ls with no argument it prints out everything* within that directory. Here you can see that we only have a directory named lecture1.
```
[user@sahara ~]$ ls
lecture1
```

However now when we pass the directory we found above you see we get a lot more information. Here we specify where is the information that we want to see. We can see that some of the files have a ".something". This is becusae they are files with a specific extension like png or jpg jsut here they are for java files. 

```
[user@sahara ~]$ ls lecture1/
Hello.class  Hello.java  messages  README
```

This is one of the use cases that is not that, well useful. When you use ls on a file it returns the path to that file here we are calling it from teh home directory and it tells us to look in the lecture1 folder and in there you will find Hello.java

```
[user@sahara ~]$ ls lecture1/Hello.java
lecture1/Hello.java
```
