# Coding style
We are adopting notepad-plus-plus style and discipline. Please see [CONTRIBUTING.md](https://github.com/graysuit/notepad-plus-plus/edit/master/CONTRIBUTING.md) by notepad-plus-plus.

![stay clean](https://notepad-plus-plus.org/assets/images/good-bad-practice.jpg)



<table>
<tr><th>Description</th> <th>Good</th><th>Bad</th></tr>

<tr><td>Don't use Java-like braces</td><td>

```cpp
if ()
{
    // Do something
}
```

</td><td>

```cpp
if () {
    // Do something
}
```

</td></tr>


<tr><td>Leave one space before & after logical operators</td><td>

```cpp
if (a == 10 && b == 42)
```

</td><td>

```cpp
if (a==10&&b==42)
```

</td></tr>


<tr><td>Specify full class names before function</td><td>

```cpp
Class.foo(24);
```

</td><td>

```cpp
foo(24);
```

</td></tr>


<tr><td>Avoid non sensable variable names</td><td>

```cpp
var Msg = MessageBox.Show("Helloworld");
```

</td><td>

```cpp
var gugUT7T8yKHhg87Y = MessageBox.Show("Helloworld");
```

</td></tr>


<tr><td>Prefer alpahbets over special characters</td><td>

```cpp
if (not string.empty())
```

</td><td>

```cpp
if (string != "")
```

</td></tr>


<tr><td>Variable name should describe its identity</td><td>

```cpp
if (hours < 24 && minutes < 60 && seconds < 60)
```

</td><td>

```cpp
if (a < 24 && b < 60 && c < 60)
```

</td></tr>


<tr><td>Use correct markdown to show colorfull code</td><td>

```cpp
```cpp
int main()
{
    cout << "Helloworld";
}
\```

and for single line:
\`cout << "Helloworld";`
```

</td><td>

```cpp
int main()
{
    cout << "Helloworld";
}

cout << "Helloworld";
```

</td></tr>


<tr><td>Don't put non sense comments</td><td>

```cpp
//This code do xxxx
//This can xxxx as well but I prefer it give xxxx performance
```

</td><td>

```cpp
//Mighty Mighty Eagle Rescue me
//I'm person that loves eating pizza and washroom bath
```

</td></tr>



<tr><td>Use correct comments operator</td><td>

```cpp
//This is single comment

/*
These are multiple comments
These are multiple comments
These are multiple comments
These are multiple comments
*/
```

</td><td>

```cpp
/*
This is single comment
*/

//These are multiple comments
//These are multiple comments
//These are multiple comments
//These are multiple comments
```

</td></tr>



<tr><td>Prefer ease than simplicity to show better understandale code</td><td>

```cpp
var Message = "This is Message";
String str = "This is string";
Int integer = "This is integer";
```

</td><td>

```cpp
var m1 = "This is m1";String m2 = "This is m2";Int m3 = "This is m3";
```

</td></tr>


</table>
