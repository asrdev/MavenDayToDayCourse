#Known Maven Build Errors

### 1. could not find dependency: (any phase)
        -----------------------------
        [INFO] ------------------------------------------------------------------------
        [INFO] BUILD FAILURE
        [INFO] ------------------------------------------------------------------------
        [INFO] Total time: 01:36 min
        [INFO] Finished at: 2018-05-23T11:07:36+05:30
        [INFO] ------------------------------------------------------------------------
        [ERROR] Failed to execute goal org.apache.maven.plugins:maven-checkstyle-plugin:3.0.0:checkstyle (default-cli) on project Addition: Execution default-cli of goal org.apache.maven.plugins:maven-checkstyle-plugin:3.0.0:checkstyle failed: Plugin org.apache.maven.plugins:maven-checkstyle-plugin:3.0.0 or one of its dependencies could not be resolved: Could not transfer artifact antlr:antlr:jar:2.7.7 from/to central (https://repo.maven.apache.org/maven2): GET request of: antlr/antlr/2.7.7/antlr-2.7.7.jar from central failed: Connection reset -> [Help 1]


### 2. Compilation errors: mvn compile


        [INFO] -------------------------------------------------------------
        [ERROR] COMPILATION ERROR :
        [INFO] -------------------------------------------------------------
        [ERROR] /C:/Users/mycomputer/Documents/Selenium/DevOpsWebApp/src/main/java/LoginServlet.java:[30,25] cannot find symbol
          symbol:   variable out
          location: class LoginServlet
        [ERROR] /C:/Users/mycomputer/Documents/Selenium/DevOpsWebApp/src/main/java/LoginServlet.java:[35,9] cannot find symbol
          symbol:   variable out
          location: class LoginServlet
        [INFO] 2 errors
        [INFO] -------------------------------------------------------------
        [INFO] ------------------------------------------------------------------------
        [INFO] BUILD FAILURE
        [INFO] ------------------------------------------------------------------------
        [INFO] Total time: 3.540 s
        [INFO] Finished at: 2018-06-07T12:44:49+05:30
        [INFO] ------------------------------------------------------------------------
        [ERROR] Failed to execute goal org.apache.maven.plugins:maven-compiler-plugin:3.1:compile (default-compile) on project DevOpsWebApp: Compilation failure: Compilation failure:


### 3. testCompilation error: mvn test  (testCompile)

        [ERROR] COMPILATION ERROR :
        [INFO] -------------------------------------------------------------
        [ERROR] /C:/Users/mycomputer/Documents/Selenium/DevOpsWebApp/src/test/java/LoginServletTest.java:[18,20] cannot find symbol
          symbol:   variable booln
          location: class LoginServletTest
        [ERROR] /C:/Users/mycomputer/Documents/Selenium/DevOpsWebApp/src/test/java/LoginServletTest.java:[18,19] illegal start of type
        [ERROR] /C:/Users/mycomputer/Documents/Selenium/DevOpsWebApp/src/test/java/LoginServletTest.java:[22,28] cannot find symbol
          symbol:   variable booln
          location: class LoginServletTest
        [INFO] 3 errors
        [INFO] -------------------------------------------------------------
        [INFO] ------------------------------------------------------------------------
        [INFO] BUILD FAILURE
        [INFO] ------------------------------------------------------------------------
        [INFO] Total time: 3.625 s
        [INFO] Finished at: 2018-06-07T12:55:58+05:30
        [INFO] ------------------------------------------------------------------------
        [ERROR] Failed to execute goal org.apache.maven.plugins:maven-compiler-plugin:3.1:testCompile (default-testCompile) on project DevOpsWebApp: Compilation failure: Compilation failure:


### 4. test case failures: mvn test (surefire test)

        Results :

        Failed tests:   testUserCheck(LoginServletTest): expected:<true> but was:<false>

        Tests run: 1, Failures: 1, Errors: 0, Skipped: 0

        [INFO] ------------------------------------------------------------------------
        [INFO] BUILD FAILURE
        [INFO] ------------------------------------------------------------------------
        [INFO] Total time: 5.018 s
        [INFO] Finished at: 2018-06-07T12:17:40+05:30
        [INFO] ------------------------------------------------------------------------
        [ERROR] Failed to execute goal org.apache.maven.plugins:maven-surefire-plugin:2.12.4:test (default-test) on project DevOpsWebApp: There are test failures.
        [ERROR]
        [ERROR] Please refer to C:\Users\mycomputer\Documents\Selenium\DevOpsWebApp\target\surefire-reports for the individual test results.


### 5. checkstyle errors: mvn checkstyle:checkstyle checkstyle:check

        [ERROR] src\main\java\WelcomeServlet.java:[22] (regexp) RegexpSingleline: Line has trailing spaces.
        [INFO] ------------------------------------------------------------------------
        [INFO] BUILD FAILURE
        [INFO] ------------------------------------------------------------------------
        [INFO] Total time: 58.903 s
        [INFO] Finished at: 2018-06-07T12:59:42+05:30
        [INFO] ------------------------------------------------------------------------
        [ERROR] Failed to execute goal org.apache.maven.plugins:maven-checkstyle-plugin:3.0.0:check (default-cli) on project DevOpsWebApp: You have 108 Checkstyle violations. -> [Help 1]


### 6. coverage failure: (jacoco)

        [INFO] --- jacoco-maven-plugin:0.7.5.201505241946:check (jacoco-check) @ DevOpsWebApp ---
        [INFO] Analyzed bundle 'DevOpsWebApp-1.0.0-SNAPSHOT' with 2 classes
        [WARNING] Rule violated for package default: classes covered ratio is 0.50, but expected minimum is 0.80
        [INFO] ------------------------------------------------------------------------
        [INFO] BUILD FAILURE
        [INFO] ------------------------------------------------------------------------
        [INFO] Total time: 15.587 s
        [INFO] Finished at: 2018-06-07T16:59:47+05:30
        [INFO] ------------------------------------------------------------------------
        [ERROR] Failed to execute goal org.jacoco:jacoco-maven-plugin:0.7.5.201505241946:check (jacoco-check) on project DevOpsWebApp: Coverage checks have not been met. See log for details. -> [Help 1]

### 7. Server offline/access issue: error code 401: (while deploy to any server)

        [ERROR] Tomcat return http status error: 401, Reason Phrase: Invalid password/token for user: tomcat
        [INFO] ------------------------------------------------------------------------
        [INFO] BUILD FAILURE
        [INFO] ------------------------------------------------------------------------
        [INFO] Total time: 18.175 s
        [INFO] Finished at: 2018-05-23T11:30:25+05:30
        [INFO] ------------------------------------------------------------------------
        [ERROR] Failed to execute goal org.apache.tomcat.maven:tomcat7-maven-plugin:2.2:deploy (default-cli) on project WebApp: Tomcat return http status error: 401, Reason Phrase: Invalid password/token for user: tomcat:  -> [Help 1]

### 8. No proper permissions on the server: error code 403: (while deploy to any server)

        [ERROR] Tomcat return http status error: 403, Reason Phrase: Forbidden
        [INFO] ------------------------------------------------------------------------
        [INFO] BUILD FAILURE
        [INFO] ------------------------------------------------------------------------
        [INFO] Total time: 5.432 s
        [INFO] Finished at: 2018-05-23T11:40:44+05:30
        [INFO] ------------------------------------------------------------------------
        [ERROR] Failed to execute goal org.apache.tomcat.maven:tomcat7-maven-plugin:2.2:deploy (default-cli) on project WebApp: Tomcat return http status error: 403, Reason Phrase: Forbidden: <!DOCTYP
        <title>403 Access Denied</title>

### 9. Jacoco Config error:
        -------------------------------------------------------
         T E S T S
        -------------------------------------------------------
        Error: Could not find or load main class @{argLine}

        Results :

        Tests run: 0, Failures: 0, Errors: 0, Skipped: 0

        [INFO] ------------------------------------------------------------------------
        [INFO] BUILD FAILURE
        [INFO] ------------------------------------------------------------------------
        [INFO] Total time: 5.679 s
        [INFO] Finished at: 2018-06-07T14:12:10+05:30
        [INFO] ------------------------------------------------------------------------
        [ERROR] Failed to execute goal org.apache.maven.plugins:maven-surefire-plugin:2.12.4:test (default-test) on project DevOpsWebApp: Execution default-test of goal org.apache.maven.plugins:maven-surefire-plugin:2.12.4:test failed: The forked VM terminated without saying properly goodbye. VM crash or System.exit called ? -> [Help 1]
        
        
        
        
