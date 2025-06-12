# What Even is Actual Python?

Actual Python is a practical, no-nonsense course designed to take you from
zero programming experience to confidently developing _real_ programs using
the Python programming language.

## What is Programming?

Programming is basically the process of making a computer (or most digital devices, really) do what you want (mostly). You're probably wondering how that's different from changing the wallpaper on your phone or adjusting the brightness of your laptop. After all, you're giving the device an instruction, and it responds. But there's a key difference.

The difference is that when you change your wallpaper or adjust the screen brightness, you're using a program to further configure your device, not creating the program that makes those options possible in the first place.

A programmer already wrote the instructions that make those features work. They told the device how to respond when you tap certain buttons, where to find image files, and how to display them on the screen. So when you change a setting, you're following a path that has already been programmed. Writing those instructions in the first place? That’s programming!

## What’s a Program?

The previous section explains that programming is about giving instructions to a computer. A program is simply a collection of those instructions, written in a way the computer understands. It tells the computer exactly what to do, step by step, to complete a specific task.

## What is a Programming Language?

Here’s the interesting bit. Computers don’t actually understand human-languages like English or Igbo. They understand a very simple language called **machine code**.

### Machine Code

Machine code is commonly referred to as **binary** because it consists entirely of `1`s and `0`s. These symbols represent the basic on and off states of electrical signals inside a computer.

Machine code is obviously not a human-friendly language. It's also very difficult to read and understand machine code. So, to make programming easier some smart developers have created more human-friendly languages that are converted to binary code that computers understand.

These human-friendly languages are called _programming languages_ and they're broadly classified into two categories: low-level languages and high-level languages.

### Low-level Programming Languages

Low-level programming languages are very close to machine code but they're slightly easier to read and write by hand.

One of the most well-known low-level programming languages is called Assembly. If, for example, we want to print `Hello Python!` to the screen on a 64-bit Linux system, we might write the following Assembly program for it.

```asm
section .data
    message db "Hello Python!", 0xA
    message_len equ $ - message

section .text
    global _start

_start:
    mov     eax, 1
    mov     edi, 1
    mov     rsi, message
    mov     edx, message_len
    syscall

    mov     eax, 60
    xor     edi, edi
    syscall
```

Programs written in low-level languages are usually very powerful, fast, and efficient. However, writing programs in such languages isn't very easy for most applications. That's because, among other things:

- Even the simplest tasks such as printing `Hello Python!` to the screen requires many lines of code.
- Developing such programs is time-consuming.
- Small mistakes in such programs can result in very serious issues while using them.
- They're not portable. So, you have to write separate instructions for each platform (e.g. Windows, Linux, Android, iOS etc.).

### High-level Programming Languages

While low-level programming languages are hard to work with, people can easily read, write, and maintain programs written in high-level programming languages. This is so because, unlike high-level programming languages, low-level programming languages:

- Are less verbose
- Have a human-like vocabulary:
- Are more portable across platforms. The same program might be able to run in your web browser, your computer, and even your smart watch.
- Are easy to maintain

For the above reasons (and others), high-level programming languages are used for most modern software development, from websites to mobile applications, and even artificial intelligence.

But before a computer can actually run programs written in high-level programming languages, such programs still need to be translated into machine code (those `1`s and `0`s it understands). This translation happens in two main ways:

- **Compilation**: The entire program is translated into machine code before it runs. This usually makes it faster and more efficient.
- **Interpretation**: The program is translated and executed line by line while it runs. This makes it easier to test and debug, but often a bit slower.

Some high-level languages (like `C` and `Rust`) are compiled, some (like `BASH`) are interpreted, and others (like `Python` and `JavaScript`) can be compiled or interpreted.

## Python Programming Language

Python is a high-level language. It's designed to be easy to read and write, making it great for beginners and expert programmers. People use Python to build websites, automation tools, tools used for statistics, and even AI.

Python is primarily an **interpreted programming language**. To ensure a Python program is portable (i.e., can run on any platform), Python actually goes through an extra step when you run a program.

First, it compiles the program to **bytecode** which is a simplified set of instructions that are not quite machine code, but not high-level either.

Next, the compiled bytecode is then **interpreted** by the **Python Virtual Machine**, which runs the program.

This mix gives Python the flexibility of an interpreted language, while still benefiting from the structure of compilation behind the scenes.

For example, if we wanted to print the same `Hello Python!` text to the screen, using Python programming language, we will only need to run the following command:

```python
print("Hello Python!")
```
