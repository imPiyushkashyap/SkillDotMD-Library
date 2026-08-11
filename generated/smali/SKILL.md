---
name: smali
description: Use this skill when working with Smali, a bytecode manipulation framework for Android. Triggers when user mentions Smali or imports from it.
---

# Smali

## What this is
Smali is a bytecode manipulation framework for Android, allowing developers to reverse engineer, modify, and recompile Android applications. It provides a disassembly and assembly language for Android's dex format, making it easier to analyze and manipulate Android bytecode. Smali is often used for debugging, optimizing, and customizing Android apps.

## Installation
To install Smali, run the following command: `git clone https://github.com/JesusFreke/smali.git && cd smali && ./build.sh`

## Key concepts
Smali provides several key concepts for working with Android bytecode, including:
* `smali` and `smali.assemble`: The disassembler and assembler tools for converting between dex and smali code.
* `baksmali`: A tool for disassembling dex files into smali code.
* Classes and methods: Smali represents Android classes and methods using a syntax similar to Java.

Example:
```smali
.class public Lcom/example/MyClass;
.super Ljava/lang/Object;

.method public constructor <init>()V
    .registers 1
    invoke-direct {p0}, Ljava/lang/Object;-><init>()V
    return-void
.end method
```

## Correct usage patterns
When working with Smali, it's essential to follow proper usage patterns, such as:
* Using the correct syntax for defining classes and methods.
* Understanding the different types of registers and their uses.
* Properly handling exceptions and errors.

Example:
```smali
.method public static newInstance()Lcom/example/MyClass;
    .registers 1
    new-instance v0, Lcom/example/MyClass;
    invoke-direct {v0}, Lcom/example/MyClass;-><init>()V
    return-object v0
.end method
```

## Common mistakes to avoid
Common mistakes to avoid when working with Smali include:
* Incorrectly defining classes or methods, leading to compilation errors.
* Failing to handle exceptions and errors properly, resulting in runtime crashes.
* Misunderstanding the different types of registers and their uses.

## File and folder conventions
Smali files typically follow the standard Java package naming conventions, with each package represented as a separate folder. The `smali` and `smali.assemble` tools expect input and output files to be in the correct format, with `.smali` files containing the disassembled code and `.dex` files containing the compiled bytecode. Configuration files, such as `baksmali.cfg`, are typically located in the root of the project directory.