---
title: How to see the code for every stage of the compilation process?
subtitle:
date: 2018-08-07
bigimg: [{src: "/img/postimg/", desc: "Coding"}]
tags: ["programming"]
---
## The Compilation Process in C/C++

Knowing how your code compiles can be very helpful when writing and debugging it.

Compiling a C/C++ program is a multi-stage process.

The complete compilation process in C/C++ can be split into four separate stages:  

  1. Preprocessing
  2. Compilation
  3. Assembly
  4. Linking

![Entire Compilation Process](/img/compilation.png)

By using appropriate compiler options, we can stop this process at any stage. These options are passed as command line parameters.

In the following examples, I will be using the **C++ programming language** to write the code and **g++ compiler** to compile it. However, these commands can be easily implemented with a program written in the **C programming language** and compiled in **gcc compiler**.

As an example, the code below is apt for understanding this.

```
/*
Name : div.cc

Program to check divisibility by 2 */

#include<iostream>

using namespace std;

int main()
{
	int x;

	cin >> x;

	if (x % 2 == 0)
	{
		cout << "Divisible" << endl;
	}

	else
	{
		cout << "Not Divisible" << endl;
	}
}
```
It is a simple program that asks the user for an input and expects an integer (int) type constant. It prints _Divisible_ on the screen if the number is divisible by 2 and _Not Divisible_ otherwise.

## Preprocessing
The C++ preprocessor copies the contents of the included header files into the source code file (#include), expands macros, and replaces constants defined using #define with their values. It also removes comments from the main code.

A new source file is created that contains code from our program as well as the header files and this is what is used as input to the further stages for the compilation to be declared complete.

We can stop at this stage and see the output by using **“-E”** flag in gcc or g++.

In g++:
`g++ -E div.cc`

In gcc:
`gcc -E div.c`

Output to a file using **“>”** or **“-o”** flag.

  - `g++ -E div.cc > div`
  - `g++ -E div.cc -o div`

The above commands will store the code in **.FILE** extension.

GNU recommends saving the preprocessed files with a **.i** or **.ii** extensions. It signifies that the code inside the file is not to be preprocessed and is to be sent directly for compilation.

![Preprocessed Code](/img/preprocess.JPG)

Our 21 line program is now 16,014 lines after preprocessing and all of that is just the header file inclusion (iostream.h) till line 15,996!

You can see the complete preprocessed file, **div.ii** - [here](/res/div.ii).

## Compilation
The preprocessed code is compiled into the assembly language for the target platform. It is in the form of assembly language for the target platform. The file extension is **.s**.


## References
 - Using the GNU Compiler Collection (GCC) - [gcc.gnu.org](https://gcc.gnu.org/onlinedocs/gcc/Overall-Options.html)
 - The C++ compilation process - [NIU](http://faculty.cs.niu.edu/~mcmahon/CS241/Notes/compile.html)
 - 15 Most Frequently Used GCC Compiler Command Line Options - [The Geek Stuff](https://www.thegeekstuff.com/2012/10/gcc-compiler-options/)
