## You will understand the structure of methods and create custom methods to perform business logic

A method in Java is a block of code that performs a specific task. Here's the basic structure:

```java
access_modifier return_type method_name(parameter_list) {
    // method body (code block)
    // business logic goes here
    return return_value; // optional
}
```

- **Access Modifier:** Specifies the visibility of the method (e.g., **`public`**, **`private`**, or **`protected`**). Determines from where the method can be accessed.
- **Return Type:** Specifies the type of value that the method will return. Use **`void`** if the method doesn't return any value.
- **Method Name:** A unique identifier for the method. Follows Java naming conventions.
- **Parameter List:** An optional list of parameters that the method can accept. Parameters provide input to the method.
- **Method Body:** The actual code that performs the task. It's enclosed in curly braces **`{}`**.
- **Return Statement:** If the method has a return type other than **`void`**, it must return a value of that type. The **`return`** statement is used for this purpose.

Let's create a simple example to illustrate creating a custom method:

```java
public class Calculator {

    // Custom method to add two numbers
    public int add(int num1, int num2) {
        int result = num1 + num2;
        return result;
    }

    public static void main(String[] args) {
        // Creating an instance of the Calculator class
        Calculator myCalculator = new Calculator();

        // Calling the custom method
        int sum = myCalculator.add(5, 7);

        // Displaying the result
        System.out.println("Sum: " + sum);
    }
}
```

- In this example, the **`add`** method takes two parameters (**`num1`** and **`num2`**) and returns their sum.
- The **`main`** method is the entry point of the program. It creates an instance of the **`Calculator`** class and calls the **`add`** method.
- The result is then printed to the console.

---

## You will understand the different primitive Java datatypes

### **1. Integer Types:**

- **`byte`:** 8 bits, range from -128 to 127.

    ```java
    byte myByte = 100;
    ```

- **`short`:** 16 bits, range from -32,768 to 32,767.

    ```java
    short myShort = 1000;
    ```

- **`int`:** 32 bits, range from -2^31 to 2^31 - 1.

    ```java
    int myInt = 100000;
    ```

- **`long`:** 64 bits, range from -2^63 to 2^63 - 1.

    ```java
    long myLong = 1000000000L; // Note the 'L' suffix for long literals
    ```


### **2. Floating-Point Types:**

- **`float`:** 32 bits, used for decimals. Note the 'f' suffix for float literals.

    ```java
    float myFloat = 3.14f;
    ```

- **`double`:** 64 bits, used for decimals (more precision than **`float`**).

    ```java
    double myDouble = 3.14159265359;
    ```


### **3. Character Type:**

- **`char`:** 16 bits, represents a single Unicode character.

    ```java
    char myChar = 'A';
    ```


### **4. Boolean Type:**

- **`boolean`:** Represents true or false values.

    ```java
    boolean isJavaFun = true;
    ```


---

## You will understand Java operators

### **1. Arithmetic Operators:**

These operators perform basic mathematical operations.

- **Addition (`+`):**

    ```java
    int sum = 5 + 3; // Result: 8
    ```

- **Subtraction (-):**

    ```java
    int difference = 7 - 4; // Result: 3
    ```

- **Multiplication (*):**

    ```java
    int product = 2 * 6; // Result: 12
    ```

- **Division (`/`):**

    ```java
    double quotient = 10.0 / 2; // Result: 5.0
    ```

- **Modulus (`%`):**

    ```java
    int remainder = 15 % 4; // Result: 3 (remainder of 15 divided by 4)
    ```


### **2. Comparison Operators:**

These operators compare two values and produce a boolean result.

- **Equal to (`==`):**

    ```java
    boolean isEqual = (5 == 5); // Result: true
    ```

- **Not equal to (`!=`):**

    ```java
    boolean isNotEqual = (7 != 3); // Result: true
    ```

- **Greater than (`>`):**

    ```java
    boolean isGreater = (10 > 8); // Result: true
    ```

- **Less than (`<`):**

    ```java
    boolean isLess = (4 < 6); // Result: true
    ```

- **Greater than or equal to (`>=`):**

    ```java
    boolean isGreaterOrEqual = (5 >= 5); // Result: true
    ```

- **Less than or equal to (`<=`):**

    ```java
    boolean isLessOrEqual = (3 <= 2); // Result: false
    ```


### **3. Logical Operators:**

These operators perform logical operations.

- **Logical AND (`&&`):**

    ```java
    boolean result = (true && false); // Result: false
    ```

- **Logical OR (`||`):**

    ```java
    boolean result = (true || false); // Result: true
    ```

- **Logical NOT (`!`):**

    ```java
    boolean result = !(true); // Result: false
    ```


---

## You will understand and utilize flow-control statements including if-else, switch, for loops, while-loops, and do-while loops

- **1. If-Else Statements:**

    Used for conditional execution based on a boolean expression.

    ```java
    int num = 10;

    if (num > 0) {
        System.out.println("Number is positive");
    } else if (num < 0) {
        System.out.println("Number is negative");
    } else {
        System.out.println("Number is zero");
    }
    ```

    - The **`if`** statement checks a condition. If it's true, the code inside the block is executed. If false, it moves to the **`else if`** or **`else`** part.
