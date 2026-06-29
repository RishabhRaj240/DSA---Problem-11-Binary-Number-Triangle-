# Binary Number Triangle Pattern in C++

A beginner-friendly C++ program that demonstrates pattern printing using nested loops.

This project generates a **Binary Number Triangle Pattern**, where each row contains alternating `1`s and `0`s. The starting value of each row depends on whether the row number is even or odd, making it an excellent exercise for learning nested loops, conditional statements, and pattern generation.

---

## 📌 Features

* Prints a Binary Number Triangle Pattern
* Uses nested `for` loops
* Demonstrates alternating binary values (`1` and `0`)
* Uses conditional logic to determine the starting value of each row
* Beginner-friendly implementation

---

## 🛠️ Technologies Used

* C++
* Standard Input/Output (`iostream`)

---

## 📂 Problem Statement

Given an integer `N`, print a binary triangle pattern where each row alternates between `1` and `0`.

### Example

For:

```txt id="zpx14i"
N = 5
```

Output:

```txt id="cmyt4v"
1
0 1
1 0 1
0 1 0 1
1 0 1 0 1
```

---

## 📸 Screenshot

<img width="1207" height="787" alt="Screenshot 2026-06-29 133805" src="https://github.com/user-attachments/assets/846b0dbd-c81e-4041-9e59-0ba9ebf01e9d" />

Example folder structure:

```txt id="gk0jpl"
project-folder/
│
├── main.cpp
├── README.md
└── screenshots/
    └── output.png
```

---

## 💻 Source Code

```cpp id="h8sv1q"
void nBinaryTriangle(int n) {
    int start = 1;

    for(int i = 0; i < n; i++) {

        if(i % 2 == 0)
            start = 1;
        else
            start = 0;

        for(int j = 0; j <= i; j++) {
            cout << start << " ";
            start = 1 - start;
        }

        cout << endl;
    }
}
```

---

## ▶️ How to Run

1. Compile the program:

```bash id="dy2kcm"
g++ main.cpp -o main
```

2. Run the executable:

```bash id="pcjlwm"
./main
```

3. Enter the value of `N`.

---

## 📸 Example Output

### Input

```txt id="ynjvrh"
4
```

### Output

```txt id="vszn7u"
1
0 1
1 0 1
0 1 0 1
```

---

## 📖 Learning Concepts

This project helps beginners understand:

* Nested loops
* Pattern printing
* Conditional statements (`if-else`)
* Modulus operator (`%`)
* Alternating binary sequences
* Algorithmic thinking

---

## 🔍 Pattern Explanation

The starting value of each row is determined by the row index:

* **Even row index (`i % 2 == 0`)** → Starts with `1`
* **Odd row index (`i % 2 != 0`)** → Starts with `0`

The following statement toggles the current value after every print:

```cpp id="n2rvaf"
start = 1 - start;
```

This changes:

* `1 → 0`
* `0 → 1`

As a result, each row prints alternating binary digits.

---

## ⏱️ Complexity Analysis

### Time Complexity

```txt id="plfwc3"
O(N²)
```

The nested loops perform approximately `N²` iterations.

### Space Complexity

```txt id="lzr1um"
O(1)
```

Only a few integer variables are used.

---

## 👨‍💻 Author

Developed as a beginner-friendly C++ practice project for learning nested loops, conditional statements, and binary pattern printing.
