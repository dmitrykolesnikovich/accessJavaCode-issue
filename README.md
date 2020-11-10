### Problem with sharing Java code between Android and JVM targets

I am trying to share Java code between android and desktop using Kotlin Multiplatform feature.

I have Java code in module "library1" and Kotlin code accessing it from module "library2".

![library2 depends on library1](dependencies.png)

When I am trying to build this sample project I am getting `Unresolved reference` error:

```
> Task :library2:compileKotlinJvm FAILED
e: ../CallingJavaCodeFromKotlinLibrary2.kt: (3, 52): Unresolved reference: JavaCode
```
