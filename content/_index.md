---
title: "UCSC"
date: 2019-11-19T17:21:20+01:00
page: true
---

# CSE 130 QUIZ PREP - WEEK 2

<!-- A hugo shortcode for writing quizzes with a markdown-like syntax: https://github.com/bonartm/hugo-quiz. -->

<!-- **Try out the live code editor: https://bonartm.github.io/quizdown-live-editor/** -->


{{< quizdown >}}

# Communication Link Layers
What does the `link_name` parameter depend on in the abstraction of a communication link?

> Explanation: The `link_name` refers to identifiers that change based on the network layer, such as TCP port numbers, IP addresses, or internet addresses.

- [ ] Buffer size
- [x] TCP port number or IP address
- [ ] Message length
- [ ] File descriptor


# SEND and RECEIVE Operations
What are the two primary operations associated with the abstraction of a communication link?

> Explanation: The two primary operations are `SEND` and `RECEIVE`, which handle outgoing and incoming message buffers respectively.

- [x] SEND and RECEIVE
- [ ] CONNECT and DISCONNECT
- [ ] OPEN and CLOSE
- [ ] START and STOP


# Memory’s READ/WRITE Interface
Why is it not ideal to use memory’s READ/WRITE interface directly in communication?

> Explanation: Using memory’s READ/WRITE interface can lead to various issues such as data corruption, duplication, or connection problems in a communication link.

- [ ] It guarantees a stable connection
- [ ] It increases data transfer speeds
- [x] It can cause data corruption, duplication, and loss
- [ ] It simplifies error handling


# SEND and RECEIVE Operations
What is the purpose of the `SEND` and `RECEIVE` operations in the abstraction of a communication link?

> Explanation: `SEND` and `RECEIVE` manage outgoing and incoming message buffers, enabling communication between layers of the network.

- [x] To handle outgoing and incoming message buffers
- [ ] To establish a connection
- [ ] To clear memory buffers
- [ ] To manage port addresses


# Examples of Hardware Communication Links
Which of the following is an example of hardware technology used for communication links?

> Explanation: Hardware technologies refer to physical mediums like cables that carry signals.

- [ ] Ethernet
- [ ] USB
- [x] Twisted pair
- [ ] Unix pipe


# Higher-Level Communication Links
Which of the following is an example of a higher-level communication link?

> Explanation: Higher-level links are protocols or systems that manage communication at a more abstract level.

- [ ] Optical fiber
- [x] The internet
- [ ] Coaxial cable
- [ ] Twisted pair


# Difference Between char *s and char s[10]
What is the primary difference between `char *s` and `char s[10]`?
> Explanation: A pointer points to a single memory address, while an array of fixed size reserves a block of memory.

- [x] `char *s` is a pointer, `char s[10]` is an array
- [ ] Both are pointers to strings
- [ ] `char s[10]` is a pointer, `char *s` is an array
- [ ] There is no difference between the two


# Reading from a File
What does the `read()` function return?
> Explanation: The return value of `read()` indicates how many bytes were actually read, or 0 at the end of the file, or -1 in case of an error.

- [x] Number of bytes read
- [ ] File descriptor
- [ ] Total number of bytes in the file
- [ ] Always -1 to indicate an error


# Buffered vs. Unbuffered I/O
Why might combining buffered I/O with unbuffered I/O lead to issues?
> Explanation: Buffered and unbuffered I/O can produce out-of-order data when used together, as buffered I/O introduces delays in writing data.

- [x] It can lead to out-of-order data
- [ ] It uses more memory
- [ ] It forces immediate writes to disk
- [ ] It disables the use of the buffer


# Creating a File
Which flag in `open()` is used to create a file if it doesn't exist?
> Explanation: The `O_CREAT` flag is used with `open()` to create a new file if it does not already exist.

- [x] `O_CREAT`
- [ ] `O_WRONLY`
- [ ] `O_RDONLY`
- [ ] `O_APPEND`


# Deleting a File
Which function is used to delete a file in Unix?
> Explanation: The `unlink()` function is used to delete a file by removing its directory entry.

