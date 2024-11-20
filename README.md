# Employee Class

This project involves implementing a simple `Employee` class in Java. The class encapsulates the properties and behaviors of an employee, including their name and salary. It provides methods to access the employee's name, salary, and to raise their salary by a specified percentage.

## Objective

Create a Java program that:

- Defines an `Employee` class with instance variables for the employee's name and salary.
- Implements a constructor to initialize the employee objects.
- Provides methods to retrieve the employee's name, salary, and to raise the salary by a percentage.

## Employee Class Implementation

### Class Definition

The `Employee` class should include:

- **Instance Variables:**
    - `String employeeName`
    - `double currentSalary`

- **Constructor:**
  ```java
  public Employee(String employeeName, double currentSalary)
  ```

- **Methods:**
    - `public String getName()`: Returns the name of the employee.
    - `public double getSalary()`: Returns the current salary of the employee.
    - `public void raiseSalary(double byPercent)`: Raises the employee's salary by a specified percentage.

### Example Usage

Here's an example of how to use the `Employee` class:

```java
Employee harry = new Employee("Hacker, Harry", 50000);
harry.raiseSalary(10); // Harry gets a 10 percent raise
```

### Example Implementation

```java
public class Employee {
    private String employeeName;
    private double currentSalary;

    // Constructor
    public Employee(String employeeName, double currentSalary) {
        this.employeeName = employeeName;
        this.currentSalary = currentSalary;
    }

    // Get employee name
    public String getName() {
        return employeeName;
    }

    // Get employee salary
    public double getSalary() {
        return currentSalary;
    }

    // Raise salary by a percentage
    public void raiseSalary(double byPercent) {
        currentSalary += currentSalary * byPercent / 100;
    }
}
```

### EmployeeTest Class

Create a test class named `EmployeeTest` to test all methods of the `Employee` class.

```java
public class EmployeeTest {
    public static void main(String[] args) {
        Employee harry = new Employee("Hacker, Harry", 50000);
        
        System.out.println("Employee Name: " + harry.getName());
        System.out.println("Current Salary: " + harry.getSalary());
        
        harry.raiseSalary(10); // Harry gets a 10 percent raise
        
        System.out.println("New Salary after raise: " + harry.getSalary());
    }
}
```

## Hints

- Ensure that the constructor initializes the instance variables correctly.
- Use the `getName()` and `getSalary()` methods to retrieve the respective values.
- The `raiseSalary()` method should correctly calculate the new salary based on the percentage provided.

## Notes

- Document your code with comments to explain the functionality of each method.
- Test the program with various inputs to ensure accuracy and robustness.

Happy coding! 🎉