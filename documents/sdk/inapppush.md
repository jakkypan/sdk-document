##游戏内公告接入SDK

历史版本号: 1.0 

###激活插件SDK下载链接：

- [Download InAppPush V1.0 SDK](http://222.73.243.55:3000/downloadsdk/inapppush.zip)

------------------------------------------------------------------------------

1. 在AndroidManifest中添加如下权限：

		<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
	    <uses-permission android:name="android.permission.ACCESS_WIFI_STATE" />
	    <uses-permission android:name="android.permission.CHANGE_NETWORK_STATE" />
	    <uses-permission android:name="android.permission.CHANGE_WIFI_STATE" />

2. 请将SDK中的assets目录下的文件拷贝到工程目录下
 
3. 在Application节点中添加如下activity：

		<activity android:name="com.mztgame.inapppush.view.ZTGiantInAppPushView"
            android:configChanges="orientation|screenSize|keyboardHidden"
                android:windowSoftInputMode="adjustResize"
                android:theme="@android:style/Theme.Translucent.NoTitleBar"
                android:screenOrientation="landscape">
        </activity>
        
4. 在需要显示游戏公告的地方输入如下代码：

		ZTGaintInAppPush.getInstance().init(MainActivity.this, "5000", "20");
		
	- 函数原型 
	
	
			public final ZTGaintInAppPush init(Activity ctx, String gameid, String channelId) 
			
			
			
`ctx`:为游戏需要显示公告的Activity  
`gameid`:为游戏的gameid，从巨人平台获取。  
`channelId`:为巨人sdk的渠道编号。