- [x] `unlink()`
- [ ] `delete()`
- [ ] `close()`
- [ ] `creat()`


# Opening a File
What does the `open()` function return upon success?
> Explanation: The `open()` function returns a file descriptor that can be used for subsequent operations.

- [x] File descriptor
- [ ] File name
- [ ] Number of bytes
- [ ] Pointer to a buffer


# File Descriptor in Write
What is the role of the file descriptor in the `write()` function?
> Explanation: The file descriptor specifies which file or stream to write data to.

- [x] It indicates which file to write to
- [ ] It sets the number of bytes to write
- [ ] It specifies the buffer location
- [ ] It signals the end of the write operation


# Buffering in File I/O
Why would you use system calls instead of standard I/O functions for file I/O?
> Explanation: System calls provide direct control over buffering, allowing fine-grained management of input and output operations.

- [x] To control buffering
- [ ] To use easier functions
- [ ] To avoid using `fopen()`
- [ ] To increase performance


# Difference Between fopen and open
Which is a key difference between `fopen()` and `open()`?
> Explanation: `fopen()` is a higher-level function that handles buffering, while `open()` is a system call that does not.

- [x] `fopen()` uses buffering, `open()` does not
- [ ] `fopen()` can only read files
- [ ] `open()` requires less memory
- [ ] There is no difference


# Returning File Position with lseek
What does `lseek()` return?
> Explanation: The `lseek()` function returns the new position in the file, or -1 if an error occurs.

- [x] New file offset
- [ ] File descriptor
- [ ] Number of bytes read
- [ ] File name


# Writing to a File
What does the `write()` function return?
> Explanation: `write()` returns the number of bytes written or -1 in case of an error.

- [x] Number of bytes written
- [ ] Buffer size
- [ ] File descriptor
- [ ] File size


# Static vs. Local Variables
What is the difference between local and static variables in C?
> Explanation: Static variables retain their value between function calls, while local variables do not.

- [x] Static variables retain their value between function calls
- [ ] Local variables are global
- [ ] Static variables can only be used once
- [ ] There is no difference


# Setting File Offset with lseek
What does `SEEK_SET` do in `lseek()`?
> Explanation: `SEEK_SET` sets the file offset to a specific value from the start of the file.

- [x] Sets the file offset from the start of the file
- [ ] Sets the file offset from the end of the file
- [ ] Resets the file to its initial state
- [ ] Reads the file contents


# Creating a New File
Which system call creates a new file and overwrites an existing one?
> Explanation: `creat()` creates a new file, overwriting it if it already exists.

- [x] `creat()`
- [ ] `write()`
- [ ] `open()`
- [ ] `delete()`


# Detecting EOF with read()
How does `read()` signal the end of a file?
> Explanation: `read()` returns 0 to indicate the end of the file.

- [x] By returning 0
- [ ] By returning -1
- [ ] By returning the file descriptor
- [ ] By closing the file


# Closing a File
What does `close()` return upon successful execution?
> Explanation: `close()` returns 0 to indicate successful file closure.

- [x] 0
- [ ] 1
- [ ] -1
- [ ] The file descriptor


# Buffering Example
Why does mixing `fprintf()` and `write()` lead to out-of-order data in the output?
> Explanation: The delay introduced by buffered I/O like `fprintf()` can cause data to be written in a different order compared to `write()`.

- [x] Because of the buffering delay in `fprintf()`
- [ ] Because `write()` is faster
- [ ] Because `fprintf()` only works on files
- [ ] There is no issue


# File Permissions in open()
What is the role of the `mode` parameter in `open()` when using `O_CREAT`?
> Explanation: The `mode` parameter defines the file permissions for a new file created with `O_CREAT`.

- [x] It sets file permissions for a new file
- [ ] It controls buffering
- [ ] It sets the file descriptor
- [ ] It specifies how much data to read


# Reading Fewer Bytes Than Requested
What happens if `read()` reads fewer bytes than requested?
> Explanation: `read()` may read fewer bytes than requested if fewer are available.

