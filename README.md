# Powered by 
[![](https://media.licdn.com/mpr/mpr/shrink_200_200/AAEAAQAAAAAAAAfpAAAAJGQxMzExNzY0LWUxZjAtNDk5OS1iYjg1LWUxYmUyOTRkMTkzYg.png)](https://uptech.team/)

### Android security tools

 * [Secure-preferences]
 * [DexGuard] - by Fabric
 * [ProGuard] - by Fabric

### Secure-preferences 

  Android Shared preference wrapper than encrypts the values of Shared Preferences. It's not bullet proof security but rather a quick win for incrementally making your android app more secure.

```
SecurePreferences prefs = new SecurePreferences(getContext(), "security_test","SECURITY_TEST.xml");
prefs.edit().putString("security_test", "security").apply();
```

this code save our string to preferences and we have result like this 

```
 <string name="nj+XbU6ahiJY18TLCV2lNtUkNhqLLixdKOYeNz9lLQ8=">rX85/SUNMw/DfWkITcdkZQ==:YMrJnNugY077GXnn2nquviD1PIIb89awiOeu4Lq0kjo=:JScKw4uV7P2+04tisONJfQ==</string>
```

If we will use just SharedPreferences we get this

```
<string name="security_test">security</string>
```


[Secure-preferences]: <https://github.com/scottyab/secure-preferences>
[DexGuard]: <https://docs.fabric.io/android/crashlytics/dex-and-proguard.html#using-dexguard>
[ProGuard]: <https://docs.fabric.io/android/crashlytics/dex-and-proguard.html>

