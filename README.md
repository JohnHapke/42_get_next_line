# 42_get_next_line

## Purpose
>The purpose of this project is to code a function that returns a line, read from a file descriptor.

## Explanation of Behavior
The get_next_line function is designed to read a single line at a time from a specified file descriptor `fd`. Each call to the function retrieves the next line from the file or input stream, returning it as a dynamically allocated string without the trailing newline character `\n`.

If the end of the file is reached or an error occurs, the function returns NULL. To handle lines that span multiple reads, the function uses a static variable to retain any leftover characters from the previous call, ensuring seamless continuation.

## Buffer Size
The buffer size determines how many bytes are read at a time from the file descriptor. By default, the buffer size is set to 42. However, you can customize it by defining your own buffer size during compilation. Use the `-D BUFFER_SIZE=n flag` (where n is your desired size) when compiling the function. 
Choosing an appropriate buffer size can impact the function's performance, depending on your use case and file size.

## Bonus
The project also includes a bonus version of the get_next_line function. This version is capable of handling multiple file descriptors simultaneously, making it possible to read from different files or inputs without losing track of the progress in each.

## Allowed Functions

- [`malloc`](https://man7.org/linux/man-pages/man3/free.3.html)
- [`free`](https://man7.org/linux/man-pages/man3/free.3.html)
- [`read`](https://man7.org/linux/man-pages/man2/read.2.html)

## Grade: 125 / 100

## Used Tests

- Francinette: https://github.com/xicodomingues/francinette
- gnlTester: https://github.com/Tripouille/gnlTester