- [x] It returns the number of bytes actually read
- [ ] It returns -1 to signal an error
- [ ] It continues reading until all bytes are read
- [ ] It returns 0 to indicate an incomplete read


# Opening a File for Writing
Which flag should be used with `open()` to truncate a file upon opening?
> Explanation: The `O_TRUNC` flag truncates a file to zero length when it is opened for writing.

- [x] `O_TRUNC`
- [ ] `O_CREAT`
- [ ] `O_RDWR`
- [ ] `O_RDONLY`


# Memory Allocation for char Arrays
How does the memory allocation differ between `char *s` and `char s[10]`?
> Explanation: `char s[10]` allocates a block of 10 bytes, while `char *s` only allocates space for the pointer.

- [x] `char s[10]` allocates memory for 10 characters, `char *s` only allocates space for the pointer
- [ ] Both allocate memory for 10 characters
- [ ] `char *s` allocates more memory than `char s[10]`
- [ ] `char s[10]` does not allocate memory until assigned


# Output of Buffered and Unbuffered Writes

What will the content of the file `out.txt` be after the following C code is executed?

> Explanation: The code mixes buffered (`fprintf`) and unbuffered (`write`) output. The `fflush()` function forces the output buffer to write to the file immediately.

```python
#include <stdio.h>
#include <stdlib.h>
#include <unistd.h>

int main(void) {
    FILE *f = fopen("out.txt", "w");
    int fd = fileno(f);

    fprintf(f, "1\n");
    write(fd, "2\n", 2);

    fflush(f);

    fprintf(f, "3\n");
    write(fd, "4\n", 2);

    fclose(f);
    return EXIT_SUCCESS;
}
```

- [x] `2\n1\n3\n4\n`
- [ ] `1\n3\n2\n4\n`
- [ ] `1\n2\n4\n3\n`
- [ ] `1234\n`


# Function of fflush()

What is the purpose of the `fflush(f)` statement in the C code?

> Explanation: `fflush()` is used to flush the output buffer and ensure that all buffered data is written to the file.

- [x] It flushes the buffer to ensure data is written immediately
- [ ] It closes the file
- [ ] It opens a new file for reading
- [ ] It clears any errors in the file


# Mixing Buffered and Unbuffered Output

Why does the code use both `fprintf()` and `write()` functions to write to the same file?

> Explanation: `fprintf()` is a buffered I/O function, while `write()` is unbuffered. Mixing the two requires caution to avoid out-of-order writes, unless `fflush()` is used.

- [x] To demonstrate the difference between buffered and unbuffered output
- [ ] To write different types of data
- [ ] To optimize performance
- [ ] To ensure file closing


# Reading from a File

What is the purpose of the `read()` function in the `show_file()` function?

> Explanation: `read()` reads data from the file descriptor into the buffer and returns the number of bytes read.

```python
result = read(fd, buf + num_read, sizeof(buf) - num_read);
```

- [x] It reads data from a file descriptor into the buffer
- [ ] It writes data to the file descriptor
- [ ] It opens a new file
- [ ] It closes the file descriptor


# Error Handling in File Operations

What happens if `open()` fails to open the file in the `main()` function?

> Explanation: If `open()` returns -1, the program calls the `fatal_error()` function, which prints an error message and exits.

```python
int fdin = open("infile", O_RDONLY, 0);
if (fdin == -1) fatal_error("can't open input file");
```

- [x] The program prints an error message and exits
- [ ] The program prints an error message and continues
- [ ] The program attempts to reopen the file
- [ ] The program closes the file and exits


# File Closing in C

What is the significance of the `close()` function in the `main()` function?

> Explanation: `close()` closes the file descriptor, releasing the resources associated with the file. If it fails, the program calls `fatal_error()`.

```python
int result = close(fdin);
if (result == -1) fatal_error("can't close input file");
```

- [x] It closes the file descriptor and handles any error
- [ ] It reads more data from the file
- [ ] It reopens the file
- [ ] It resets the file pointer

# Opening a File in C

What will happen if the file `infile` does not exist when the following code is executed?

> Explanation: The `open()` function uses the `O_RDONLY | O_CREAT` flags, meaning it will open the file in read-only mode if it exists, or create it if it doesn't.

