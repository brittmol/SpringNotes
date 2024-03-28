## You will be able to identify the advantages of Java

- **Platform Independence (Write Once, Run Anywhere - WORA):**
  - Java uses the "Write Once, Run Anywhere" philosophy, meaning you can write code on one platform (e.g., Windows) and run it on any other platform (e.g., Linux or macOS) without modification. This is achieved through the use of the Java Virtual Machine (JVM), which interprets Java bytecode.
- **Object-Oriented Programming (OOP):**
  - Java is designed around the principles of Object-Oriented Programming, promoting modular and reusable code. Objects encapsulate data and behavior, making it easier to understand and maintain code.
- **Robust and Secure:**
  - Java enforces strong type-checking during compile time and runtime checks, reducing the likelihood of errors. Additionally, it has built-in security features, such as the Java Security Manager, to create a secure computing environment.
- **Automatic Memory Management (Garbage Collection):**
  - Java uses a garbage collector to automatically manage memory, freeing developers from manual memory allocation and deallocation. This reduces the risk of memory leaks and enhances the stability of Java applications.
- **Rich Standard Library:**
  - Java comes with a comprehensive standard library that provides ready-to-use classes and methods for common tasks. This allows developers to be more productive and focus on solving specific problems rather than reinventing the wheel.

**Revature:** Java advantages include platform independence, C-language inspired syntax, automatic memory management, an extensive built-in runtime library, support from the Oracle corporation, and a rich open source community.

---

## You will be able to explain the difference between JDK, JRE, and JVM

- **JVM (Java Virtual Machine):**
  - Think of the JVM as a virtual computer that executes Java bytecode. When you compile your Java source code, it's translated into bytecode, which is platform-independent. The JVM is responsible for running this bytecode on the target machine.
  - It provides an abstraction layer between your Java program and the underlying hardware and operating system, ensuring that Java applications can run on any device with a compatible JVM.
  - The JVM also manages memory, performs garbage collection, and provides runtime services.
- **JRE (Java Runtime Environment):**
  - The JRE is a package of software that includes the JVM, libraries, and other components required to run Java applications, but it doesn't include development tools.
  - If you only want to run Java applications and don't intend to develop them, you just need the JRE. It provides everything needed at runtime.
- **JDK (Java Development Kit):**
  - The JDK is a full-featured software development kit that includes the JRE, development tools (compiler, debugger, etc.), and additional libraries to facilitate Java development.
  - If you plan to write, compile, and run Java code, you'll need the JDK. It's a superset of the JRE, containing everything needed for both development and execution.
- In summary:
  - **JVM** is the runtime environment that executes Java bytecode.
  - **JRE** is a package that includes the JVM and libraries needed to run Java applications.
  - **JDK** is a comprehensive development kit that includes the JRE, development tools, and libraries for Java development.

---

## You will be able to discuss the foundations of Java Garbage collection

- **1. Memory Management in Java:**
  - **Heap Memory:**
    - Objects in Java are created in the heap memory, a region dedicated to storing objects dynamically allocated during the program's execution.
    - The heap is managed by the garbage collector to automatically allocate and deallocate memory.
- **2. Garbage Collection Basics:**
  - **What is Garbage Collection?**
    - Garbage Collection is the process of automatically identifying and reclaiming memory occupied by objects that are no longer in use or reachable by the program.
  - **Why Garbage Collection?**
    - Manual memory management can lead to memory leaks and program instability. Garbage Collection automates the process, freeing developers from manual memory cleanup.
- **3. How Garbage Collection Works:**
  - **Mark and Sweep:**
    - The most common garbage collection algorithm.
    - It works in two phases:
      1. **Marking Phase:** Identifies all objects that are reachable from the root of the application (like variables in the main method).
      2. **Sweeping Phase:** Removes or deallocates memory for objects that are not marked as reachable.
- **4. Object Reachability:**
  - **Roots:**
    - The starting point for the garbage collector.
    - Examples include local variables in the main method, static variables, and references from native methods.
  - **Reachable Objects:**
    - Objects that are accessible or reachable from the roots.
    - These objects are considered "alive" and won't be garbage collected.
  - **Unreachable Objects:**
    - Objects that are not accessible from the roots.
    - These objects are candidates for garbage collection.
- **5. Finalization and `finalize()` method:**

  - **`finalize()` Method:**

    - A method in the **`Object`** class that can be overridden by user-defined classes.
    - It is called by the garbage collector before an object is reclaimed.

      ```java
      public class MyClass {
          @Override
          protected void finalize() throws Throwable {
              // Cleanup logic before garbage collection
              super.finalize();
          }
      }
      ```

### **Metaphor:**

Think of the heap memory as a bustling city where objects live. Garbage collection is like a diligent janitor who roams the city, identifies abandoned buildings (unreachable objects), and clears them away to free up space for new constructions.

- **Roots are like the main entrances:**
  - People (references) enter the city through main entrances (roots). The janitor starts from these entrances to identify the buildings (objects) that are still in use.
- **Reachable objects are like occupied buildings:**
  - Buildings that can be reached from the entrances (roots) are considered occupied (alive). The janitor knows not to touch them.
- **Unreachable objects are like abandoned buildings:**
  - Buildings that can't be reached from the entrances (unreachable objects) are considered abandoned. The janitor marks them for demolition (garbage collection).

---

## You will be able to describe stack and heap memory in Java

- **1. Stack Memory:**

  - **Description:**
    - Stack memory is used for the execution of a thread. Each thread in a Java application has its own stack, and it's used for storing local variables and managing method calls.
  - **Characteristics:**
    - **LIFO (Last-In-First-Out):** The last method called is the first one to finish, and its stack frame is removed.
    - **Fast Access:** Accessing variables in the stack is faster than in the heap because it follows a simple and fixed pattern.
  - **Examples:**
    - **Local Variables:** Variables declared inside a method.
    - **Method Calls:** Each method call gets its own stack frame.

  ```java
  public class StackExample {
      public static void main(String[] args) {
          int a = 5; // Variable 'a' is stored in the stack
          int b = calculateSquare(a); // Method call creates a new stack frame
      }

      private static int calculateSquare(int num) {
          return num * num;
      }
  }
  ```

- **2. Heap Memory:**

  - **Description:**
    - Heap memory is used for dynamic memory allocation. Objects, arrays, and instances of classes are stored in the heap.
  - **Characteristics:**
    - **Larger Memory Pool:** The heap is generally larger than the stack, and memory can be allocated and deallocated at runtime.
    - **Slower Access:** Accessing variables in the heap is slightly slower than in the stack because it involves a more complex process.
  - **Examples:**
    - **Objects and Arrays:** Instances of classes and arrays are allocated in the heap.
    - **Dynamic Memory:** Memory allocated using **`new`** keyword.

  ```java
  public class HeapExample {
      public static void main(String[] args) {
          // Objects are allocated in the heap
          String message = new String("Hello, Heap!");
          System.out.println(message);
      }
  }
  ```

### **Metaphor:**

Think of the stack as a stack of plates in a cafeteria. When you add a plate (method call), it goes on top. When you remove a plate (method finishes), you take it from the top. It's a straightforward and organized process.

Now, envision the heap as a shared dining table where people can sit. Each person (object) gets a seat, and seats can be dynamically allocated or freed up as needed. It's a more flexible but slightly more complex arrangement.

In Java, stack memory is like having a personal notebook (local variables) on your desk while working on a specific task. Heap memory is like having a communal storage room (dynamic memory) where you can keep larger items that are shared among different tasks.

---
