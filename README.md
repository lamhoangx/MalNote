# Reset AndroidStudio in MacOs 
Sometime AndroidStudio have issues by unknown reason. Finally way to troubleshoot the problem is clearing cache in AndroidStudio.  
You need remove all the directories that are related to AndroidStudio:  
~/Library/Application Support/AndroidStudio*  
~/Library/Caches/AndroidStudio*  
~/Library/Logs/AndroidStudio*  
~/Library/Preferences/AndroidStudio*  



## Reset git to initial
```
git update-ref -d HEAD
```
Hope doing well...