```python
int fdin = open("infile", O_RDONLY | O_CREAT, 0);
if (fdin == -1) fatal_error("can't open input file");
```

- [x] The file will be created, and the program will continue
- [ ] The program will exit with an error
- [ ] The file will not be created, and the program will continue
- [ ] The program will enter an infinite loop


# Buffer Size in show_file()

What is the maximum number of characters that can be read and printed by the `show_file()` function?

> Explanation: The buffer size is set to 50 characters, which means the function reads at most 50 characters from the file.

```python
char buf[50];
```

- [x] 50
- [ ] 100
- [ ] Unlimited
- [ ] 25


# Handling File Descriptors

Why is the `close()` function necessary at the end of `main()`?

> Explanation: `close()` is used to release the file descriptor and any resources associated with the file. It is good practice to close a file after completing operations on it.

```python
int result = close(fdin);
if (result == -1) fatal_error("can't close input file");
```

- [x] It ensures the file is properly closed and resources are released
- [ ] It flushes the buffer
- [ ] It writes data to the file
- [ ] It reads more data from the file


# File Permissions

What file permissions are assigned when the file `infile` is created by the following `open()` function call?

> Explanation: The `0666` mode grants read and write permissions to the owner, group, and others when the file is created.

```python
int fdin = open("infile", O_RDONLY | O_CREAT, 0666);
```

- [x] Read and write for owner, group, and others
- [ ] Read and write for owner only
- [ ] Read, write, and execute for all
- [ ] No permissions


# Infinite Loop Protection

How does the `show_file()` function avoid an infinite loop when reading from the file?

> Explanation: The `read()` function returns 0 when the end of the file is reached, causing the loop to break.

```python
if (result == 0) break;
```

- [x] The `read()` function returns 0 at the end of the file
- [ ] The loop exits after 50 characters
- [ ] The file descriptor is closed inside the loop
- [ ] It never exits the loop


# Error Handling in C

What does the program do if an error occurs while reading from the file?

> Explanation: If `read()` returns a negative value (indicating an error), the `fatal_error()` function is called, which prints an error message and exits the program.

```python
if (result < 0) fatal_error("error reading input file");
```

- [x] It prints an error message and exits
- [ ] It retries reading the file
- [ ] It continues reading and ignores the error
- [ ] It skips over the error and closes the file


# Handling the Write System Call

What is the purpose of the `str_write()` function?

> Explanation: The `str_write()` function repeatedly writes a given string to the file descriptor until all characters have been written, handling potential partial writes.

```python
void str_write(int fd, char *buf, size_t num_chars) {
    ssize_t result;
    size_t num_written = 0;

    for (;;) {
        result = write(fd, buf + num_written, num_chars);
        if (result < 0) fatal_error("error writing output file");
        if (result == 0) break;
        num_written += result;
        num_chars -= result;
    }
}
```

- [x] It writes the string to the file descriptor, handling partial writes
- [ ] It reads data from the file and prints it
- [ ] It appends data to the file without overwriting
- [ ] It closes the file after writing


# Error Handling in Writing to Files

What happens if the `write()` system call fails in the `str_write()` function?

> Explanation: If `write()` returns a negative value, the `fatal_error()` function is called, which prints an error message and exits the program.

```python
if (result < 0) fatal_error("error writing output file");
```

- [x] The program prints an error message and exits
- [ ] The program retries the write operation
- [ ] The program ignores the error and continues
- [ ] The program closes the file and continues


# Opening a File in Write-Only Mode

What happens if the file `outfile` cannot be opened for writing in the `main()` function?

> Explanation: If `open()` returns -1, indicating that the file could not be opened, the `fatal_error()` function is called to handle the error by printing a message and exiting.

```python
int fdout = open("outfile", O_WRONLY, 0);
if (fdout == -1) fatal_error("can't open output file");
```

- [x] The program prints an error message and exits
- [ ] The program opens the file in read-only mode instead
- [ ] The program continues without writing to the file
- [ ] The program waits for the file to become available


