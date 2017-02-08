#Realm 2.3.0 with Kotlin issue

Adding Realm 2.3.0 to a brand new, clean Kotlin project makes the build fail with the following message:

```
FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':app:compileDebugAndroidTestJavaWithJavac'.
> java.lang.NoClassDefFoundError: org/jetbrains/kotlin/annotation/AnnotationProcessorWrapper
```

###Update:

Adding
```
apply plugin: 'kotlin-kapt'
```
to the module level gradle file solves this issue.

The issue is tracked here: https://github.com/realm/realm-java/issues/4087

###Update 2:

As of Realm 2.3.1 this is no longer an issue, it works just fine without the `kotlin-kapt` plugin.

The commit that fixed it can be found here: https://github.com/realm/realm-java/commit/8055b1772f89998a87f3bb9e26ccdd0591615589