- **2. Switch Statement:**

    Used for multiple branches based on the value of an expression.

    ```java
    int dayOfWeek = 3;

    switch (dayOfWeek) {
        case 1:
            System.out.println("Monday");
            break;
        case 2:
            System.out.println("Tuesday");
            break;
        // ... (cases for other days)
        default:
            System.out.println("Invalid day");
    }
    ```

    - The **`switch`** statement evaluates the expression (**`dayOfWeek`** in this case) and executes the block of code associated with the matching **`case`**. The **`break`** statement is crucial to prevent fall-through.
- **3. For Loop:**

    Used for iterating a specific number of times.

    ```java
    for (int i = 1; i <= 5; i++) {
        System.out.println("Iteration " + i);
    }
    ```

    - The **`for`** loop consists of initialization (**`int i = 1`**), condition (**`i <= 5`**), and iteration (**`i++`**). It repeats the code block as long as the condition is true.
- **4. While Loop:**

    Used for repeated execution as long as a condition is true.

    ```java
    int count = 0;

    while (count < 3) {
        System.out.println("Count: " + count);
        count++;
    }
    ```

    - The **`while`** loop checks the condition (**`count < 3`**) before each iteration. If true, the code inside the loop is executed.
- **5. Do-While Loop:**

    Similar to the **`while`** loop but guarantees at least one execution.

    ```java
    int attempts = 0;

    do {
        System.out.println("Attempt: " + attempts);
        attempts++;
    } while (attempts < 3);
    ```

    - The **`do-while`** loop executes the code block first and then checks the condition. It ensures that the code block is executed at least once.

### **Metaphor:**

Think of flow-control statements as traffic signals in a city. The **`if-else`** statement is like a decision point where you choose a path based on conditions. The **`switch`** statement is like a junction with multiple roads, and you choose the road based on the value of a variable. The **`for`** loop is like driving a certain number of blocks, the **`while`** loop is like driving until you reach a specific condition, and the **`do-while`** loop is like driving at least once through a neighborhood before deciding to leave.

## You will learn the break and continue keywords

- **1. `break` Statement:**

    The **`break`** statement is used to terminate the loop prematurely. It's often used with the **`switch`** statement or to exit a loop based on a certain condition.

    **Example with a For Loop:**

    ```java
    for (int i = 1; i <= 5; i++) {
        if (i == 3) {
            System.out.println("Breaking the loop at i = 3");
            break;
        }
        System.out.println("Iteration " + i);
    }

    ```

    - In this example, the loop breaks when **`i`** becomes equal to 3. The output will be:

        ```arduino
        Iteration 1
        Iteration 2
        Breaking the loop at i = 3
        ```

- **2. `continue` Statement:**

    The **`continue`** statement is used to skip the rest of the loop's code block for the current iteration and move to the next iteration.

    **Example with a While Loop:**

    ```java
    int i = 0;

    while (i < 5) {
        i++;
        if (i == 2 || i == 4) {
            System.out.println("Skipping iteration " + i);
            continue;
        }
        System.out.println("Processing iteration " + i);
    }
    ```

    - In this example, the loop skips iterations where **`i`** is 2 or 4. The output will be:

        ```
        Processing iteration 1
        Skipping iteration 2
        Processing iteration 3
        Skipping iteration 4
        Processing iteration 5
        ```


### **Metaphor:**

Think of the **`break`** statement as an emergency exit in a building. When a specific condition is met, you want to break out of the loop or switch statement, just like using an emergency exit when needed.

On the other hand, the **`continue`** statement is like skipping a step in a recipe. If a certain condition is met, you want to skip the current iteration and move on to the next one, just like skipping a step in a cooking process when necessary.

---

## You will understand how to create, iterate over, and use arrays

- **1. Creating Arrays:**

    Arrays in Java are declared with a specific type and size. Here's how you can create arrays:

    ```java
    // Array of integers
    int[] numbers = new int[5];

    // Array of strings
    String[] names = new String[3];

    // Initializing array with values
    double[] temperatures = {23.5, 26.8, 22.1, 25.5, 24.0};
    ```

    - In the first example, an array of integers named **`numbers`** is created with a size of 5.
    - The second example creates an array of strings named **`names`** with a size of 3.
    - The third example initializes an array of doubles named **`temperatures`** with specific values.
- **2. Iterating Over Arrays:**

    You can use loops, such as the **`for`** loop, to iterate over array elements:

    ```java
    // Iterating over an array of integers
    for (int i = 0; i < numbers.length; i++) {
        System.out.println("Element at index " + i + ": " + numbers[i]);
    }

    // Iterating over an array of strings with enhanced for loop
    for (String name : names) {
        System.out.println("Name: " + name);
    }
    ```

    - The first example uses a **`for`** loop to iterate over the **`numbers`** array, printing each element and its index.
    - The second example uses an enhanced **`for`** loop to iterate over the **`names`** array, printing each name.
