1) **(add-line)** ***Route:** /manifests/AndroidManifest.xml/* ---  **INTERNET PERMISSIONS**
```xml
<uses-permission android:name="android.permission.INTERNET" />
```
2) **(add-line)** ***Route:** Gradle Scripts/build.gradle(Module: app)* ---  **NETWORKING LIBRARY**
```kotlin
dependencies {
  ...
  implementation 'com.amitshekhar.android:android-networking:1.0.2'
  ...
}
```
3) **(add-block)** ***Route:** /res/values/colors.xml* ---  **COLOR PALLETE**
```xml
<resources>
  <color name="colorPrimary">#FF9800</color>
  <color name="colorPrimaryDark">#F57C00</color>
  <color name="colorAccent">#FF5722</color>
  <color name="colorPrimaryLight">#FFE0B2</color>
  <color name="colorPrimaryText">#212121</color>
  <color name="colorSecondaryText">#757575</color>
  <color name="colorIcons">#212121</color>
  <color name="colorDivider">#BDBDBD</color>
</resources>
```
4) **(add-block)** ***Route:** /res/values/styles.xml* ---  **SET APP STYLES**	
```xml
<resources>
  <style name="AppTheme" parent="Theme.AppCompat.Light.DarkActionBar">
    <item name="colorPrimary">@color/colorPrimary</item>
    <item name="colorPrimaryDark">@color/colorPrimaryDark</item>
    <item name="colorAccent">@color/colorAccent</item>
    <item name="android:textColorPrimary">@color/colorPrimaryText</item>
    <item name="android:textColorSecondary">@color/colorSecondaryText</item>
    <item name="android:horizontalDivider">@color/colorDivider</item>
  </style>

  <style name="AppTheme.NoActionBar">
    <item name="windowActionBar">false</item>
    <item name="windowNoTitle">true</item>
  </style>

  <style name="AppTheme.AppBarOverlay" parent="ThemeOverlay.AppCompat.Dark.ActionBar" />

  <style name="AppTheme.PopupOverlay" parent="ThemeOverlay.AppCompat.Light" />
</resources>
```
	