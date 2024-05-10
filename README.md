# decode-tree
#Overview
The decode function is designed to read a specially formatted text file where each line contains a number followed by a word. The function constructs a message by reading these numbers and words, aligning them into a "pyramid" structure, and then concatenating the words at the end of each pyramid line to form a decoded message.

#How It Works
The function reads the input file and builds a dictionary mapping numbers to corresponding words. It then calculates key numbers that correspond to the end of each line in a pyramid structure. For instance, in a pyramid that grows by one additional number each line, the key numbers might be the numbers that are positioned at the end of each line (e.g., 1, 3, 6 for a three-line pyramid). The function collects the words associated with these key numbers and concatenates them to form the final decoded message.

#Usage
To use this function, ensure your data file is formatted correctly, with each line containing a number followed by a word. The function expects the path to this file as an argument.

#Prerequisites
Python 3.x
Text file with data formatted as <number> <word>
Running the Script
Save your input file (e.g., messages.txt) in the same directory as your script or provide the relative path to the file.
Call the function with the file path as the argument:
python
Copy code
print(decode('messages.txt'))
Example
Given an input file messages.txt with the following content:

3 love
6 computers
2 dogs
4 cats
1 I
5 you
When you run the script, it will output:

I love computers

This output is derived from building a pyramid where the lines end with the numbers 1, 3, and 6, corresponding to the words "I", "love", and "computers", respectively.

File Format
Ensure each line of your input file is formatted as follows:

php
Copy code
<number> <word>
The number and word should be separated by a space, with each pair on a new line.
