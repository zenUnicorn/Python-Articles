---
title: "How do i append to a file"
description: "How you can easily i append to a file in python"
date: "2022-09-04"
draft: false
link: "How do i append to a file"
author: "Shittu Olumide"
---

In Python, reading, writing, and editing files are common tasks since the language gives us built-in functions to do so. 

As a developer there are so many reason why you will want to read, write and also edit the files in your project, and python really offers the flexibility to do so in very simple and easy ways. There are a couple of file handling operations in python such as `r` which works for reading the file, `w` opening a file and writing to it, `a` opens a file for appending at the end of the file without truncating it, `+` opens a file for updating(reading & writing) and so on.

In this article, I will be discussing briefly how you can easy append to a file using the python programming language and how to use the append operation effectively.

### What is a file?
A file is a designated spot on the hard drive where associated data is kept. It is used to keep data in non-volatile memory for all time (e.g. hard disk). 

A file must first be opened before we can append to it. It must be closed once we are finished so that the resources associated with the file can be released.

Consequently, a file operation in Python happens in the following order:
- Open a file
- Append to the file
- Close the file


### How to append a text to a file
There are different methods to append a text to a file and I will be showing you that shortly, but firstly let us talk about how it works.
So bascially when you are trying to append to a file, what you are trying to do is that you are trying to add a word, character or a sentence to the end of the file. In simpler terms, whatever goes into the `.write()` method will be added to the end of the text file.

Let us take a look at the different way to append to a file.

#### Using the with statement
The concise shorthand of a try-catch block is replaced with the with statement. More significantly, it makes sure that resources are closed immediately after being processed. Reading from or writing to a file is a typical example of using the with statement. A context manager is a function or class that supports the with statement.

Imagine you have a file with the name `example.txt` and the content looks like this.
```python
The sun shines brighter in the day
Especially in the afternoon
```

Code sample:
```python
with open("example.txt","a") as file:
    file.write("I like to play in the sun light")
```

The example.txt file should look like this now.
```python
The sun shines brighter in the day
Especially in the afternoon
I like to play in the sun light
```
When you're done appending to the file, the with statement immediately closes it.

#### Using the open function
The file is opened via the open() function, which also returns the appropriate file object. 
The syntax of `open()` is:

```python
open(file, mode='')
```


## Conclusion

As you can see, Python has a variety of methods for determining whether a list is empty. Additionally, using this condition before and then nesting your if or for loops is a good practice as it will help to minimize unintended errors. It all depends on your preference but the PEP 8 method is highly recommended as it usually pays off in performance.






