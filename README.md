# jcuda-parent

The parent POM project for JCuda. 

The Java compiler source and bytecode target are Java 8. Rebuilt artifacts
therefore require a Java 8 or newer runtime. This matches the Java 8 APIs
already used by the core library, such as `Math.toIntExact`.

Install this parent before building a sibling Java module:

```text
mvn install
mvn -f ../jcuda/JCudaJava/pom.xml test-compile
```

This target also avoids the rejected Java 7 compiler options on newer JDKs.
It does not by itself update the other Maven plugins, build native libraries,
or establish compatibility of every module or packaging goal with every JDK.

Refer to [jcuda-main](https://github.com/jcuda/jcuda-main) for further
information and build instructions.
