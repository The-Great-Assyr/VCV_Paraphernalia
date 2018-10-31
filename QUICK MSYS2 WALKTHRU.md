Vcv rack uses c++, so you're going need a c++ compiler. 

I'd suggest using msys2.

Just keep hitting next, and you should see a window with a command prompt open. 

If you don't, go to C:\msys2, and you should see an msys2 application somewhere in there. When you are in the command prompt, type 
```
pacman -Syu. 
```

If prompted to continue, hit y and then hit enter. 

The console will tell you to close it and reopen it. 

Close it, and when you are asked if you want to end the process, hit yes. 

Once you reopen it, type  
```
pacman -Syu  
```

again. Once that finishes, type
```
pacman -S gcc make
```
, and once it's done, close msys2. 

Go to control pannel, and search for "environment variables". 

Click on it, and go to the bottom where it says "edit environment variables". 

In the bottom menu, scroll until you see "PATH". 

Double click on it, and hit "add". Type 
```
C:\msys2\mingw64\bin. 
```
Hit add again, and type 
```
C:\msys2\mingw32\bin. 
```
Now, exit everything, and open the windows command prompt (not msys2). 

Type 
```
gcc
```
and hit enter. 

It should give you an error about not having input files - if it says command not found, you messed up somewhere. 

Now, go into the plugin folder in the command prompt. 

Type 
```
make. 
```
There you go - if you don't get any errors, all of your files should be compiled. 

If you do make dist, you will even get a fancy zip file for your plugin.

Thank you to https://www.reddit.com/user/MazeOfEncryption
