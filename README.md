# Initial Configuration

1) **(add-line)** ***Route:** /manifests/AndroidManifest.xml/* ---  **ADD INTERNET PERMISSIONS**
```xml
<uses-permission android:name="android.permission.INTERNET" />
<application
  android.name=".CatchUpApp"
  ...
>
...
</application>
```
2) **(add-line)** ***Route:** Gradle Scripts/build.gradle(Module: app)* ---  **ADD NETWORKING LIBRARY**
```kotlin
dependencies {
  ...
  implementation 'com.amitshekhar.android:android-networking:1.0.2'
  ...
}
```
3) **(edit-content)** ***Route:** /res/values/colors.xml* ---  **SET COLOR PALLETE**
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
4) **(edit-content)** ***Route:** /res/values/styles.xml* ---  **SET APP STYLES**	
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

  <style 
    name="AppTheme.AppBarOverlay"
    parent="ThemeOverlay.AppCompat.Dark.ActionBar"
  />

  <style name="AppTheme.PopupOverlay" parent="ThemeOverlay.AppCompat.Light" />
</resources>
```
5) **(edit-content)** ***Route:** /res/values/strings.xml* ---  **SET APP STRINGS**	
```xml
<resources>
  <string name="app_name">CatchUp</string>
  <string name="action_settings">Settings</string>
  <string name="onboarding_welcome_text">Welcome to CatchUp!</string>
  <string name="onboarding_start_button_title">Start</string>
  <string name="title_activity_main">CatchUp</string>
  <string name="title_home">Home</string>
  <string name="title_sources">Sources</string>
  <string name="title_favorites">Favorites</string>
  <string name="title_settings">Settings</string>

  <!-- TODO: Remove or change this placeholder text -->
  <string name="hello_blank_fragment">Hello blank fragment</string>
  <string name="mock_text">Mock Text</string>
  <string name="title_activity_article">About Article</string>
  <string name="title_activity_source">About Source</string>
</resources>
```
6) **(edit-content)** ***Route:** /res/values/dimens.xml* ---  **SET APP DIMENSIONS**
```xml
<resources>
  <dimen name="fab_margin">16dp</dimen>
  <dimen name="default_margin">16dp</dimen>
  <!-- Default screen margins, per the Android Design guidelines. -->
  <dimen name="activity_horizontal_margin">16dp</dimen>
  <dimen name="activity_vertical_margin">16dp</dimen>
  <dimen name="default_image_size">120dp</dimen>
  <dimen name="image_big_side">180dp</dimen>
</resources>
```
7) **(create-file)** ***Route:** /java/pe.edu.upc.catchup/**CatchUpApp.kt*** ---  **INITIALIZE ANDROID NETWORKING**	
```kotlin
class CatchUpApp : Application() {
  override fun onCreate() {
    super.onCreate()
    AndroidNetworking.initialize(getApplicationContext())
  }
}
```