- **3. Using Arrays:**

    Arrays provide various methods and properties for manipulation:

    ```java
    // Accessing elements
    int firstNumber = numbers[0];
    System.out.println("First number: " + firstNumber);

    // Modifying elements
    temperatures[2] = 23.9;
    System.out.println("Updated temperature at index 2: " + temperatures[2]);

    // Finding the length of an array
    int lengthOfNumbers = numbers.length;
    System.out.println("Length of the numbers array: " + lengthOfNumbers);
    ```

    - You can access elements using square brackets (**`numbers[0]`** gets the first element).
    - Elements can be modified by assigning new values.
    - The **`length`** property provides the size of the array.

### **Metaphor:**

Think of an array as a row of mailboxes, where each mailbox has a unique number (index). Each mailbox can store something different (an element), and you can easily access and modify what's inside each mailbox. The array's length is like the number of mailboxes in the row.

Iterating over an array is like checking each mailbox in order. You can go from the first to the last, or use a shortcut to check what's inside each mailbox one by one.

---

## You will understand the static keyword

- **1. Static Variables:**

    When a variable is declared as **`static`**, it belongs to the class rather than instances of the class. All instances (objects) of the class share the same static variable.

    ```java
    public class MyClass {
        static int staticVariable = 10;
    }
    ```

    - In this example, **`staticVariable`** is shared among all instances of **`MyClass`**. If one instance modifies its value, the change is reflected for all instances.
- **2. Static Methods:**

    When a method is declared as **`static`**, it belongs to the class rather than an instance. Static methods can be called directly on the class without creating an instance.

    ```java
    public class MathOperations {
        static int add(int a, int b) {
            return a + b;
        }
    }
    ```

    - The **`add`** method can be called using **`MathOperations.add(5, 3)`** without creating an instance of **`MathOperations`**.
- **3. Static Blocks:**

    A static block is a block of code enclosed in curly braces **`{}`** and preceded by the **`static`** keyword. It's executed when the class is loaded into the memory.

    ```java
    public class InitializationExample {
        static {
            // Static block code
            System.out.println("This is a static block");
        }
    }
    ```

    - Static blocks are often used for static initialization, such as loading configuration files or initializing static variables.
- **4. Static Nested Classes:**

    A static nested class is a nested class that is declared as **`static`**. It can be instantiated without creating an instance of the outer class.

    ```java
    public class OuterClass {
        static class StaticNestedClass {
            // Code for static nested class
        }
    }
    ```

    - Instances of a static nested class are not tied to an instance of the outer class and can be created independently.

### **Metaphor:**

Think of the **`static`** keyword as a shared resource or a common space that all instances of a class can access. It's like a library that contains books (variables and methods) accessible to everyone without needing to check out a personal copy (create an instance).

Static methods are like public services in a city that you can access directly without having to own a building (object) yourself. Static variables are like bulletin boards where everyone can see and update information collectively.

---

## You will understand how to cast datatypes

- **1. Widening (Implicit) Casting:**

    Widening casting happens automatically when you assign a smaller datatype to a larger datatype.

    ```java
    int intValue = 42;
    double doubleValue = intValue; // Implicit casting from int to double
    ```

    - In this example, the **`int`** value is implicitly cast to a **`double`** because a **`double`** can represent a larger range of values than an **`int`**.
- **2. Narrowing (Explicit) Casting:**

    Narrowing casting requires explicit syntax and is used when you assign a larger datatype to a smaller datatype.

    ```java
    double doubleValue = 3.14;
    int intValue = (int) doubleValue; // Explicit casting from double to int
    ```

    - In this example, the **`double`** value is explicitly cast to an **`int`**. Be cautious, as this may result in loss of precision.
- **3. Casting Between Related Types:**

    Casting is also useful when working with related types, such as subclasses or interfaces.

    ```java
    class Animal {
        void makeSound() {
            System.out.println("Generic animal sound");
        }
    }

    class Dog extends Animal {
        void bark() {
            System.out.println("Woof!");
        }
    }

    public class Main {
        public static void main(String[] args) {
            Animal myAnimal = new Dog();
            ((Dog) myAnimal).bark(); // Explicit casting to access subclass-specific method
        }
    }
    ```

    - In this example, **`myAnimal`** is declared as an **`Animal`** but refers to a **`Dog`** instance. To access the **`bark`** method specific to the **`Dog`** class, explicit casting is required.

### **Metaphor:**

Think of casting like converting between different currencies. Widening casting is like converting from a smaller currency (e.g., cents) to a larger one (e.g., dollars) where you don't lose any precision. Narrowing casting is like converting from a larger currency to a smaller one, where you might lose precision, similar to rounding off decimals.

Casting between related types is like having a general employee badge (Animal) that also allows you to access a specific department (Dog). You need to explicitly show your department badge to enter and use department-specific facilities.

---

## You will be able to create constructors and invoke them to create objects

- **1. Default Constructor:**

    A default constructor is automatically created by Java if you don't define any constructor explicitly. It has no parameters and initializes the object with default values.

    ```java
    public class Car {
        // Default constructor
        public Car() {
            System.out.println("A new car is created with default values");
        }
    }
    ```

    - In this example, when you create a **`Car`** object, the default constructor is automatically called.

    ```java
    Car myCar = new Car(); // Output: "A new car is created with default values"
    ```

