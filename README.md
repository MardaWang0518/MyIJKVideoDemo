# MyIJKVideoDemo
根据bilibili开源的ijkplayer框架实现的一个视频播放的简单demo

# 运行页面

![](show01.mp4)


## 使用步骤

### 1. 在project的build.gradle添加如下代码(如下图)

	allprojects {
	    repositories {
	        maven { url "https://jitpack.io" }
	    }
	}
  

### 2. 在Module的build.gradle添加依赖

    compile 'com.github.open-android:IjkPlayer:1.0.0'
    

### 3.清单文件添加权限

	<uses-permission android:name="android.permission.INTERNET"></uses-permission>
  
  
### 4.对应xml中要用全局包名

<com.dl7.player.media.IjkPlayerView
        android:id="@+id/player_view"
        android:layout_width="match_parent"
        android:layout_height="300dp" />


### 5.播放视频核心代码

        mUri = Uri.parse("http://covertness.qiniudn" +
                ".com/android_zaixianyingyinbofangqi_test_baseline.mp4");

        mPlayerView.init()
                .setVideoPath(mUri)
                .setMediaQuality(IjkPlayerView.MEDIA_QUALITY_HIGH)
                .enableDanmaku()
                .start();

	
* 整个demo其实很简单，只需要传入对应的视频地址就可以播放,如果你觉得这个库还不错,请star我一下吧~~~，谢谢！


	
