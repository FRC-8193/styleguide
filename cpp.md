
# C++ Style Guide

This document defines the C++ style rules for our team’s projects.  
The goal: **readable, consistent code** that feels the same no matter who wrote it.

---

## Indentation & Spacing
- Use **2 spaces** per indent (no tabs).  
- **K&R braces**:  
  - Space after keywords:  
    ```cpp
    if (condition) {
      do_something();
    } else {
      do_something_else();
    }
    ```
  - Space before `{`.  
  - `else` sits on the same line as the closing `}`.  

---

## Naming Conventions
- **Functions, variables, namespaces** → `snake_case`  
  ```cpp
  int calculate_power(int base, int exponent);
  namespace robot_utils { ... }
  ```

* **Constants, enum values, macros** → `SCREAMING_SNAKE_CASE`

  ```cpp
  const int MAX_SPEED = 42;

  enum Direction {
    NORTH,
    EAST,
    SOUTH,
    WEST
  };
  ```
* **Types (classes, structs, enums, typedefs)** → `PascalCase`

  ```cpp
  class MotorController {
  public:
    void set_speed(int speed);
  };
  ```

---

## Classes & Access Control

* `public:`, `private:`, and `protected:` go on the **same indent level** as `class`.
* Class members are indented **inside** the access section.

```cpp
class Example {
public:
  Example();

  void do_something();

private:
  int value;
};
```

---

## General Guidelines

* Keep lines ≤ 100 chars where possible.
* Prefer modern C++ (smart pointers, `auto`, range-for) but avoid being “clever” at the cost of readability.
* Use `this` rather than implicit member access. (`this->do_stuff()` instead of just `do_stuff()`)
* Document *why*, not *what*. The code should explain *what*.

---

That’s it. Keep it simple. Consistency > perfection.
