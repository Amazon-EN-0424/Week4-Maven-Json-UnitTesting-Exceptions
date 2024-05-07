# 📚 Week 4

## 🔧 Introduction to Maven

### Understanding Maven
- **What is Maven?**
  - Maven is a build automation and project management tool for Java projects.
  - It simplifies the build process, dependency management, and project structure.

### Basic Operations
- **Creating a Maven Project:**
  - Use an IDE to create a new Maven project.
  - Define the project's `groupId`, `artifactId`, and `version` in the `pom.xml` file.

- **Managing Dependencies:**
  - Declare project dependencies in the `pom.xml` file.
  - Maven automatically downloads and manages the required libraries.

- **Building the Project:**
  - Use Maven commands like `mvn compile`, `mvn test`, and `mvn package` to build the project.

### 🚀 Practical Exercise: Building a Maven Project
- **Task:** Create a simple Maven project and explore its structure and build process.
- **Instructions:**
  - Create a new Maven project using your IDE
  - Define a simple Java class.
  - Build the project using Maven commands and observe the generated artifacts.

### 💡 Discussion
- Discuss the benefits of using Maven for Java project management and build automation.
- Explore how Maven simplifies dependency management and promotes a standardized project structure.

## 📊 JSON and GSON Library

### Understanding JSON
- **What is JSON?**
  - JSON (JavaScript Object Notation) is a lightweight data interchange format.
  - It is easy for humans to read and write and easy for machines to parse and generate.

### Basic Operations with GSON
- **Adding GSON Dependency:**
  - Include the GSON library dependency in your project's `pom.xml` file.

- **Object to JSON Conversion:**
  ```java
  Gson gson = new Gson();
  String json = gson.toJson(object);
  ```

- **JSON to Object Conversion:**
  ```java
  Gson gson = new Gson();
  Object object = gson.fromJson(json, Object.class);
  ```

- **Reading from a JSON File:**
  ```java
  Gson gson = new Gson();
  BufferedReader reader = new BufferedReader(new FileReader("file.json"));
  Object object = gson.fromJson(reader, Object.class);
  ```

### 🗺️ Practical Exercise: JSON Serialization and Deserialization
- **Task:** Use the GSON library to convert Java objects to JSON and vice versa.
- **Instructions:**
  - Create a Java class with a few fields and methods.
  - Use GSON to convert an instance of the class to a JSON string.
  - Write the JSON string to a file.
  - Read the JSON file and deserialize it back into a Java object.

### 💡 Discussion
- Discuss the importance of JSON as a data interchange format in modern web development.
- Explore how libraries like GSON simplify working with JSON in Java applications.

## 🧪 Introduction to Unit Testing and JUnit 5

### Understanding Unit Testing
- **What is Unit Testing?**
  - Unit testing is a software testing method that focuses on testing individual units or components of code.
  - It helps ensure the correctness and reliability of individual parts of the application.

### JUnit 5 Basics
- **Adding JUnit 5 Dependency:**
  - Include the JUnit 5 dependency in your project's `pom.xml` file.

- **Writing a Test Case:**
  ```java
  import org.junit.jupiter.api.Test;
  import static org.junit.jupiter.api.Assertions.*;

  class ExampleTest {
      @Test
      void testMethod() {
          // Test case logic here
          assertEquals(expected, actual);
      }
  }
  ```

- **Running Tests:**
  - Use an IDE or Maven command `mvn test` to run the test cases.

### Test-Driven Development (TDD)
- **What is TDD?**
  - TDD is a software development approach where tests are written before the actual code.
  - It follows a cycle of writing a failing test, writing minimal code to pass the test, and refactoring the code.

### 🧩 Practical Exercise: Testing a Java Class
- **Task:** Write unit tests for a Java class using JUnit 5.
- **Instructions:**
  - Create a Java class with a few methods that perform specific operations.
  - Write unit tests for each method using JUnit 5 assertions.
  - Run the tests and ensure they pass.
  - Optionally, practice TDD by writing tests before implementing the methods.

### 💡 Discussion
- Discuss the benefits of unit testing in ensuring code quality and reducing bugs.
- Explore how TDD can lead to more reliable and maintainable code.

## 🚨 Exception Handling

### Understanding Exceptions
- **What are Exceptions?**
  - Exceptions are events that occur during the execution of a program, disrupting the normal flow of instructions.
  - They are used to handle errors or exceptional conditions gracefully.

### Types of Exceptions
- **Checked Exceptions:**
  - Checked exceptions are checked at compile-time and must be explicitly handled or declared in the method signature.
  - Examples: `IOException`, `SQLException`.

- **Unchecked Exceptions:**
  - Unchecked exceptions are not checked at compile-time and do not need to be explicitly handled.
  - Examples: `NullPointerException`, `ArrayIndexOutOfBoundsException`.

### Handling Exceptions
- **Try-Catch Block:**
  ```java
  try {
      // Code that may throw an exception
  } catch (ExceptionType e) {
      // Exception handling code
  }
  ```

- **Throwing Exceptions:**
  ```java
  if (condition) {
      throw new ExceptionType("Exception message");
  }
  ```

### 🎯 Practical Exercise: Handling Exceptions
- **Task:** Implement exception handling in a Java program.
- **Instructions:**
  - Create a Java class with a method that may throw an exception.
  - Use a try-catch block to handle the exception gracefully.
  - Throw a custom exception in a specific scenario.

### 💡 Discussion
- Discuss the importance of exception handling in creating robust and reliable software.
- Explore best practices for handling exceptions and designing exception hierarchies.

## 🧪🚨 Unit Testing with Exceptions

### Testing Exceptions
- **Asserting Exceptions with JUnit 5:**
  ```java
  import org.junit.jupiter.api.Test;
  import static org.junit.jupiter.api.Assertions.*;

  class ExceptionTest {
      @Test
      void testExceptionThrown() {
          assertThrows(ExceptionType.class, () -> {
              // Code that throws the exception
          });
      }
  }
  ```

### 🎯 Practical Exercise: Testing Exception Scenarios
- **Task:** Write unit tests to verify exception handling in a Java class.
- **Instructions:**
  - Create a Java class with methods that throw exceptions in specific scenarios.
  - Write unit tests using JUnit 5 to assert that the expected exceptions are thrown.
  - Ensure that the exceptions are handled correctly in the class.

### 💡 Discussion
- Discuss the importance of testing exception scenarios to ensure the robustness of the application.
- Explore strategies for designing effective exception handling tests.
