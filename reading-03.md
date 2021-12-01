# READING, WRITING, and EXCEPTIONS

## [Reading and Writing Files in Python](https://realpython.com/read-write-files-python/)
- File
  - Basic
    - "a contiguous set of bytes used to store data" (*realpython.com*)
  - Modern
    - Header
      - name, size,type
    - Data
      - content
    - End of File(EOF)
      - we saw these in our enviroment setup on the .profile page we wrote
- File Paths
  - Folder Path
    - / in unix
  - File name
    - name of file (duh)
  - Extenstion
    - the suffix of the file name to indicate what file type

### Open and Closing a File in Python
- open()
  - part of standard library
  - requires path to file you want to open
  - e.g. open('the_cake_house/the_pie_room/apple_pie.txt')
- how to close open()
  - try/finally
```python
    file = open('some_file.txt')
        try:
          do something
        finally:
          file.close 
```
  - with
``` python
with open('some_file.txt') as file:
  do something
```
|Character| Meaning|
|---|---|
|r|Open for Reading|
|w|Open for writing|

- Categories of File objects
  - Text Files
    - most common type of file
  - Buffered Binary Files
    - used for reading and writing binary files
  - Raw Binary Files
    - used for low-level building-block for binary and text streams
    - not common

- Method of Reading
  - `.read(size = -1)`
    - if no argument is passed or -1 then the whole file is read
  - `. readline(size -1)`
    - reads whole line if no arguments are passed or -1
  - `.readlines()`
    - this reads the remain lines from the file object and returns tham as a list

- Method of Writing
  - `.write(string)`
    - this writes the string to the file
  - `.writelines(seq)`
    - this writes the sequence to teh file

- Tips
 - `a` in the arguments of the open()
   - allows writing to the end of a file

## [Exceptions](https://realpython.com/python-exceptions/)
- Exceptions vs SyntaxError
  - SyntaxError
    - I did something wrong and the parser can not run it
  - ExceptionsError
    - something has tripped an error code while running the code

- Raising an Exception
  - its us creating our own error to trip
``` python
bobs_burger = "not profitable"
if bobs_burger = "profitable"
  raise Exception('they are never profitiable, the world must be ending')
```

- AssertionError Exception
- assert
  - like in our tests we wrote but used differently
```python
import my_face
assert("My eyes" in my_face), "where did they go!"
```
- Try/ Except 
- this is a way to handle exceptions
- try is the first thing
  - if it has no problems then gravy
  - if there is an exception
- except block springs to action but only if there is an exception
  - otherwise it is never run

- Finally!
- Its the i run no matter what piece
  - so even if an exception was caught and ran the exception block
  - finally will still run

[Return to Home](README.md)
