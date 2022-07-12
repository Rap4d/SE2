# pitest-plugins

This repository contains the self made RandomTestPrioritiserPlugin for the pitest mutation testing system. This Plugin was purely created for academic research.

This plugin is not currently released. To install locally from source

```bash
mvn install
```

To use this plugins via maven add them as dependencies to the pitest-maven plugin (i.e **not** to your project dependencies) e.g

```xml
      <build>
    <plugins>
        <plugin>
        <groupId>org.pitest</groupId>
        <artifactId>pitest-maven</artifactId>
        <version>1.4.0</version>
        <dependencies>
            <dependency>
                <groupId>org.pitest.plugins</groupId>
                <artifactId>random-test-prioritiser-plugin</artifactId>
                <version>0.1-SNAPSHOT</version>
            </dependency>
             </dependencies>
     </plugin>
	</plugins>
</build>
</project>
```

# The examples

## RandomTestPrioritiserPlugin

This plugin uses the TestPrioritiserFactory extension point to run half of the test suite against each mutation.

It's similar to the bogus sort algorithm. 
By luck, we might hit a faster time than regular pitest. This is only the case if we actually manage to test only the neccessary mutations/use the neccessary test suites.


This plugin will make mutation testing fast in b/c. In w/c it will make it slow. (see Bogus Sort)


