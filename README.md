# 🔧 Compiler-in-C++

A simple but powerful compiler written in C++ for a custom programming language that supports variables, loops, conditionals, arithmetic expressions, input/output, and comments. The project features a complete frontend with a scanner and parser, and compiles code into assembly-like instructions which can be interpreted.

---

## 🚀 Features

- ✅ Lexical analysis (Scanner)
- ✅ Syntax analysis (Parser)
- ✅ Simple custom language with:
  - 🧮 Variables and arithmetic expressions
  - 🔁 Loops (`iter`)
  - 🔀 Conditionals (`if`)
  - 🖨️ Input/Output (`read`, `print`)
  - ❗Comments using `! ... !`
- ✅ Code generation to `.asm`-like output
- ✅ Interpreter to run generated code

---

## 📁 Project Structure

```
Compiler-in-cpp/
├── src/                # Source code files (compiler logic)
├── examples/           # Sample programs in custom language
├── bin/                # Compiled binaries (comp, asmb)
├── include/            # Header files
├── tests/              # Optional: unit tests
├── Makefile            # Build automation
├── README.md
└── LICENSE
```

---

## ⚙️ Build Instructions

### 🔨 Prerequisites
- C++ Compiler (e.g., `g++`)
- Make

### 🔧 Compile the Compiler and Interpreter

```bash
make
```

This will generate:
- `comp` → compiler binary
- `asmb` → interpreter binary

---

## 📝 Example Program

Create a file `myprogram.txt`:

```plaintext
program
var num
start
  let num = 42 ,
  print num ,
end
```

### ✅ Compile:
```bash
$ ./comp myprogram.txt
```

### ▶️ Run:
```bash
$ ./asmb myprogram.asm
```

**Output:**
```
42
```

---

## 🔡 Language Reference

### 📌 Variables
```plaintext
var num
let num = 10 ,
```

### 🔁 Loops
```plaintext
iter (i < 3)
  start
    print i ,
    let i = (i + 1) ,
  end ,
```

### 🔀 Conditionals
```plaintext
if (10 > 5)
  print 1 ,
,
```

### 🧮 Expressions
```plaintext
print #(((2 + 2) * 3) / 4) ,
```
> `#` is a unary negation operator.

### 📥 Input
```plaintext
read num ,
```

### 💬 Comments
```plaintext
! This is a comment !
```

---

## 📌 Supported Operators

| Operator | Description         |
|----------|---------------------|
| `+`      | Addition             |
| `-`      | Subtraction          |
| `*`      | Multiplication       |
| `/`      | Division             |
| `<`      | Less than            |
| `>`      | Greater than         |
| `:`      | Equals (assignment)  |
| `#`      | Negation             |

---

## 📚 Future Improvements

- [ ] Semantic analysis (type checking, scoping)
- [ ] Better error handling and reporting
- [ ] Intermediate code representation (IR)
- [ ] LLVM code generation
- [ ] Function support

---

## 🤝 Contributing

Pull requests and feature suggestions are welcome!  
Feel free to fork this project and help improve it.

---

## 📜 License

This project is licensed under the MIT License. See [LICENSE](./LICENSE) for details.

---

## 👨‍💻 Author

**Aksharma127**  
🔗 [GitHub Profile](https://github.com/Aksharma127)

---
