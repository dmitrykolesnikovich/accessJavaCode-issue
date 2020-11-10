### Question on StackOverflow

https://stackoverflow.com/questions/59479020/how-to-share-java-code-between-android-and-jvm-targets-with-kotlin-multiplatfor

### Issue Description

I am trying to share Java code between android and desktop using Kotlin Multiplatform feature.

I have Java code in `library1` and Kotlin code accessing it from `library2`.

![library2 depends on library1](dependencies.png)

When I am trying to build this sample project I am getting `Unresolved reference` error:

```
> Task :library2:compileKotlinJvm FAILED
e: ../CallingJavaCodeFromKotlinLibrary2.kt: (3, 52): Unresolved reference: JavaCode
```
