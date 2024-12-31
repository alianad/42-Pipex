<p align="center">
   <img width="100" src="https://github.com/mcombeau/mcombeau/blob/main/42_badges/pipexe.png">
</p>

# 42-Pipex
A program that mimics shell pipe behavior in C. This project focuses on understanding and implementing UNIX mechanisms for inter-process communication.


## 📝 Description

`Pipex` recreates the functionality of shell pipes, allowing the execution of commands in a pipeline fashion. It handles input/output redirection and command execution similar to how the shell processes the following command:

```bash
< file1 cmd1 | cmd2 > file2
```


## 🚀 Features

Mandatory

+ Handles basic pipeline with two commands
+ Input/output file redirection
+ Error handling and memory management
+ Shell command execution with parameters


## 🧩 Usage

Compilation :

```bash
make  #Compile mandatory part
```

Basic Usage :
```bash
./pipex file1 cmd1 cmd2 file2
```

Example :
```bash
./pipex infile "ls -l" "wc -l" outfile
# Equivalent to: < infile ls -l | wc -l > outfile

./pipex infile "grep a1" "wc -w" outfile
# Equivalent to: < infile grep a1 | wc -w > outfile
```


## 📚 Technical Details

Function Used :

+ File operations: `open`, `close`, `read`, `write`
+ Memory management: `malloc`, `free`
+ Process control: `fork`, `wait`, `waitpid`, `exit`
+ Error handling: `perror`
+ File descriptor manipulation: `dup2`
+ Command execution: `execve`
+ Pipe creation: `pipe`
+ File access checking: `access` 

Project Requirements:

+ Written in C
+ Follows Norm coding standards
+ No memory leaks
+ Error handling for unexpected situations
+ Makefile with standard rules (all, clean, fclean, re)
+ Libft usage allowed


## 🎴 Error Handling

The program handles various error cases similar to shell behavior, including:

+ File access permissions
+ Invalid commands
+ Memory allocation failures
+ Pipe creation errors
+ Fork failures

  
## 🛠 Building

The project includes a Makefile with the following rules:

+ `make all`: Compile the project
+ `make clean`: Remove object files
+ `make fclean`: Remove object files and executable
+ `make re`: Rebuild the project



## ⚙️ Testers

+ https://github.com/mariadaan/PIPEXaminator
+ https://github.com/vfurmane/pipex-tester
+ https://github.com/michmos/42_pipex_tester

