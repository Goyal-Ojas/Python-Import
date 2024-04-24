# Python-Import

Exercise 1 – Converting Code to Functions
In Python, functions are efficient ways to encapsulate blocks of code that can be reused, promote
modularity, and enhance the readability of your program. They allow you to break down complex tasks
into smaller, more manageable components, making your code more organized and maintainable.
You have the following code to turn into a function. The code below checks if the variable num is a prime
number or not (Note: A prime number is a natural number greater than 1 that has no positive divisors
other than 1 and itself). The first few prime numbers are 2, 3, 5, 7, 11, ...
Based on the above code, create a Python function named is_prime with a single positional argument
named num that determines if num is a prime number or not. Note you have to revise this code so that
your is_prime function will return the boolean True to the function caller (using the function return
statement) if the positional argument num is a prime number. Otherwise, it should return the boolean
False to the function caller.
To ensure the correctness of your function, you can run a few checks, such as is_prime(1), is_prime(5),
is_prime(6), etc. Print out these results and see if you can get correct answers.

Exercise 2 – Print vs Return
This isn’t really an exercise, just an important bit of reading (you don’t need to submit anything). Suppose
you have the following two functions:
Run this code in the python console. What happens when we call these functions?
It looks like they behave in exactly the same way. But they really don’t. Try this:
In the case of f1, the function, when evaluated, prints 3; then it returns the value None, which is printed by
the Python shell. In the case of f2, it doesn’t print anything, but it returns 3, which is printed by the Python
shell. Finally, we can see the difference here:
In the first case, the function doesn’t return a value, so there’s nothing to add to 1, and an error is generated.
In the second case, the function returns the value 3, which is added to 1, and the result, 4, is shown on the
screen. For just about everything we do, it will be returned values that matter, and printing will be used
only for debugging, or to give information to the user.
Print is very useful for debugging, helping you understand the state of your program at different points
during execution. It’s important to know that you can print out as many variables and strings as you want
in one line, when they are separated by commas. This allows you to display relevant information
simultaneously. Using print within loops is particularly useful for tracking variables' values in each iteration,
aiding in identifying potential issues and monitoring program flow. Moreover, print statements can be
employed to observe intermediate values in complex calculations, providing valuable insights for
troubleshooting. Additionally, you can utilize print to measure the time taken to execute specific code blocks,
aiding in performance optimization and identifying potential bottlenecks.
Try this:
The expected output is
It shows that drawing 100 random variables from a normal distribution will only take about 0.0002 seconds!

Exercise 3 – Comprehensions
You have been provided the following conversion formulas between Fahrenheit and Celsius:
Fahrenheit to Celsius conversion: 𝐂𝐞𝐥𝐬𝐢𝐮𝐬 = (𝐅𝐚𝐡𝐫𝐞𝐧𝐡𝐞𝐢𝐭 − 𝟑𝟐) × 𝟓
𝟗
Celsius to Fahrenheit conversion: 𝐅𝐚𝐡𝐫𝐞𝐧𝐡𝐞𝐢𝐭 = 𝐂𝐞𝐥𝐬𝐢𝐮𝐬 × 𝟗
𝟓 + 𝟑𝟐
Based on the formula above, do the following:
• Create a Python dictionary comprehension statement that converts integer Celsius degrees ranging
from 0 to 35 (including both 0 and 35) to Fahrenheit.
• You will store your dictionary comprehension statement in a variable named A.
▪ The key for your dictionary comprehension would be the range of Celsius degrees from 0 to
35.
▪ The values for your dictionary comprehension would be the converted value to Fahrenheit from
your keys that have the corresponding Celsius value.
▪ Ensure your converted values are rounded up to 1 decimal value (you may use the round()
function).
▪ Your dictionary comprehension will need to use one for loop with a range() statement that
includes the number 0 (zero) through and including the number 35 in increments of 1.
• You will then need to print your dictionary A to the Python console resulting in the sample output
below.
Expected output:

Exercise 4 – Temperature Convertor
Create a Python function that achieves temperature conversions, as follows:
• Create a function named convert_temp with one positional argument named degrees; and another
keyword argument named cnv_type with a default value of 'ftoc'.
• Inside your new function, you will need to check for the type of variable being passed in your
positional argument named degrees.
▪ If the variable type is an int or a float, you will proceed with the required degrees conversion.
▪ If the variable type is not an int or a float, your function will use the return statement to provide
a value of −2 to the function caller and will not do any further conversions.
▪ HINT: Let’s say that you have a Python variable named x. To check if this variable x is an int
type, you can use either isinstance(x, int) or type(x) == int. Similarly, you can use isinstance(x,
float) or type(x) == float to check if x is a float type. Lookup the Python built-in isinstance()
function.
• After ensuring that the variable type of your positional argument named degrees is either int or
float, you are ready to do the conversions. If cnv_type is passed the value 'ftoc', you will convert the
input degrees (= your function positional argument) to Celsius using the correct formula provided
in the above question. If the argument cnv_type is passed the value 'ctof', you will convert the input
degrees to Fahrenheit. The converted degrees (by your formula) will use the return statement to
provide its converted value to the function caller.
• Ensure all of your conversion values are rounded up to 1 decimal for both options ('ftoc' and 'ctof').
• If you pass a positional argument with values other than 'ftoc' or 'ctof', your function will use the
return statement to provide a value of −1 to the function caller and will not do any further
conversions.
Correctness Checks: If you were to run the following function calls, your output should be as follows:

Exercise 5 - Sort by Selected Key
The following code sorts a list of tuples named tups using the second element of each tuple as the sort key.
As shown in the code, this is done by setting the argument key of the sorted() function as a lambda function,
which takes an input argument named x and returns x[1] (= second element of x).
The above code outputs the following (sorted list of tuples) to the console:
Now write a function that sorts a list of dictionaries, as follows:
• Create a function named sort_by_selected_key with two positional arguments named dicts and
keyname. The function will allow users to choose which key (using the positional argument keyname)
to use for sorting the input list of dictionaries.
• Sort the list of dictionaries dicts by the keyname in ascending order. Accomplish this by using the
sorted() function with its argument key set as a lambda function. This lambda function should take a
dictionary as its input and return the value for the keyname (this will be similar to the lambda function
in the above example code with the list of tuples).
• Use the function return statement to provide the newly sorted list of dictionaries to the function caller
and your function will not proceed any further.
Correctness Checks: If you were to run the following function calls, your output should be as follows:
# Example list of dictionaries

Exercise 6 – Python Class
You are provided with the following Python class definitions:
With respect to the code above, answer the following questions. Write your answers as Python comments.
1. What are the attributes of the class Fish?
2. What are the methods of the class Fish?
3. Which class is the parent class?
4. Which class is the child class (= subclass)?
5. In Object-Oriented Programming (OOP) terms, what is the code in line 14 doing?
6. Briefly explain how the code in line 15 and line 20 each got their console output. HINT: Your
explanation should include the __init__ constructor method.
7. In you own words using OOP terms, briefly explain how the code in line 21 works and got its
console output even though there is no swim() method defined within the BlueTang class.
