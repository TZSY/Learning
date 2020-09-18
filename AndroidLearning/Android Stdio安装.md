## grade下载

需要手动下载

放到地址

C:\Users\tzsy\.gradle\wrapper\dists中

##  编译报错

原因是需要翻墙。

改一下的buil.gradle

```java
buildscript {
    
    repositories {
        maven{ url = "http://maven.aliyun.com/nexus/content/groups/public/" }
        google()
        jcenter()
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:3.1.2'
        

        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
    }
}

allprojects {
    repositories {
        maven{ url = "http://maven.aliyun.com/nexus/content/groups/public/" }
        google()
        jcenter()
    }
}
```

## 针对AMDCPU的配置

https://blog.csdn.net/a497785609/article/details/103832368



