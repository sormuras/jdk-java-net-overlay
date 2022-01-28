# jdk-java-net-overlay

Additional resources for <https://jdk.java.net>

## `jdk-uri.properties`

The [jdk-uri.properties](jdk-uri.properties) file provides a set of key-value pairs mapping JDK
descriptions to their download links.

```properties
17,17.0.1,linux,x64=https://download.java.net/java/[...]/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz
```

Keys are composed of `FEATURE,VERSION,OS-NAME,OS-ARCH` with:

- `FEATURE`: Either a release feature number or a name of an early-access project
- `VERSION`: Either a specific version or `latest`
- `OS-NAME`: An operating system name, usually one of: `linux`, `macos`, `windows`
- `OS-ARCH`: An operating system architecture, like: `aarch64`, `x64`, or `x64-musl`

Run `java src/ListOpenJavaDevelopmentKits.java` to parse a set of default pages hosted
at <https://jdk.java.net> and print all key-value pairs, including aliases.
Consult [src/ListOpenJavaDevelopmentKits.java](src/ListOpenJavaDevelopmentKits.java) for details.

Run `java src/ListOpenJavaDevelopmentKits.java PAGE [MORE...]` to parse `https://jdk.java.net/PAGE`
only and print key-value pairs found on that particular page.