- **2. Parameterized Constructor:**

    You can define your own constructors with parameters to initialize object properties based on specific values.

    ```java
    public class Person {
        String name;
        int age;

        // Parameterized constructor
        public Person(String personName, int personAge) {
            name = personName;
            age = personAge;
            System.out.println("A new person is created with name: " + name + " and age: " + age);
        }
    }
    ```

    - When you create a **`Person`** object with the parameterized constructor:

    ```java
    Person newPerson = new Person("Alice", 25);
    // Output: "A new person is created with name: Alice and age: 25"
    ```

- **3. Chaining Constructors:**

    You can chain constructors within the same class using **`this()`** to avoid code duplication and ensure that common setup logic is centralized.

    ```java
    public class Book {
        String title;
        String author;

        // Parameterized constructor
        public Book(String bookTitle, String bookAuthor) {
            title = bookTitle;
            author = bookAuthor;
        }

        // Constructor chaining using this()
        public Book(String bookTitle) {
            this(bookTitle, "Unknown");
            System.out.println("A new book is created with title: " + title + " and author: " + author);
        }

    ```

    - In this example, the second constructor calls the first one using **`this()`** to set default values for unspecified parameters.

    ```java
    Book newBook = new Book("Java Fundamentals");
    // Output: "A new book is created with title: Java Fundamentals and author: Unknown"
    ```


### **Metaphor:**

Think of a constructor as a blueprint or a recipe for creating objects. When you build a house (create an object), you follow a blueprint (constructor) to set up the structure and initial state. The default constructor is like a standard blueprint, and a parameterized constructor is like a customizable blueprint where you provide specific details.

Chaining constructors is like assembling different parts of a product in an assembly line. Each constructor does its part, and by chaining them, you ensure a smooth and efficient manufacturing process.

---

## You will understand Special Classes in Java, including Object and String

- **1. Object Class:**

    The **`Object`** class is at the root of the Java class hierarchy. Every class in Java is a direct or indirect subclass of the **`Object`** class. It provides some fundamental methods that can be overridden by other classes.

    ```java
    public class CustomObject {
        // Fields, methods, and constructors specific to CustomObject

        @Override
        public String toString() {
            return "CustomObject's string representation";
        }

        @Override
        public boolean equals(Object obj) {
            // Custom logic for equality comparison
            // Return true if objects are equal, false otherwise
        }

        @Override
        public int hashCode() {
            // Custom logic for generating a hash code
            // Should be consistent with the equals method
            return 42;
        }
    }
    ```

    - The **`toString`** method provides a string representation of the object. When you print an object, Java implicitly calls its **`toString`** method.
    - The **`equals`** method is used to compare objects for equality. It's important to override this method when creating custom classes. By default, the **`equals`** method provided by the **`Object`** class compares object references, which means it checks whether two references point to the same memory location.

    ```java
    		Person person1 = new Person("Alice", 30); //Alice
        Person person2 = new Person("Alice", 30); //Some other Alice

        System.out.println(person1.equals(person2));
    		// Expected response since diff people = false,
    		// Actual response since same mem loc = true.
    ```

    - The **`hashCode`** method is used for hash-based collections. It's also crucial to override this method if your class is used in hash-based collections. The **`hashCode`** method should consistently return the same value for objects that are considered equal according to the **`equals`** method. This ensures that if two objects are equal, they will have the same hash code, which is crucial for the proper functioning of hash-based collections.

        ```java
        Map<Person, String> personMap = new HashMap<>();
        personMap.put(new Person("Alice", 30), "Employee");

        String role = personMap.get(new Person("Alice", 30));
        System.out.println(role);
        ```

        In a similar case as above, even though the **`Person`** objects have the same name and age, you may not get the expected result because the **`hashCode`** method is not overridden. The default **`hashCode`** implementation inherited from **`Object`** computes the hash code based on the memory address of the object, and different **`Person`** instances will likely have different hash codes. As a result, the **`get`** method may not find the associated value, and **`role`** could be **`null`**.

- **2. String Class:**

    The **`String`** class in Java represents a sequence of characters. It is widely used and comes with many built-in methods for string manipulation.

    ```java
    public class StringExample {
        public static void main(String[] args) {
            String str1 = "Hello";
            String str2 = new String("World");

            // Concatenation
            String result = str1 + ", " + str2; // "Hello, World"

            // Length
            int length = result.length(); // 12

            // Substring
            String substring = result.substring(7); // "World"

            // Comparison
            boolean isEqual = str1.equals(str2); // false

            // Searching
            int index = result.indexOf("World"); // 7
        }
    }
    ```

    - Strings in Java are immutable, meaning their values cannot be changed after creation. Operations on strings usually result in a new string.
    - The **`equals`** method in the **`String`** class is overridden to compare the content of two strings.
    - Various methods like **`length`**, **`substring`**, **`indexOf`**, etc., provide powerful tools for manipulating and extracting information from strings.

### **Metaphor:**

Think of the **`Object`** class as the universal base class, like a generic container that every class inherits from. It provides common methods that are essential for proper functioning in the Java environment.

The **`String`** class is like a versatile tool belt with many specialized tools for working with text. You can concatenate, compare, search, and manipulate strings effortlessly, making it a fundamental part of Java programming.

---

