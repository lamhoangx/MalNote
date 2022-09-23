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

## Install Bundle build (.abb)
```
brew install bundletool
bundletool build-apks --bundle=app-release.aab --output=app-release.apks
bundletool install-apks --apks=app-release.apks
```
Hope doing well...
