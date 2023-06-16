### Simple Calculator

```
first number = get user input
if first number not numeric then print warning
second number = get user input
if second number not numeric then print warning
operation = get user input
lower case the operation for case insensitive
if operation is + or "add" then
    print first number + second number
otherwise if operation is - or "sub" then
    print first number - second number
otherwise if operation is * or "mul" then
    print first number * second number
otherwise if operation is / or "div" then
    print first number / second number
otherwise
    print warning
```

### Variables and data types

```
int n1 = 32;
long n2 = 32l;

float f1 = 33.0f;
double f2 = 33.0;

char a = 'a';
bool isAdmin = false;

string greet = "Hello";
```

### Operators

```
n1 + n2;
n1 - n2;
n1 * n2;
n1 / n2;
n1 % 2;

n1++;
n1--;
```

### Print to console

```
Console.WriteLine("Hello, World");
```

### User input

```
string? input = Console.ReadLine();
```

### String to number

```
string? input = Console.ReadLine();
int converted;
bool ok = int.TryParse(input, out converted);

// converted is zero or parsed int
```

### Compare Strings

```
string txt1 = "some text";
string txt2 = "another text";

bool isEqual = txt1.Equals(txt2, StringComparison.OrdinalIgnoreCase);
```

### More Strings

```
// Format
string result = string.Format("{0} {1}", txt1, txt2);

// Length
result.Length

// Substring
result.Substring(2, 6);

// Replace
result.Replace("text", "TEXT");

// Lower Upper
result.ToLower();
result.ToUpper();

// Empty String
string empty = string.Empty;
```

### Conditional Statements

```
if (condition)
{
  // some stuff
}
else if (condition)
{
  // some stuff
}
else
{
  // some stuff
}

switch(expression)
{
  case value1:
    // some stuff
    break;
  case value2:
    // some stuff
    break;
  default:
    // some stuff
}

```

### Logical Operators

```
AND -> &&
OR  -> ||
NOT -> !

if (condition1 && condition2)
{
  // some stuff
}
```

### Objects and Classes

- Class: template that allow create new types
- Object: instance of these class

```
public class Person
{

}
```

### Methods

Function: set of statements that perform a process.
Method: Function inside a class.

```
public class Person
{
  private int _age = 33;

  public int getAge()
  {
    return _age;
  }

  public void setAge(int age)
  {
    _age = age;
  }
}

```

### Create objects

```
Person p = new Person();
p.setAge(35);
Console.PrintLine(p.getAge());
```

### Static methods

Static methods are class level.

```
public class Person
{
  // ...
  static public void greet()
  {
    Console.WriteLine("Hello World");
  }
}

Person.greet();  // dont need instanciate
```

### Throw Exceptions

```
string input = Console.ReadLine();
int parsedInt;
bool successParse = int.TryParse(input, out parsedInt);
if (!succesParse)
{
  throw new Exception("Conversion is not successful.");
}
```

### Handle Exceptions

```
try
{
    string input = Console.ReadLine();
    int parsedInt;
    bool successParse = int.TryParse(input, out parsedInt);
    if (!succesParse)
    {
      throw new Exception("Conversion is not successful.");
    }
} catch (Exception ex) {
    Console.WriteLine("There was an error: {0}", ex.Message);
} finally {
    // Do stuff even if throw
}

```
