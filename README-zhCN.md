# libpng-android-prefab [![](https://jitpack.io/v/LimeVista/libpng-android-prefab.svg)](https://jitpack.io/#LimeVista/libpng-android-prefab)

[English](README.md) | [简体中文](README-zhCN.md)

用于 Android 的 `libpng` 静态库。

## 库上游
[libpng](http://www.libpng.org/pub/png/libpng.html)

## 要求
* Android SDK 21+
* Android Studio 4.1.+

## 应用

* 添加源
```groovy
allprojects {
  repositories {
    // ...
    maven { url 'https://jitpack.io' }
  }
}
```

* 添加依赖
```groovy
dependencies {
    // ...
    implementation "com.github.LimeVista:libpng-android-prefab:${ver}"
}
```

* 启用 `prefab`（预制模式）
```groovy
android {
    // ...
    buildFeatures {
        prefab true
    }
}
```
* 修改 `CMakeLists.txt`
```cmake
# ...

find_package(libpng REQUIRED CONFIG)

# ...

target_link_libraries(your-lib
        libpng::png_static
        ${ZLIB_LIBRARY}
        # ...
        )
```