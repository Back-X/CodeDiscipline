# Coding style
We are adopting notepad-plus-plus style and discipline. Please see [CONTRIBUTING.md](https://github.com/graysuit/notepad-plus-plus/edit/master/CONTRIBUTING.md) by notepad-plus-plus.

![stay clean](https://notepad-plus-plus.org/assets/images/good-bad-practice.jpg)



#### GENERAL

1. ##### Do not use Java-like braces.

  * ###### Good:
    ```cpp
    if ()
    {
        // Do something
    }
    ```

  * ###### Bad:
    ```cpp
    if () {
        // Do something
    }
    ```

2. ##### Use tabs instead of white-spaces (we usually set our editors to 4 white-spaces for 1 tab, but the choice is up to you).


3. ##### Always leave one space before and after binary and ternary operators.

  * ###### Good:
    ```cpp
    if (a == 10 && b == 42)
    ```

  * ###### Bad:
    ```cpp
    if (a==10&&b==42)
    ```

4. ##### Only leave one space after semi-colons in "for" statements.

  * ###### Good:
    ```cpp
    for (int i = 0; i != 10; ++i)
    ```

  * ###### Bad:
    ```cpp
    for(int i=0;i<10;++i)
    ```

5. ##### Function names are not separated from the first parenthesis.

  * ###### Good:
    ```cpp
    foo();
    myObject.foo(24);
    ```

  * ###### Bad:
    ```cpp
    foo ();
    ```

6. ##### Keywords are separated from the first parenthesis by one space.

  * ###### Good:
    ```cpp
    if (true)
    while (true)
    ```

  * ###### Bad:
    ```cpp
    if(myCondition)
    ```

7. ##### Use the following indenting for "switch" statements:

  ```cpp
  switch (test)
  {
      case 1:
      {
          // Do something
          break;
      }
      default:
          // Do something else
  } // No semi-colon here
  ```

8. ##### Avoid magic numbers.

  * ###### Good:
    ```cpp
    if (foo < I_CAN_PUSH_ON_THE_RED_BUTTON)
        startThermoNuclearWar();
    ```

  * ###### Bad:
    ```cpp
    while (lifeTheUniverseAndEverything != 42)
        lifeTheUniverseAndEverything = buildMorePowerfulComputerForTheAnswer();
    ```

9. ##### Prefer enums for integer constants.

10. ##### Use initialization with curly braces.

  * ###### Good:
    ```cpp
    MyClass instance{10.4};
    ```

  * ###### Bad:
    ```cpp
    MyClass instance(10.4);
    ```

11. ##### Always use `empty()` for testing if a string is empty or not.

  * ###### Good:
    ```cpp
    if (not string.empty())
    ...
    ```

  * ###### Bad:
    ```cpp
    if (string != "")
    ...
    ```


12. ##### Always use `C++ conversion` instead of `C-Style cast`. Generally, all the conversion among types should be avoided. If you have no choice, use C++ conversion.

  * ###### Good:
    ```cpp
    char aChar = static_cast<char>(_pEditView->execute(SCI_GETCHARAT, j));
    ```

  * ###### Bad:
    ```cpp
    char aChar = (char)_pEditView->execute(SCI_GETCHARAT, j);
    ```

13. ##### Use `!` instead of `not`, `&&` instead of `and`, `||` instead of `or`.

  * ###### Good:
    ```cpp
    if (!::PathFileExists(dir2Search))
    ```

  * ###### Bad:
    ```cpp
    if (not ::PathFileExists(dir2Search))
    ```

#### NAMING CONVENTIONS

1. ##### Classes uses Pascal Case

  * ###### Good:
    ```cpp
    class IAmAClass
    {};
    ```

  * ###### Bad:
    ```cpp
    class iAmAClass
    {};
    class I_am_a_class
    {};
    ```

2. ##### Methods & method parameters use camel Case

  ```cpp
  void myMethod(uint myVeryLongParameter);
  ```

3. ##### Member variables

Any member variable name of class/struct should be preceded by an underscore.

  ```cpp
  public:
      int _publicAttribute;
  private:
      int _pPrivateAttribute;
      float _pAccount;
  ```

4. ##### Always prefer a variable name that describes what the variable is used for.

  * ###### Good:
    ```cpp
    if (hours < 24 && minutes < 60 && seconds < 60)
    ```

  * ###### Bad:
    ```cpp
    if (a < 24 && b < 60 && c < 60)
    ```



#### COMMENTS

1. ##### Use C++ comment line style than C comment style.

  * ###### Good:
    ```
    // Two lines comment
    // Use still C++ comment line style
    ```

  * ###### Bad:
    ```
    /*
    Please don't piss me off with that
    */
    ```



#### BEST PRACTICES

1. ##### Use C++11/14/17 whenever it is possible

2. ##### Use C++11 member initialization feature whenever it is possible

  ```cpp
  class Foo
  {
      int value = 0;
  };
  ```

3. ##### Prefer Pre-increment:
  ```cpp
  ++i
  ```

 ##### **Over Post-increment:**
  ```cpp
  i++
  ```
  (It does not change anything for built-in types but it would bring consistency)

4. ##### Avoid using pointers. Prefer references. You might need the variable to be assigned a NULL value: in this case the NULL value has semantics and must be checked. Wherever possible, use a SmartPtr instead of old-school pointers.

5. ##### Avoid using new if you can use automatic variable. However, avoid `shared_ptr` as much as possible. Prefer `unique_ptr` instead.

6. ##### Don't place any "using namespace" directives in headers.

7. ##### Compile time is without incidence. Increasing compile time to reduce execution time is encouraged.

8. ##### Code legibility and length is less important than easy and fast end-user experience.
