# Reset AndroidStudio in MacOs 
Sometime AndroidStudio have issues by unknown reason. Finally way to troubleshoot the problem is clearing cache in AndroidStudio.  
You need remove all the directories that are related to AndroidStudio:  
~/Library/Application Support/AndroidStudio*  
~/Library/Caches/AndroidStudio*  
~/Library/Logs/AndroidStudio*  
~/Library/Preferences/AndroidStudio*  

# Java Env
```
# Install via `brew`
  $ brew install openjdk
# Or
  $ brew upgrade openjdk
```
For the system Java wrappers to find this JDK, symlink it with
```
  sudo ln -sfn /opt/homebrew/opt/openjdk/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk.jdk
```
If you need to have openjdk first in your PATH, run:
```
  echo 'export PATH="/opt/homebrew/opt/openjdk/bin:$PATH"' >> ~/.zshrc
```
Check version and replace the version into source file (.zshrc) at `JAVA_HOME`
```
  /usr/libexec/java_home -V
```

.zshrc
```
  export ANDROID_HOME=/Users/lamhoangx/Library/Android/sdk
  export PATH=$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools
  export PATH=$PATH:/opt/homebrew/bin
  
  export JAVA_HOME=`/usr/libexec/java_home -v 20.0.1`
  export PATH="/opt/homebrew/opt/openjdk/bin:$PATH"
```

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
