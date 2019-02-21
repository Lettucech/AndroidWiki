Tell Shrinker keep class name
```
-keep class
```

Tell Shrinker keep the class name but remove it if nobody use it
```
-keep,allowshrinking class
```

Tell Shrinker keep class members (get/set method here) for runtime instantiated objects.
The reason that no need to keep class name is because the instantiation is not reflection.
```
-keepclassmembers class com.example.** {
  *** get*();
  void set*(***);
}
```
