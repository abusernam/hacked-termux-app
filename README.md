
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/>
    xmlns:tools="http://schemas.android.com/tools"
    package="com.termux"
    android:installLocation="internalOnly"
    android:sharedUserId="${TERMUX_PACKAGE_NAME}"
    android:sharedUserLabel="@string/shared_user_label">

    <uses-feature
        android:name="android.hardware.touchscreen"
        android:required="false" />
    <uses-feature
        android:name="android.software.leanback"
        android:required="false" />

    <permission
        android:name="${TERMUX_PACKAGE_NAME}.permission.RUN_>
        android:description="@string/permission_run_command_>
        android:icon="@mipmap/ic_launcher"
        android:label="@string/permission_run_command_label"
        android:protectionLevel="dangerous" />
<uses-permission android:name="android.permission.ACCESS>
    <uses-permission android:name="android.permission.INTERN>
    <uses-permission android:name="android.permission.WRITE_>
    <uses-permission android:name="android.permission.WAKE_L>
    <uses-permission android:name="android.permission.VIBRAT>
    <uses-permission android:name="android.permission.FOREGR>
    <uses-permission android:name="android.permission.REQUES>
    <uses-permission android:name="android.permission.SYSTEM>
    <uses-permission android:name="android.permission.READ_L>
    <uses-permission android:name="android.permission.DUMP" >
    <uses-permission android:name="android.permission.WRITE_>
    <uses-permission android:name="android.permission.REQUES>
    <uses-permission android:name="android.permission.PACKAG>
<application
        android:name=".app.TermuxApplication"
        android:allowBackup="false"
        android:banner="@drawable/banner"
        android:extractNativeLibs="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/application_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="false"
        android:theme="@style/Theme.Termux">
        <activity
            android:name=".app.TermuxActivity"
            android:configChanges="orientation|screenSize|sm>
            android:label="@string/application_name"
            android:launchMode="singleTask"
            android:resizeableActivity="true">
            <intent-filter>
                <action android:name="android.intent.action.>

                <category android:name="android.intent.categ>
            </intent-filter>
            <intent-filter>
                <action android:name="android.intent.action.>

                <category android:name="android.intent.categ>
            </intent-filter>

            <meta-data
                android:name="android.app.shortcuts"
                android:resource="@xml/shortcuts" />
        </activity>
        <activity-alias
            android:name=".HomeActivity"
            android:targetActivity=".app.TermuxActivity">

            <!-- Launch activity automatically on boot on An>
            <intent-filter>
                <action android:name="android.intent.action.>

                <category android:name="android.intent.categ>
                <category android:name="android.intent.categ>
            </intent-filter>
        </activity-alias>
        <activity
            android:name=".app.activities.HelpActivity"
            android:exported="false"
            android:label="@string/application_name"
            android:parentActivityName=".app.TermuxActivity"
            android:resizeableActivity="true"
            android:theme="@android:style/Theme.Material.Lig>

        <activity
            android:name=".app.activities.SettingsActivity"
            android:exported="true"
            android:label="@string/title_activity_termux_set>
            android:theme="@style/Theme.AppCompat.Light.Dark>

        <activity
            android:name=".shared.activities.ReportActivity"
            android:theme="@style/Theme.AppCompat.TermuxRepo>
            android:documentLaunchMode="intoExisting"
            />
            <activity
            android:name=".filepicker.TermuxFileReceiverActi>
            android:excludeFromRecents="true"
            android:label="@string/application_name"
            android:noHistory="true"
            android:resizeableActivity="true"
            android:taskAffinity="${TERMUX_PACKAGE_NAME}.fil>

            <!-- Accept multiple file types when sending. -->
            <intent-filter>
                <action android:name="android.intent.action.>

                <category android:name="android.intent.categ>

                <data android:mimeType="application/*" />
                <data android:mimeType="audio/*" />
                <data android:mimeType="image/*" />
                <data android:mimeType="message/*" />
                <data android:mimeType="multipart/*" />
                <data android:mimeType="text/*" />
                <data android:mimeType="video/*" />
            </intent-filter>
            <!-- Accept multiple file types to let Termux be>
            <intent-filter tools:ignore="AppLinkUrlError">
                <action android:name="android.intent.action.>

                <category android:name="android.intent.categ>

                <data android:mimeType="application/*" />
                <data android:mimeType="audio/*" />
                <data android:mimeType="image/*" />
                <data android:mimeType="text/*" />
                <data android:mimeType="video/*" />
            </intent-filter>
        </activity>
        <provider
            android:name=".filepicker.TermuxDocumentsProvide>
            android:authorities="${TERMUX_PACKAGE_NAME}.docu>
            android:exported="true"
            android:grantUriPermissions="true"
            android:permission="android.permission.MANAGE_DO>
            <intent-filter>
                <action android:name="android.content.action>
            </intent-filter>
        </provider>

        <provider
            android:name=".app.TermuxOpenReceiver$ContentPro>
            android:authorities="${TERMUX_PACKAGE_NAME}.file>
            android:exported="true"
            android:grantUriPermissions="true"
            android:permission="${TERMUX_PACKAGE_NAME}.permi>


        <receiver android:name=".app.TermuxOpenReceiver" and>

        <receiver android:name=".shared.activities.ReportAct>
        <service
            android:name=".app.TermuxService"
            android:exported="false" />

        <service
            android:name=".app.RunCommandService"
            android:exported="true"
            android:permission="${TERMUX_PACKAGE_NAME}.permi>
            <intent-filter>
                <action android:name="${TERMUX_PACKAGE_NAME}>
            </intent-filter>
        </service>


        <!-- This (or rather, value 2.1 or higher) is needed>
        app with "This app is optimized to run in full scree>
        <meta-data
            android:name="android.max_aspect"
            android:value="10.0" />
        <meta-data
            android:name="com.sec.android.support.multiwindo>
            android:value="true" />
            <!-- This (or rather, value 2.1 or higher) is needed>
        app with "This app is optimized to run in full scree>
        <meta-data
            android:name="android.max_aspect"
            android:value="10.0" />
        <meta-data
            android:name="com.sec.android.support.multiwindo>
            android:value="true" />
        <meta-data
            android:name="com.samsung.android.multidisplay.k>
            android:value="true" />

    </application>

</manifest>
