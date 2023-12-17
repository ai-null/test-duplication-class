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

### error log
````
Duplicate class com.chuckerteam.chucker.api.Chucker found in modules library-4.0.0-runtime (com.github.chuckerteam.chucker:library:4.0.0) and library-no-op-3.5.2-runtime (com.github.chuckerteam.chucker:library-no-op:3.5.2)
Duplicate class com.chuckerteam.chucker.api.ChuckerCollector found in modules library-4.0.0-runtime (com.github.chuckerteam.chucker:library:4.0.0) and library-no-op-3.5.2-runtime (com.github.chuckerteam.chucker:library-no-op:3.5.2)
Duplicate class com.chuckerteam.chucker.api.ChuckerInterceptor found in modules library-4.0.0-runtime (com.github.chuckerteam.chucker:library:4.0.0) and library-no-op-3.5.2-runtime (com.github.chuckerteam.chucker:library-no-op:3.5.2)
Duplicate class com.chuckerteam.chucker.api.ChuckerInterceptor$Builder found in modules library-4.0.0-runtime (com.github.chuckerteam.chucker:library:4.0.0) and library-no-op-3.5.2-runtime (com.github.chuckerteam.chucker:library-no-op:3.5.2)
Duplicate class com.chuckerteam.chucker.api.RetentionManager found in modules library-4.0.0-runtime (com.github.chuckerteam.chucker:library:4.0.0) and library-no-op-3.5.2-runtime (com.github.chuckerteam.chucker:library-no-op:3.5.2)
Duplicate class com.chuckerteam.chucker.api.RetentionManager$Period found in modules library-4.0.0-runtime (com.github.chuckerteam.chucker:library:4.0.0) and library-no-op-3.5.2-runtime (com.github.chuckerteam.chucker:library-no-op:3.5.2)

Go to the documentation to learn how to Fix dependency resolution errors.
````