# Opening a File for Writing

What are the permissions assigned to the file `outfile` when it is opened with the following `open()` call?

> Explanation: The `0664` permission mode allows the owner to read and write, and the group to read. Others also have read permissions.

```python
int fdout = open("outfile", O_WRONLY | O_CREAT, 0664);
```

- [x] Owner has read and write, group has read, others have read permissions
- [ ] Owner has read and write, group has write, others have no permissions
- [ ] Owner and group have read and write, others have no permissions
- [ ] Everyone has read and write permissions


# Function of `write()` System Call

What is the role of the `write()` system call inside the `str_write()` function?

> Explanation: The `write()` function attempts to write the specified number of bytes to the file descriptor and returns the number of bytes successfully written.

```python
result = write(fd, buf + num_written, num_chars);
```

- [x] It writes the remaining part of the string to the file and returns the number of bytes written
- [ ] It reads data from the file
- [ ] It closes the file
- [ ] It appends the string to the end of the file


# Handling Partial Writes

Why does the `str_write()` function use a loop to call `write()` repeatedly?

> Explanation: The `write()` system call may write fewer bytes than requested, so the loop ensures that all the data is written by repeatedly calling `write()` with the remaining data.

```python
for (;;) {
    result = write(fd, buf + num_written, num_chars);
    if (result < 0) fatal_error("error writing output file");
    if (result == 0) break;
    num_written += result;
    num_chars -= result;
}
```

- [x] To ensure that all bytes are written, handling partial writes
- [ ] To retry writing the file on failure
- [ ] To keep reading data from the file
- [ ] To check if the file is writable


# Truncating a File

What does the `O_TRUNC` flag do in the `open()` system call?

> Explanation: The `O_TRUNC` flag truncates the file, which means it clears all its content if the file already exists before writing new data.

```python
int fdout = open("outfile", O_WRONLY | O_CREAT | O_TRUNC, 0664);
```

- [x] It clears the content of the file if it exists
- [ ] It appends new data to the file
- [ ] It prevents the file from being opened if it exists
- [ ] It opens the file in read-only mode


# Error Handling with `write()`

What happens if the `write()` system call fails in the `str_write()` function?

> Explanation: If `write()` returns a negative value, the `fatal_error()` function is called, which prints an error message and terminates the program.

```python
if (result < 0) fatal_error("error writing output file");
```

- [x] The program prints an error message and exits
- [ ] The program retries writing to the file
- [ ] The program ignores the error and continues
- [ ] The program closes the file and continues


# Handling Partial Writes in C

Why does the `str_write()` function contain a loop for calling `write()`?

> Explanation: The `write()` system call may write fewer bytes than requested, so the loop ensures that all the data is written by calling `write()` repeatedly until the entire string is written.

```python
for (;;) {
    result = write(fd, buf + num_written, num_chars);
    if (result < 0) fatal_error("error writing output file");
    if (result == 0) break;
    num_written += result;
    num_chars -= result;
}
```

- [x] To handle partial writes and ensure all bytes are written
- [ ] To keep appending data to the file
- [ ] To retry writing if an error occurs
- [ ] To ensure that the file is opened in write mode


<!-- ---
primary_color: steelblue
---

# The sound of dog

---
shuffle_answers: false
---

What do dogs sound like?

> ![](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2d/Dog_-_%E0%B4%A8%E0%B4%BE%E0%B4%AF-6.JPG/150px-Dog_-_%E0%B4%A8%E0%B4%BE%E0%B4%AF-6.JPG)

```python
class Dog(Animal):
    def __init__(self, name):
        self.name = name
```

- [ ] yes
- [ ] no
- [ ] `self.sound = "meow"`
- [x] wuff

# Put the [days](https://en.wikipedia.org/wiki/Day) in order!

> Monday is the *first* day of the week.

1. Monday
2. Tuesday
3. Wednesday
4. Friday
5. Saturday  


# Optional Math formula rendering

$$
x = \frac{2+2}{\sqrt{a^2+b^2}}
$$


- [ ] yes
- [ ] no -->

{{< /quizdown >}}
