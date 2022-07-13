# libpng-android-prefab [![](https://jitpack.io/v/LimeVista/libpng-android-prefab.svg)](https://jitpack.io/#LimeVista/libpng-android-prefab)
 
[English](README.md) | [简体中文](README-zhCN.md)

The `libpng` static library for Android.  

## Upstream
[libpng](http://www.libpng.org/pub/png/libpng.html)

## Environment
* Android SDK 19+
* Android Studio 4.1.+

## Usage

* Add repositorie.
```groovy
allprojects {
  repositories {
    // ...
    maven { url 'https://jitpack.io' }
  }
}
```

* Add dependencie.
```groovy
dependencies {
    // ...
    implementation "com.github.LimeVista:libpng-android-prefab:${ver}"
}
```

* Enable prefab
```groovy
android {
    // ...
    buildFeatures {
        prefab true
    }
}
```
* Change `CMakeLists.txt`
```cmake
# ...

find_package(libpng REQUIRED CONFIG)

# ...

target_link_libraries(your-lib
        libpng::png_static
        ${ZLIB_LIBRARY}
        z
        # ...
        )
```