## You will understand the new keyword

- **Creating Objects with `new`:**

    When you want to use a class to create an actual instance or object, you use the **`new`** keyword followed by the class constructor.

    ```java
    // Creating an instance of the Person class
    Person john = new Person();
    ```

    - In this example, **`new Person()`** creates a new object of the **`Person`** class, and the reference to this object is stored in the variable **`john`**.
- **Allocating Memory:**

    Think of the **`new`** keyword as instructing Java to allocate memory on the heap for your object. The heap is like a big playground where objects are stored during the program's execution.

    ```java
    Person john = new Person();
    ```

    - Here, **`john`** is like the entry ticket to a specific location in the playground allocated for the **`Person`** object.
- **Constructor Invocation:**

    When you use **`new`**, you are implicitly calling the constructor of the class. The constructor initializes the object, setting its initial state.

    ```java
    public class Person {
        // Constructor
        public Person() {
            // Initialization code goes here
            System.out.println("A new person is created!");
        }
    }
    ```

    - The **`Person`** class has a constructor that prints a message when a new person is created.
- **Dynamic Object Creation:**

    The **`new`** keyword enables dynamic memory allocation, allowing you to create objects at runtime based on user input or other dynamic factors.

    ```java
    Scanner scanner = new Scanner(System.in);
    System.out.print("Enter the class name: ");
    String className = scanner.next();

    Object dynamicObject = Class.forName(className).newInstance();
    ```

    - In this example, the **`newInstance()`** method is used with the **`new`** keyword to dynamically create an object based on user input.

### **Metaphor:**

Think of the **`new`** keyword as a magic wand that brings objects to life in the world of your program. When you say **`new Person()`**, it's like conjuring a new person into existence, complete with a set of characteristics and behaviors.

The **`new`** keyword is like a chef's command to create a new dish. You describe what you want, and the kitchen (Java runtime) takes care of preparing it for you.

---

## You will understand how to use the List class

- **1. Importing the List Interface:**

    Before using the **`List`** interface, make sure to import it from the **`java.util`** package:

    ```java
    import java.util.List;
    ```

- **2. Creating a List:**

    You can create instances of classes that implement the **`List`** interface, such as **`ArrayList`** or **`LinkedList`**.

    ```java
    import java.util.ArrayList;
    import java.util.List;

    // Creating an ArrayList
    List<String> myList = new ArrayList<>();
    ```

- **3. Adding Elements:**

    Use the **`add`** method to add elements to the list. The elements are added to the end of the list.

    ```java
    myList.add("Apple");
    myList.add("Banana");
    myList.add("Orange");
    ```

- **4. Accessing Elements:**

    Access elements by their index using the **`get`** method. Indices start from 0.

    ```java
    String fruit = myList.get(1); // Retrieves "Banana"
    ```

- **5. Iterating Over the List:**

    You can use loops or enhanced for loops to iterate over the elements of the list.

    ```java
    for (String item : myList) {
        System.out.println(item);
    }
    ```

- **6. Removing Elements:**

    Remove elements by their index or value.

    ```java
    myList.remove(0); // Removes the element at index 0
    myList.remove("Banana"); // Removes the first occurrence of "Banana"
    ```

- **7. List Size:**

    Use the **`size`** method to get the number of elements in the list.

    ```java
    int size = myList.size(); // Returns the size of the list
    ```


### **Metaphor:**

Think of a **`List`** like a shopping list. It's a dynamic and ordered collection of items. You can add items to the list, check what's at a specific position, remove items, and know how many items are on the list.

Creating a **`List`** is like preparing an empty shopping cart (ArrayList or LinkedList) at the store. Adding items is like placing products in the cart, and removing items is like taking products out.

Iterating over a **`List`** is akin to going through each item on your shopping list one by one, checking them off as you go.

---

## You will understand Wrapper classes

- **1. Introduction to Wrapper Classes:**
    - **Purpose:**
        - Wrapper classes "wrap" primitive data types in an object so that they can be included in activities that require objects, like collections.
            - **List of Wrapper Classes:**
                - **`Byte`**, **`Short`**, **`Integer`**, **`Long`**, **`Float`**, **`Double`**, **`Character`**, **`Boolean`**
- **2. Autoboxing and Unboxing:**
    - **Autoboxing:**
        - Automatic conversion of a primitive data type to its corresponding wrapper class.

            ```java
            int primitiveInt = 42;
            Integer wrappedInt = primitiveInt; // Autoboxing
            ```

    - **Unboxing:**
        - Automatic conversion of a wrapper class object to its primitive data type.

            ```java
            Integer wrappedNumber = 10;
            int primitiveNumber = wrappedNumber; // Unboxing
            ```

- **3. Example Usage:**
    - **Working with Collections:**
        - Collections in Java typically work with objects, so using wrapper classes is common.

            ```java
            List<Integer> numbers = new ArrayList<>();
            numbers.add(5); // Autoboxing
            int retrievedNumber = numbers.get(0); // Unboxing
            ```

    - **Passing to Methods:**
        - Some methods may expect objects, and using wrapper classes facilitates this.

            ```java
            void processInteger(Integer value) {
                // Processing logic
            }

            int primitiveValue = 42;
            processInteger(primitiveValue); // Autoboxing
            ```


