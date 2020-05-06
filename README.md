## LiveWallpaperPicker
Ever had a problem finding the live wallpaper picker on MIUI? MIUI does not contain any option to open the LiveWallpaper Activity through the launcher or settings app.
This app acts as a shortcut to the LiveWallpaperPicker and lands you right to the list of your favorite live wallpapers.

### The below method can be used to redirect one app to another app's any(known) activity.
```
   public void shortcut(String appName, String appActivity){
        Intent intent = new Intent();
        intent.setClassName(appName, appName+"."+appActivity);
        intent.setFlags(Intent.FLAG_ACTIVITY_NEW_TASK);
        startActivity(intent);
       }
```
Uses:
```
   shortcut("com.android.wallpaper.livepicker", "LiveWallpaperActivity");
```
