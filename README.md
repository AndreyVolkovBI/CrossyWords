# Crossy words: word matrix
Library that generates the word matrix in a way to have multiple words in one 5x5 matrix.
## Available methods
`getMatrix(lang="en")`

Parametrs:
- lang - language of words in the matrix. Values: "en", "ru". By default - "en".

Note that files "russian.txt" and "english.txt" should be added to the root folder.

Result:
- a list of lists representing a 5x5 matrix 
- a dictionary of coordinates of specific word {word: [coordinates in matrix]}

`printMatrix(matrix)` - prints generated matrix

`printWords(words)` - prints generated words with coordinates of letters in the matrix

## Installation
`pip install crossywords`

## Example
```python
import crossywords as cw

matrix, words = cw.getMatrix("en")  # getting a matrix and words in it

cw.printMatrix(matrix)  # printing matrix
print()
cw.printWords(words)  # printing words in it
```
Output:
```
t a t s o
r h l k b
s o w k t
g a n h n
e t h i a

think - [[4, 1], [4, 2], [4, 3], [3, 4], [2, 3]]
thank - [[2, 4], [3, 3], [4, 4], [3, 4], [2, 3]]
own - [[2, 1], [2, 2], [3, 2]]
show - [[2, 0], [1, 1], [2, 1], [2, 2]]
talk - [[0, 2], [0, 1], [1, 2], [1, 3]]
start - [[0, 3], [0, 2], [0, 1], [1, 0], [0, 0]]

```
