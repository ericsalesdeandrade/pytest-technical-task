
# How to test Python Code with Pytest

Are you a Python programmer looking to level up your testing game and supercharge your development process? 

If you aren't familiar with the most obvious and popular choice to achieve this, then let me introduce you to Pytest. 

This powerful and intuitive testing framework for Python is the secret sauce to writing clean, concise, and reliable test cases. 

With automatic test discovery, easy-to-read syntax, and an array of built-in assertions, Pytest makes writing tests a breeze.

In this article, we'll touch upon the many benefits of Pytest and why it is so popular. From setting up your environment to writing tests that cover all your code, we've got you covered. Let's dive in:


## 1. What is Pytest?

Pytest is a full-featured, open-source testing framework that allows developers to write test functions using simple and expressive syntax. 

It aims to make writing tests as easy as possible, encouraging developers to focus on the actual testing logic rather than boilerplate code. 

Integrating Pytest into your code allows you to identify and fix bugs before they become problems, saving you time and effort in the long run.

Let's look at why Pytest is a fan favourite in the Python ecosystem.

## 2. Advantages of Pytest
It is the little things that Pytest provides that have altogether made it revolutionary. From quick debugging of code to providing extensibility, Pytest has much to offer:

 1. Pytest can execute multiple test cases simultaneously,
    reducing the execution duration.
 2. Pytest can skip a test method from a group of test methods during execution.
 3. Pytest is free and does not have licensing costs.
 4. Pytest provides detailed test reports with clear indications of
    passed, failed, and skipped tests and timing information.
 5. Pytest can skip a few test methods out of all the test
    methods during test execution.
 6. Pytest can be used to test a wide range of applications on API,
    database, etc.

##  Project Set Up
Here's a small guide to show you how to test a code in Pytest.

### Prerequisites
To follow this guide, you should have the following:

-   Python 3.10 or higher.
    
-   Basic understanding of Python's syntax and functions

- Pytest

If you don't have Pytest, then you need to install it first. You can install Pytest using pip, the Python package manager:

    pip install pytest

### Writing test functions
Pytest expects our tests to be located in files whose names begin with `test_` or end with `_test.py`. So go ahead and create a Python file, for example, `area_calculator.py`, and write the following code:

    def square(side: float) -> float:
    """
    Calculate the area of a square
    """
    return round(side * side, 2)
    

    def rectangle(length: float, breadth: float) -> float:
        """
        Calculate the area of a rectangle
        """
        return round(length * breadth, 2)
        

    def circle(radius: float) -> float:
        """
        Calculate the area of a circle
        """
        return round(3.14 * radius * radius, 2)
    
    
    def triangle(base: float, height: float) -> float:
        """
        Calculate the area of a triangle
        """
        return round(0.5 * base * height, 2)

The above code includes a set of functions that calculate the area of different geometric shapes. These functions take specific parameters related to each shape and return the calculated area.

In the same directory where we saved the above file, add another script for the tests named `test_area_calculator.py`.

    from src.area_calculator import (
    square, 
    rectangle, 
    circle, 
    triangle
    )
    
    def test_square():
        """
        Test square function
        """
        assert square(2) == 4
        assert square(3) == 9
        assert square(4) == 16
    
    def test_rectangle():
        """
        Test rectangle function
        """
        assert rectangle(2, 3) == 6
        assert rectangle(3, 4) == 12
        assert rectangle(4, 5) == 20
    
    def test_circle():
        """
        Test circle function
        """
        assert circle(2) == 12.56
        assert circle(3) == 28.26
        assert circle(4) == 50.24
    
    def test_triangle():
        """
        Test triangle function
        """
        assert triangle(2, 3) == 3
        assert triangle(3, 4) == 6
        assert triangle(4, 5) == 10


The code defines several test functions, each targeting one of the area calculation functions. 

Within each test function, there are multiple `assert` statements. Each `assert` statement checks whether the actual result returned by the corresponding area calculation function matches the expected result.

Similarly, you can write more tests for the other functions. You can find the complete example in  [this GitHub repository](https://github.com/ericsalesdeandrade/pytest-technical-task/blob/master/src/area_calculator.py).

To run tests, open a terminal and run the following command from the folder where there are the two scripts:

    pytest

## Conclusion
Congratulations! You have just learned how to add tests to your Python code using Pytest! Embracing Pytest as your testing framework ensures the reliability and longevity of your Python code! 

If you have any ideas for improvement or like me to cover any topics, please comment below or send me a message via  [Twitter](https://twitter.com/ericsda),  [GitHub](https://github.com/ericsalesdeandrade)  or  [Email](mailto:sdaeric19@gmail.com).

Till the next time… Cheers!

## Additional Reading

[How to write and report assertions in tests - pytest documentation](https://docs.pytest.org/en/7.1.x/how-to/assert.html%20%22https://docs.pytest.org/en/7.1.x/how-to/assert.html)