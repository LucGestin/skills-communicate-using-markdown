
# Header 1
## Header 2
### Header 3
#### Header 4
##### Header 5
###### Header 6

[Search for it!](www.google.com)

Here's [a link to something else] [another place].
Here's [yet another link] [another-link].
And now back to [the first link][another place].

[another place]: www.github.com
[another-link]: www.google.com

![Black cat][Black]
![Orange cat][Orange]

[Black]: https://upload.wikimedia.org/wikipedia/commons/a/a3/81_INF_DIV_SSI.jpg
[Orange]: http://icons.iconarchive.com/icons/google/noto-emoji-animals-nature/256/22221-cat-icon.png

I read this interesting quote the other day:
> "Her eyes had called him and his soul had leaped at the call. To live, to err, to fall, to triumph, to recreate life out of life!"
> 
A list of cooking elements :
* Milk
  * Eggs
* Salmon
  * Butter

1. Cut the cheese
2. Slice the tomatoes,
3. Rub the tomatoes in flour

A task list :
- [x] Turn on GitHub Pages
- [ ] Outline my portfolio
- [ ] Introduce myself to the world

# Python

**int()**, which turns things into ints
**float()**, which turns things into floats
**bool()**, which turns things into bools.

**or** used in an expression : The Python docs describe it as **if x is false, then y, else x**

**and** : The Python docs describe it as **if x is false, then x, else y**
```
print(0 or 1) ## 1
print(0 and 1) ## 0
```
**is**, the identity operator, is used to compare two objects and returns true if both are the same object.
```python
def is_adult(age):
   return True if age > 18 else False
```

**Complex numbers** : you can get its real and imaginary part:
```
complexNumber.real #2.0
complexNumber.imag #3.0  
```
**Enums**
```
class State(Enum):
INACTIVE = 0
ACTIVE = 1
```
**Lists**, a list can contain a mix of different types of variable
```
dogs = ["Roger", "Syd"]
```
the **list.append** method modifies a list by adding an item to the end

the **list.pop** method removes and returns the last element of a list

the **list.index** method returns its index.


**Tuples**, immuable group of objects, often used for functions that have multiple return values.
```
names = ("Roger", "Syd")
```

**Sets**, like Tuples but they are not ordered and they are mutable.
```
set1 = {"Roger", "Syd"}
set2 = {"Roger"}
intersect = set1 & set2 #{'Roger'}
union = set1 | set2
difference = set1 - set2 #{'Syd'}
isSuperset = set1 > set2 # True
```
**Strings** are sequence of characters
```
claims = 'pluto is a planet!'
words = claims.split
' 👏 '.join([word.upper() for word in words]) 
the output is 'PLUTO 👏 IS 👏 A 👏 PLANET!'
"{}, you'll always be the {}th planet to me.".format(planet, position)
```

**Dictionnaries**, to create collections of key / value pairs.
```
dog = { 'name': 'Roger', 'age': 8 }
```

**Objects** : If the object provides methods to change its content, then it's mutable. Otherwise it's immutable.

**For** loops
```
for i in range(5):
    print("Doing important work. i =", i)
```
**While** loops
```
i = 0
while i < 10:
   print(i, end=' ')
   i += 1 # increase the value of i by 1
```

**List comprehension**
```
squares = [n**2 for n in range(10)]
```

**Help** function and **docstrings**
```
def least_difference(a, b, c): 
# Return the smallest difference between any two numbers among a, b and c.
# least_difference(1, 5, -5) returns 4
    diff1 = abs(a - b)
    diff2 = abs(b - c)
    diff3 = abs(a - c)
    return min(diff1, diff2, diff3)

help (least_difference)
```

**External libraries**
```
from math import log, pi
from numpy import asarray
type(rolls)
dir()
help()
```

**Linear Algebra**

$\hat{i}$ and $\hat{j}$ are the basic vectors of the xy coordinate system

the span of vector $\vec{v}$ and vector $\vec{w}$ is the set of all their possible linear combinations : a $\vec{v}$ + b $\vec{w}$

linear dependent vector $\vec{u}$ = a $\vec{v}$ + b $\vec{w}$

linear independent vector $\vec{u}$ != a $\vec{v}$ + b $\vec{w}$

the basis of a vector space is a set of linear independent vectors that span the full space

Linear transformation: grids lines remain parallel and evenly spaced, and such that the orginin remains fixed.

$\vec{v}$ = -1 $\vec{i}$ + 2 $\vec{j}$

Transformed $\vec{v}$ = -1 (Transformed $\vec{i}$ ) + 2 (Transformed $\vec{j}$ )

$$\begin{bmatrix}
       a & c \\
       b & d
     \end{bmatrix}$$

$$\begin{bmatrix}
       x \\
       y
     \end{bmatrix}$$

$$\begin{bmatrix}
       ax+cy \\
       bx+dy
\end{bmatrix}$$

a,b the place where the 1rst basis vector lands and c,d the place where the 2nd basis vector lands.

matrices are transformation of space.

vector multiplication 
$$\[ \vec{v} = \begin{pmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{pmatrix} \]$$

$$\(\vec{v} = \begin{bmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{bmatrix}\)$$

$$\(\vec{v} = (v_1, v_2, \ldots, v_n)\)$$

$$\overrightarrow{AB}$$
$$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$


