# Hi my name is Max and welcome to my first lab report for CSE 15L

In this lab report I will be going over basic some basic terminal actions such as using cd, ls, and cat



## cd

cd is a powerfull tool and allows you to change the current working directory. This is useful when navigating a codebase or simply being in the right directory inorder to execute code.

When you run cd with not arguments you go to the home directroy. In the example bellow you are start in the /home/lecture1/ directory, however after you run the command you end up in the home directory. You can tell this because it just says ~ which means home. The following example will not cause an error.


```
[user@sahara ~/lecture1]$ cd
[user@sahara ~]$ 
```

When you run cd followed by a directory it changes your current directory. You can tell by the second line where it now includes "~/lecture1" in the path. The working directory at the start is home, however after the command you change your working directory to ~/lecture1/. This example bellow will not cause an error.

```
[user@sahara ~]$ cd lecture1/
[user@sahara ~/lecture1]$ 
```
When you run cd followed by a path to a file you will get an error. This is becuase you can not have a file as your working directory. Directories are just another name for a folder. At the start your working directory is ~ which is home. When your run the commmand with the example bellow you will get an error and your working directory will not change. 

```
[user@sahara ~]$ cd lecture1/Hello.java
bash: cd: lecture1/Hello.java: Not a directory
[user@sahara ~]$ 
```

## ls

ls is another tool that is crucal when using a terminal. ls tells you all the files and directories that are in your current working directory. I know a little confusing, but in a second you will see what I mean.

When you run ls with no argument it prints out everything* within that directory. Here you can see that we only have a directory named lecture1. During this example your working directory will remain your home directory, you can tell becuase you see ~ followed by nothing. The exmaple bellow will not cause an error.
```
[user@sahara ~]$ ls
lecture1
```

However now when we pass the directory we found above you see we get a lot more information. Here we specify where is the information that we want to see. We can see that some of the files have a ".something". This is becusae they are files with a specific extension like png or jpg jsut here they are for java files. In the example bellow your working directory remain ~ which is home. The command bellow will not cause an error.  

```
[user@sahara ~]$ ls lecture1/
Hello.class  Hello.java  messages  README
```

This is one of the use cases that is not that, well useful. When you use ls on a file it returns the path to that file here we are calling it from the home directory and it tells us to look in the lecture1 folder and in there you will find Hello.java. The working directory of the example bellow will remain you home directory and you will not get an error if you run the example bellow. 
```
[user@sahara ~]$ ls lecture1/Hello.java
lecture1/Hello.java
```

## cat

Lastly we have cat. Cat is short for concatinate, however this tool although is not used as much as the previous two it has a lot of uses that unfortanatly we do not cover here. However a general premise is it works with text.

When you use cat by itself it opens a sort of terminal where it will return everything you type. Something important to keep in mind is if you want to exit this you use the commant ctrl c. The working directory is your home directory and if you run the exmaple bellow you will not get an error.

```

[user@sahara ~]$ cat
hello world
hello world
```

Next when you run the cat command on a directory you get the following prompt:

```
[user@sahara ~]$ cat lecture1/
cat: lecture1/: Is a directory
```

This happens becuase you can't concatinate a directory. Directories are more like a road that leads you to building. They do not themselves hold the critical information but they lead to where it is. Your working directory during the example above is your home directory and you will get an error if your run the example above. This happens becuase you can't use cat on directories. 

Lastly we have when you use a file as an argument. When you do this it will print out all the contents of that file. This can be useful when youa re de-bugging or whenever you are just curious what that file contains. The working directory in the example bellow is ~/lecture1 and you will not get an error if you run the example bellow.

```
[user@sahara ~/lecture1]$ cat Hello.java
import java.io.IOException;
import java.nio.charset.StandardCharsets;
import java.nio.file.Files;
import java.nio.file.Path;

public class Hello {
  public static void main(String[] args) throws IOException {
    String content = Files.readString(Path.of(args[0]), Standar
dCharsets.UTF_8);    
    System.out.println(content);
  }
```
