### Problem with accessing Java code from Kotlin code externally

I am trying to share Java code between android and desktop using Kotlin Multiplatform feature.

Here I published sample project to demonstrate issue I am struggling with: https://github.com/dmitrykolesnikovich/accessJavaCode-issue

In short: I have Java code in module "library1" and Kotlin code accessing it from module ":library2".

![library2 depends on library1](docs/dependency-graph.png)

When I am trying to build this sample project I am getting error:

```
> Task :library2:compileDebugKotlinAndroid FAILED
e: /Users/dmitrykolesnikovich/workspace/accessJavaCode-issue/library2/src/jvmMain/kotlin/accessJavaCode/issue/library2/AccessJavaCodeExternally.kt: (3, 38): Unresolved reference: JavaCode
e: /Users/dmitrykolesnikovich/workspace/accessJavaCode-issue/library2/src/jvmMain/kotlin/accessJavaCode/issue/library2/AccessJavaCodeExternally.kt: (5, 34): Unresolved reference: JavaCode
```

Most probably there is something in my Gradle configuration goes wrong, but I am stuck with understanding what exactly.

Any advice and suggestions will be greatly appreciated.
