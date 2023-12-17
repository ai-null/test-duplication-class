issue with chucker

### step to reproduce
- add chucker library to dependencies, sync & run returns success
```gradle
debugImplementation "com.github.chuckerteam.chucker:library:4.0.0"
releaseImplementation "com.github.chuckerteam.chucker:library-no-op:4.0.0"
```
- add midtrans library to dependencies, sync and run returns Duplicate class
```gradle
debugImplementation 'com.midtrans:uikit:2.0.0-SANDBOX'
releaseImplementation 'com.midtrans:uikit:2.0.0'
```