### **Metaphor:**

Think of wrapper classes as gift wrappers for your primitive data types. When you're working with collections, APIs, or methods that expect objects, you need to "wrap" your primitive values in a nice wrapper.

- **Autoboxing is like putting a gift in a box:**
    - You take a primitive value (the gift), and Java automatically puts it in a suitable wrapper class (the box) when needed.
- **Unboxing is like taking the gift out of the box:**
    - When you need to use the value, Java automatically takes it out of the wrapper, converting it back to a primitive type.

Imagine you're exchanging gifts (primitive values) with a friend who prefers everything nicely wrapped (expects objects). Autoboxing is the act of putting your gift in a beautiful box, and unboxing is your friend unwrapping and enjoying the gift.

---

## You will understand Exceptions and Errors and how to handle them

- **1. Exceptions and Errors:**
    - **Exceptions:**
        - Exceptions represent abnormal conditions or unexpected situations that occur during the execution of a program.
        - Examples: **`NullPointerException`**, **`ArrayIndexOutOfBoundsException`**, **`ArithmeticException`**.
    - **Errors:**
        - Errors represent serious issues that typically cannot be handled by the program, and they often lead to abnormal termination.
        - Examples: **`OutOfMemoryError`**, **`StackOverflowError`**.
- **2. Handling Exceptions:**
    - **`try`, `catch`, and `finally` Blocks:**
        - Use a **`try`** block to enclose code that might throw an exception.
        - Use a **`catch`** block to handle the exception if it occurs.
        - Use a **`finally`** block to ensure certain code (e.g., cleanup tasks) always executes, whether an exception occurs or not.

            ```java
            try {
                // Code that may throw an exception
            } catch (ExceptionType exception) {
                // Code to handle the exception
            } finally {
                // Code that always executes
            }
            ```

    - **Multiple `catch` Blocks:**
        - You can have multiple **`catch`** blocks to handle different types of exceptions.

            ```java
            try {
                // Code that may throw an exception
            } catch (NullPointerException e) {
                // Handle NullPointerException
            } catch (ArrayIndexOutOfBoundsException e) {
                // Handle ArrayIndexOutOfBoundsException
            } catch (Exception e) {
                // Handle any other exception
            }
            ```

    - **Throwing Exceptions:**
        - You can use the **`throw`** statement to explicitly throw an exception.

            ```java
            void checkValue(int value) {
                if (value < 0) {
                    throw new IllegalArgumentException("Value must be non-negative");
                }
            }
            ```


### **Metaphor:**

Think of exceptions as unexpected events that can happen during a journey. When you're traveling, you might encounter road closures (exceptions) or severe weather conditions (errors). Handling these situations involves having contingency plans, like taking alternative routes or changing your travel plans.

- **`try` block is like the main route:**
    - Your main code is in the **`try`** block, representing your primary route. If everything goes smoothly, you follow this route.
- **`catch` blocks are like detour signs:**
    - When an exception occurs, you take a detour by entering a **`catch`** block. Each **`catch`** block is like a different detour sign for handling specific types of exceptions.
- **`finally` block is like the cleanup crew:**
    - The **`finally`** block is where you put your cleanup crew. Whether you take a detour or not, the cleanup crew ensures that essential tasks are done before you continue your journey.
- **Throwing exceptions is like sounding an alarm:**
    - When something is fundamentally wrong or violates a condition (e.g., negative value), you sound an alarm by throwing an exception.

---

## You will be able to utilize the following keywords: super, this

- **1. `this` Keyword:**
    - **Purpose:**
        - The **`this`** keyword refers to the current instance of the class. It distinguishes instance variables from local variables when they share the same name.
    - **Usage:**
        - Used to access instance variables and methods within the current instance of the class.

            ```java
            public class MyClass {
                private int value;

                // Constructor using 'this'
                public MyClass(int value) {
                    this.value = value;
                }

                // Method using 'this'
                public void printValue() {
                    System.out.println("Value: " + this.value);
                }
            }
            ```


    **Metaphor:**

    Think of **`this`** as a self-reference. When you say **`this.value`**, you're saying "the value of this current object."

- **2. `super` Keyword:**
    - **Purpose:**
        - The **`super`** keyword is used to refer to the immediate parent class object. It is often used to call the parent class's methods or access its fields.
    - **Usage:**
        - Used to invoke the parent class's methods or access its fields.

            ```java
            public class Parent {
                public void display() {
                    System.out.println("Parent class");
                }
            }

            public class Child extends Parent {
                // Using 'super' to call the parent class method
                public void displayInChild() {
                    super.display();
                    System.out.println("Child class");
                }
            }
            ```


    **Metaphor:**

    Imagine a family tree where each class is like a generation. Using **`super`** is like acknowledging your parent's contribution before adding your own. It's a way of saying, "Let's not forget where we came from."

- **3. When to Use `this` and `super`:**
    - **`this`:**
        - Used to differentiate between instance variables and local variables in a class.
        - Used to invoke methods or access fields within the current instance.
    - **`super`:**
        - Used to invoke methods or access fields in the parent class.
        - Used to call the parent class's constructor from the child class.

