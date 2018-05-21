# proxy-object
Load java jar files dynamically in isolated class loader to avoid dependency conflicts and enable modular updates

## Code Examples
1. Create Object from a JAR file located in the myLib/2.0 folder:
```java
ObjectBuilder builder = ObjectBuilder.builder()
       .setPackageName("org.my.package")
       .setClassName("MyClass")
       .setVersionInfo(newVersionInfo("myLib", "2.0"))
       .build();
builder.call("objectMethod");
