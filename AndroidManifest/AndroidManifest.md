## AndroidManifest ##

### 应用程序的配置文件 可以定义组件.权限.版本等... ###

	<manifest xmlns:android="http://schemas.android.com/apk/res/android"
		package="com.vagrancys.android">
		<application android:label="@string/app_name"
					 android:icon="@drawable/ic_lacuncher_android">
			<activity 
				android:name=".MainActivity"
				android:label="@string/app_name">
				<intent-filter>
					<action android:name="android.intent.action.MAIN"/>
					<category android:name="android.intent.category.LAUNCHER"/>
				<intent-filter/>
			</activity>
		</application>
	</manifest>