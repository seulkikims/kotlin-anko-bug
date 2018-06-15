# kotlin-anko-bug

### Description
Anko extension onClick crashes app after upgrading kotlin from 1.2.41 to 1.2.50

### Dependencies
- kotlin 1.2.50
- anko 0.10.5

### Android env
- minifyEnabled true
- proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'

### Steps to reproduce
- Run 'bad' app
- Click on 'click me' button
- App crashes

```
E/AndroidRuntime: FATAL EXCEPTION: main
                  Process: com.jetbrain.kotlin.anko.bug, PID: 8335
                  java.lang.IllegalAccessError: Final field 'a.a.a.a.b.a' cannot be written to by method 'void a.a.a.a.c.<clinit>()' (declaration of 'a.a.a.a.c' appears in /data/app/com.jetbrain.kotlin.anko.bug-2/base.apk)
                      at a.a.a.a.c.<clinit>(Unknown Source)
                      at a.a.a.a.c.a(Unknown Source)
                      at org.a.a.a.a.a$a$1.a(Unknown Source)
                      at a.a.a.b.a.a.a(Unknown Source)
                      at b.a.a.k$a.run(Unknown Source)
                      at android.os.Handler.handleCallback(Handler.java:751)
                      at android.os.Handler.dispatchMessage(Handler.java:95)
                      at android.os.Looper.loop(Looper.java:154)
                      at android.app.ActivityThread.main(ActivityThread.java:6682)
                      at java.lang.reflect.Method.invoke(Native Method)
                      at com.android.internal.os.ZygoteInit$MethodAndArgsCaller.run(ZygoteInit.java:1520)
                      at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:1410)
```
