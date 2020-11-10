### Problem with sharing Java code between Android and JVM targets

I am trying to share Java code between android and desktop using Kotlin Multiplatform feature.

In short: I have Java code in module "library1" and Kotlin code accessing it from module "library2".

![library2 depends on library1](docs/dependency-graph.png)

When I am trying to build this sample project I am getting `Unresolved reference` error:

```
> Task :library2:compileKotlinJvm FAILED
e: ../AccessJavaCodeExternally.kt: (3, 38): Unresolved reference: JavaCode
```

Most probably there is something in my Gradle configuration goes wrong, but I am stuck with understanding what exactly.