### **Metaphor:**

Think of a class as a house. Each instance of the class (object) is like a room in that house.

- **`this` is like referring to something within the current room:**
    - If you're in the living room (current instance), saying **`this.tv`** refers to the TV in the living room.
- **`super` is like acknowledging something from the parent's room:**
    - If you're in your room (child class), saying **`super.parentBed`** refers to the bed in your parent's room (parent class).

---

## You will be able to describe Inheritance and Polymorphism

- **1. Inheritance:**
    - **Definition:**
        - Inheritance is a mechanism in OOP that allows a new class (subclass/derived class) to inherit attributes and behaviors from an existing class (superclass/base class).
    - **Key Terms:**
        - **Superclass/Base Class/Parent Class:** The existing class whose attributes and behaviors are inherited.
        - **Subclass/Derived Class/Child Class:** The new class that inherits from the superclass.
    - **Syntax:**
        - Use the **`extends`** keyword to establish an inheritance relationship.

            ```java
            public class Animal {
                // Attributes and behaviors of the Animal class
            }

            public class Dog extends Animal {
                // Additional attributes and behaviors specific to Dog
            }
            ```

    - **Metaphor:**
        - Think of inheritance like a family tree. The superclass is like a parent, and the subclass is like a child inheriting traits, such as eye color or height.
- **2. Polymorphism:**
    - **Definition:**
        - Polymorphism allows objects of different types to be treated as objects of a common type. It simplifies the way objects are manipulated, making code more generic and reusable.
    - **Types of Polymorphism:**
        - **Compile-Time Polymorphism (Method Overloading):**
            - Methods with the same name but different parameter lists.
        - **Run-Time Polymorphism (Method Overriding):**
            - Methods with the same signature in both the superclass and subclass.
    - **Example:**
        - Method Overriding

            ```java
            public class Animal {
                public void makeSound() {
                    System.out.println("Some generic sound");
                }
            }

            public class Dog extends Animal {
                @Override
                public void makeSound() {
                    System.out.println("Woof! Woof!");
                }
            }
            ```

    - **Metaphor:**
        - Consider polymorphism like a universal remote control. The same button on the remote (method name) can do different things depending on the device (object type) it is currently controlling.
- **3. Inheritance and Polymorphism Together:**
    - **Example:**

        ```java
        public class Shape {
            public void draw() {
                System.out.println("Drawing a shape");
            }
        }

        public class Circle extends Shape {
            @Override
            public void draw() {
                System.out.println("Drawing a circle");
            }
        }

        public class Square extends Shape {
            @Override
            public void draw() {
                System.out.println("Drawing a square");
            }
        }
        ```

    - **Metaphor:**
        - Think of a shape as a general concept. Inheritance is like creating specific shapes (Circle, Square) that inherit the ability to be drawn. Polymorphism is like using a single command (**`draw()`**) to draw different shapes.

### **Key Takeaways:**

- **Inheritance:**
    - Creates a hierarchy of classes.
    - Promotes code reuse and establishes an "is-a" relationship between classes.
- **Polymorphism:**
    - Allows objects of different types to be treated as objects of a common type.
    - Enhances code flexibility and reusability.

---

## You will be able to utilize all of the following Java keywords: final, abstract, private, protected, public

- **1. Access Modifiers:**

    ### **`public`**:

    - **Access:**
        - Public members are accessible from anywhere, both within and outside the class.
    - **Example:**

        ```java
        public class PublicExample {
            public int publicVariable;

            public void publicMethod() {
                // Code here
            }
        }
        ```


    ### **`private`**:

    - **Access:**
        - Private members are only accessible within the same class. They are not visible to outside classes.
    - **Example:**

        ```java
        public class PrivateExample {
            private int privateVariable;

            private void privateMethod() {
                // Code here
            }
        }
        ```


    ### **`protected`**:

    - **Access:**
        - Protected members are accessible within the same class, same package, and subclasses (even if they are in a different package).
    - **Example:**

        ```java
        public class ProtectedExample {
            protected int protectedVariable;

            protected void protectedMethod() {
                // Code here
            }
        }
        ```

- **2. Non-Access Modifiers:**

    ### **`final`**:

    - **Purpose:**
        - Applied to a class, method, or variable to indicate that it cannot be extended (for classes), overridden (for methods), or modified (for variables).
    - **Example:**

        ```java
        public final class FinalExample {
            final int constantVariable = 42;

            final void finalMethod() {
                // Code here
            }
        }
        ```


    ### **`abstract`**:

    - **Purpose:**
        - Applied to a class or method to indicate that it is incomplete and must be implemented by its subclasses (for classes) or overridden (for methods).
    - **Example:**

        ```java
        public abstract class AbstractExample {
            abstract void abstractMethod(); // No method body
        }
        ```


### **Metaphor:**

Think of access modifiers as security gates in a building:

- **`public`:**
    - Public areas are accessible to everyone. Anyone can enter and use these spaces.
- **`private`:**
    - Private areas are restricted. Only individuals inside that room or class have access. Outsiders are unaware of what's happening inside.
- **`protected`:**
    - Protected areas are accessible to a specific group. It's like a members-only room where certain people (subclasses) have access.

