# **(Splash Screen) Compilation with Custom Icon**

## **Overview**

This guide explains how to compile a C program into an executable (`.exe`) with a custom icon.

## **Prerequisites**

Ensure you have the following files in your project directory:

- **`splashScreen.c`**: Your main C source file.
- **`bangla_keyboard.ico`**: Your custom icon file.
- **`resource.h`**: Resource header file.
- **`resources.rc`**: Resource script file.

## **Compilation Steps**

### 1. Compile the Resource File

Run the following command:

```bash
windres resources.rc -o resource.o
```
## Expected Result:

- **`resource.o`**: that contains machine code.

### 2. Generated Executable File (.exe)
```bash
gcc splashScreen.c resource.o -o splashScreen.exe -mwindows
```
#### Behavior of Flags
> **`-mwindows:`** Tells GCC to create a Windows GUI application. This means that the application will not have a console window attached to it when run.

## Expected Result:

- **`splashScreen.exe`**: Executable File (.exe)

### 3. Run Executable File (.exe)

```bash
splashScreen.exe
```
OR
```bash
./splashScreen.exe
```
