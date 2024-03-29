# Unit Testing Assignment

The current module serves the unit testing of the given Java source files. Implemented with the Maven build
automation tool, several test cases evaluate the functionality of multiple operations. Aiming to verify
the tests' expected behavior, we take into consideration exception cases as well a plethora of challenging
instances. Being dependant on the JUnit testing framework (version 4.12), we apply a variety of techniques
for the needs of a sufficient testing coverage level.

## Getting started with the Unit Testing project

### Software Requirements

- [Git](https://git-scm.com/)
- [Java](https://www.java.com/en/)
- [Maven](https://maven.apache.org/)

### Project Structure

Implementing project inherintance, we follow an hierarchical parent - child structure, with:

- [seip-lab](https://www.github.com/demetres12/seip-lab) --> being the **parent**, and
	- [unittesting](https://www.github.com/demetres12/seip-lab/tree/development-2/unittesting) --> being the **module**

#### Structure of the module before building
<h1 align="center">
	<img height="600"  width="500" src="../media/unittesting-tree-before-build.png" alt="">
</h1>

#### Structure of the module's build output

<h1 align="center">
	<img height="600"  width="500" src="../media/unittesting-tree-build-output.png" alt="">
</h1>

### Step by Step

1. Initially, it's recommended to take a look at the main [README](https://github.com/demetres12/seip-lab/blob/development-2/README.md), in order to get familiar with Maven's lifecycles.

2. In case you need to run all the tests, execute the following command.

```bash
# In our example we run each and every test case / method located in the src/test.
mvn test
```

3. Otherwise, to run an individual test class, execute the command stated below.

```bash
# In our example, we run each and every test case / method in reference to the MyMathTest java class.
 mvn -Dtest=MyMathTest test
```

4. Finally, if you need to run a single test case / method, specify that by the upcoming command.

```bash
# In our example, we run the `test_isPrimeReturnsFalse` test case / method in reference to the MyMathTest java class.
 mvn -Dtest=MyMathTest#test_isPrimeReturnsFalse test
```

#### Noteworthy Comments

- Following Unit Testing optimal practices, we consider *naming conventions, code readability / maintenability and Annotations / Assertions
proper declaration* to be of paramount importance.
- Our project utilizes Mockito Java framework, in order to handle effectively dependencies in the context of unit testing.
- Note that only classes with a **Test suffix** located in the src/test will be executed and reported as Tests.
- When running signle test classes or methods, make sure that your working directory is set accordingly, so it includes the `pom.xml` file.