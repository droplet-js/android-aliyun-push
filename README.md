# android-aliyun-push

[![Build Status](https://cloud.drone.io/api/badges/v7lin/android-aliyun-push/status.svg)](https://cloud.drone.io/v7lin/android-aliyun-push)
[![GitHub tag](https://img.shields.io/github/tag/v7lin/android-aliyun-push.svg)](https://bintray.com/v7lin/maven/aliyun-push-android/_latestVersion)
[![API](https://img.shields.io/badge/API-14%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=14)

### snapshot

````
ext {
    latestVersion = '1.0.0-SNAPSHOT'
}

allprojects {
    repositories {
        ...

        // aliyun
        maven {
            url 'http://maven.aliyun.com/nexus/content/repositories/releases/'
        }

        maven {
            url 'https://oss.jfrog.org/artifactory/oss-snapshot-local'
        }
        ...
    }
}
````

### release

````
ext {
    latestVersion = '1.0.0'
}

allprojects {
    repositories {
        ...
        jcenter()

        // aliyun
        maven {
            url 'http://maven.aliyun.com/nexus/content/repositories/releases/'
        }
        ...
    }
}
````

### usage

android
````
...
android {
    ...
    defaultConfig{
        ...
        manifestPlaceholders = [TENCENT_APP_ID: "${appId}"]
        ...
    }
    ...
}
...
dependencies {
    ...
    implementation "io.github.v7lin:aliyun-push-android:${latestVersion}"
    ...
}
...
````
