
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
