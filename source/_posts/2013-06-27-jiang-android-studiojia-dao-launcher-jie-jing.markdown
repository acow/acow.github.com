---
layout: post
title: "將Android Studio加到Ubuntu的Launcher捷徑"
date: 2013-06-27 17:29
comments: true
categories: 
- Android Studio
- Ubuntu
---

在 /usr/share/applications 中新增檔案：

`$ sudo vim android-studio.desktop`

檔案內容為：

    [Desktop Entry]
    Type=Application
    Terminal=true
    Name=Android Studio
    Icon=/home/acow/android-studio/bin/idea.png
    Exec=/home/acow/android-studio/bin/studio.sh

存檔後，打開此資料夾：

`$ nautilus .`

將 Android Studio 圖示拖拉至 Ubuntu 的 Launcher 即可新增捷徑

* * * 

## 註1：
Terminal 為設定是否開啟 terminal 來列印執行 output，
可設 false 代表背景執行。


## 註2：
由 Laucher 執行的 shell 不會載入 ~/.bashrc 之變數，
因此將變數加在 ~/.profile 檔案尾端：

	# Oracle (Sun) JDK for Android Studio
	export STUDIO_JDK="/usr/lib/jvm/jdk1.7.0_25"
