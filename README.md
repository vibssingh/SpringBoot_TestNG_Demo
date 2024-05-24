**Spring Boot with TestNG Integration**

This is a sample application to demonstrate how to setup and run SpringBoot tests with TestNG.
````
1. This framework consists of:
   Springboot – 3.5.0
   Java 17
   TestNG – 7.10.2
   Maven – 3.9.6
   RestAssured – 5.4.0
````

2. To run the tests through Maven command line, add the below dependency to surefire plugin:
````
<plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-surefire-plugin</artifactId>
        <version>${maven.surefire.plugin.version}</version>
        <configuration>
          <suiteXmlFiles>
            <suiteXmlFile>testng.xml</suiteXmlFile>
          </suiteXmlFiles>
        </configuration>
        <dependencies>
          <dependency>
            <groupId>org.apache.maven.surefire</groupId>
            <artifactId>surefire-testng</artifactId>
            <version>${maven.surefire.plugin.version}</version>
          </dependency>
        </dependencies>
      </plugin>
````

3. Use the below command to run the tests through Maven
````
   mvn clean test
````   
4. Reports - This framework contains sample TestNG Reports under test-output folder.

5. Surefire Reports can be seen under target/surefire-reports.