Now, consider non-access modifiers as characteristics of rooms:

- **`final`:**
    - A final room cannot be extended or changed. Once built, its structure remains unchanged.
- **`abstract`:**
    - An abstract room is incomplete. It's like having an outline or blueprint but no concrete implementation. It needs to be filled in by subclasses.

### **Key Takeaways:**

- **Access Modifiers:**
    - **`public`**: Accessible everywhere.
    - **`private`**: Restricted to the class.
    - **`protected`**: Accessible within the class, package, and subclasses.
- **Non-Access Modifiers:**
    - **`final`**: Prevents extension, overriding, or modification.
    - **`abstract`**: Requires implementation by subclasses.

---

## You will be able to describe Encapsulation and Abstraction

- **1. Encapsulation:**
    - **Definition:**
        - Encapsulation is the bundling of data (attributes) and methods (functions) that operate on the data into a single unit known as a class. It restricts access to some of the object's components, emphasizing the idea of information hiding.
    - **Key Concepts:**
        - **Attributes (Fields):** Data members of a class.
        - **Methods (Functions):** Operations that can be performed on the data.
    - **Example:**

        ```java
        public class BankAccount {
            private double balance; // Encapsulated attribute

            // Encapsulated method to deposit money
            public void deposit(double amount) {
                if (amount > 0) {
                    balance += amount;
                }
            }

            // Encapsulated method to get the balance
            public double getBalance() {
                return balance;
            }
        }
        ```

    - **Metaphor:**
        - Think of encapsulation like a treasure chest. The chest (class) holds valuable items (attributes) and has a lock on it. To interact with the items, you use specific methods (functions) that the chest provides. The inner workings of the chest are hidden, emphasizing security and controlled access.
- **2. Abstraction:**
    - **Definition:**
        - Abstraction is the process of simplifying complex systems by modeling classes based on the essential properties and behaviors they share. It involves focusing on the relevant details while ignoring unnecessary complexities.
    - **Key Concepts:**
        - **Abstract Classes:** Classes that cannot be instantiated and may contain abstract methods.
        - **Abstract Methods:** Methods without a body, to be implemented by concrete subclasses.
    - **Example:**

        ```java
        // Abstract class representing a shape
        public abstract class Shape {
            // Abstract method to calculate area
            public abstract double calculateArea();
        }

        // Concrete subclass implementing the abstract method
        public class Circle extends Shape {
            private double radius;

            // Constructor and other methods...

            @Override
            public double calculateArea() {
                return Math.PI * radius * radius;
            }
        }
        ```

    - **Metaphor:**
        - Imagine an art class where you're learning to paint. The concept of a "shape" is abstract—you're not painting a specific shape, but the idea of shapes in general. Abstracting away the details of each specific shape allows you to focus on common characteristics, like area calculation, that all shapes share.

    Here are the main purposes of abstract classes:

    1. **To House Abstract Methods**: Abstract classes can declare abstract methods, which are methods that have no implementation in the abstract class itself. These methods are meant to be defined (implemented) in concrete subclasses that inherit from the abstract class. Abstract methods provide a contract that subclasses must adhere to, ensuring that certain methods are implemented in a consistent way across different subclasses.
    2. **To Provide a Common Base**: Abstract classes often serve as a common base or template for related concrete classes. They can contain shared attributes and methods that are common to multiple subclasses. By placing common code in the abstract class, you can avoid code duplication and ensure a consistent structure among related classes.
    3. **To Prevent Direct Instantiation**: Abstract classes cannot be instantiated directly; they exist to be subclassed. This can be useful when you want to ensure that certain methods are implemented in subclasses before objects of those subclasses can be created. It helps enforce a specific structure in derived classes.
    4. **To Define Partial Implementations**: Abstract classes can provide partial implementations for some methods while leaving others abstract. This allows concrete subclasses to inherit common behavior while still requiring them to implement specific functionality.
    5. **To Define a Type**: An abstract class can be used to define a common type or interface for a group of related classes. This allows you to treat instances of different concrete subclasses uniformly through polymorphism, improving code flexibility and maintainability.
    6. **To Facilitate Code Extensibility**: Abstract classes can be extended by concrete subclasses, allowing you to extend and customize the behavior of existing classes without modifying their code directly. This supports the open-closed principle of software design.

    In summary, while abstract classes are commonly used to declare abstract methods and enforce method implementation in subclasses, they also serve as a mechanism for code reuse, structure definition, and enforcing design principles like encapsulation and inheritance. Abstract classes are an essential part of object-oriented programming and help create hierarchies of related classes with shared behavior and attributes.


### **Key Takeaways:**

- **Encapsulation:**
    - Bundling data and methods into a class.
    - Restricting access to certain components for information hiding.
    - Enhancing security and maintainability.
- **Abstraction:**
    - Modeling classes based on essential properties and behaviors.
    - Creating abstract classes with abstract methods.
    - Simplifying complex systems by focusing on relevant details.

These principles help developers design classes and systems that are modular, adaptable, and easy to understand. Encapsulation provides a protective barrier around the object's internal state, and abstraction simplifies the representation of complex concepts, making it easier to manage and extend the codebase.
