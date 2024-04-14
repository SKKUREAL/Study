## 14.14 — Introduction to the copy constructor

```cpp
#include <iostream>

class Fraction
{
private:
    int m_numerator{ 0 };
    int m_denominator{ 1 };

public:
    // Default constructor
    Fraction(int numerator=0, int denominator=1)
        : m_numerator{numerator}, m_denominator{denominator}
    {
    }

    void print() const
    {
        std::cout << "Fraction(" << m_numerator << ", " << m_denominator << ")\n";
    }
};

int main()
{
    Fraction f { 5, 3 };  // Calls Fraction(int, int) constructor
    Fraction fCopy { f }; // What constructor is used here?

    f.print();
    fCopy.print();

    return 0;
}
```

You might be surprised to find that this program compiles just fine, and produces the result:

Fraction(5, 3)
Fraction(5, 3)

Let’s take a closer look at how this program works.

The initialization of variable `f` is just a standard brace initialization that calls the `Fraction(int, int)` constructor.

But what about the next line? The initialization of variable `fCopy` is also clearly an initialization, and you know that constructor functions are used to initialize classes. So what constructor is this line calling?

The answer is: the copy constructor.

### The copy constructor

A **copy constructor** is a constructor that is used to initialize an object with an existing object of the same type. After the copy constructor executes, the newly created object should be a copy of the object passed in as the initializer.

