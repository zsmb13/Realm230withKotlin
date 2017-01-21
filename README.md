#Realm 2.3.0 with Kotlin issue

Adding Realm 2.3.0 to a brand new, clean Kotlin project makes the build fail with the following message:

```
FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':app:compileDebugAndroidTestJavaWithJavac'.
> java.lang.NoClassDefFoundError: org/jetbrains/kotlin/annotation/AnnotationProcessorWrapper
```
