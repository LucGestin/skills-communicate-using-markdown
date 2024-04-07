
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

$\hat{i}$ and $\hat{j}$ are the **basic vectors** of the xy coordinate system

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

Matrix multiplication

$$\begin{bmatrix}
       a & b \\
       c & d
     \end{bmatrix}$$

$$\begin{bmatrix}
       e & f \\
       g & h
     \end{bmatrix}$$

$$\begin{bmatrix}
       ae+bg & af+bh\\
       ce+dg & cf+dh
\end{bmatrix}$$

matrix representing the 90° rotation transformation around $\vec{j}$ :

$$\begin{bmatrix}
       0 & 0 & 1 \\
       0 & 1 & 0 \\
      -1 & 0 & 0
     \end{bmatrix}$$

**The determinant** : the factor by which a linear transformation changes any area is called the **determinant** of that transformation. Whenever the orientation has been inverted, the determinant will be negative.

$$det\left(\begin{bmatrix}
       a & b \\
       c & d
     \end{bmatrix}\right) = ad-bc$$

$$det\left(M1M2\right) = det\left(M1\right)det\left(M2\right)$$

**A Inverse** times A equals the matrix of the transformation that doing nothing

$$ A^-1 A = \begin{bmatrix}
       1 & 0 \\
       0 & 1
     \end{bmatrix}$$

$$A \vec{x} = \vec{v} \\ \\  or \\ \\  \vec{x} = A^-1 \vec{v}$$

**rank** : number of dimensions in the output of the transformation

**column space** of A: the set of all possible outputs for your matrix

when the rank equals the number of columns, we call the matrix **full rank**

the set of vectors that land on the origin is called the **null space** or the **kernel** of your matrix

**non-square matrices** are transfomrations between dimesnions.

the **dot product** of 2 vectors of the same dimension :

$$\begin{bmatrix} 1 \\ 
                  2 \end{bmatrix} \\ . \begin{bmatrix} 3 \\
                                                          4 \end{bmatrix} \\ = 1.3 + 2.4 $$


Formal linear properties :

$L(\vec{v}+\vec{w})$ = $L(\vec{v}) + L(\vec{w})$

$L(c\vec{v})$ = $cL(\vec{v})$

Any time you have a 2d-to-1d linear transformation, applying that transformation is the same thing as taking a dot product with that vector.

The dual of a vector is the linear transformation that it encodes  
The dual of a linear transformation from some space to one-dimension is a vector in that space.

Dotting 2 vectors together :

$$\begin{bmatrix} x_1 \\ 
                  y_1 \end{bmatrix} \\ . \begin{bmatrix} x_2 \\
                                                         y_2 \end{bmatrix}$$ 
                                                 
                                                         is equivallent to 

$$\begin{bmatrix} x_1 & y_1 \end{bmatrix} \\ \begin{bmatrix} x_2 \\
y_2 \end{bmatrix} = x_1 . x_2 + y_1 . y_2$$

area of parallelogram : the **cross product** $\vec{v}$ X $\vec{w}$ is positive when $\vec{v}$ is on the right of $\vec{w}$ and negative when $\vec{v}$ is on the left of $\vec{w}$.


$$ \vec{v} \\ X \\ \vec{w}  =  det (\begin{bmatrix}
      -3 & 2 \\
       1 & 1
     \end{bmatrix}) = (-3).(1) - (1).(2) = -5 $$
     
     
$$\begin{bmatrix} v_1 \\
                  v_2 \\
                  v_3 \end{bmatrix} X \begin{bmatrix} w_1 \\
                                                      w_2 \\
                                                      w_3 \end{bmatrix} =  det  \left(\begin{bmatrix} \hat{i} & v_1 & w_1 \\
                                                                                                \hat{j} & v_2 & w_2 \\
                                                                                                \hat{k} & v_3 & w_3 \end{bmatrix}\right)                                                                                                                             = \hat{i}(v_2w_3 - v_3w_2) + \hat{j}(v_3w_1 - v_1w_3) + \hat{k}(v_1w_2 - v_2w_1)$$

This function is linear :

$$\begin{bmatrix} ? & ? & ? \end{bmatrix} X \begin{bmatrix} x \\
                                                      y \\
                                                      z \end{bmatrix} =  det  \left(\begin{bmatrix} x & v_1 & w_1 \\
                                                                                                y & v_2 & w_2 \\
                                                                                                z & v_3 & w_3 \end{bmatrix}\right)$$

                                                                                                
**Cramer's rule**

$$ \begin{bmatrix}
      2 & -1 \\
      0 & 1
     \end{bmatrix} \begin{bmatrix}
      x \\
      y
     \end{bmatrix} = \begin{bmatrix}
      4 \\
      2
     \end{bmatrix} $$

$$ x  = \frac {det (\begin{bmatrix}
      4 & -1 \\
      2 & 1
     \end{bmatrix})} {det (\begin{bmatrix}
      2 & -1 \\
      0 & 1
     \end{bmatrix})} = \frac {(4)(1) - (2)(-1)} {(2)(1) - (0)(-1)} = 3 $$

$$ y  =  \frac{det(\begin{bmatrix}
      2 & 4 \\
      0 & 2
     \end{bmatrix})} {det (\begin{bmatrix}
      2 & -1 \\
      0 & 1
     \end{bmatrix})} = \frac{(2)(2) - (0)(4)} {(2)(1) - (0)(-1)}= 2 $$

$\vec{v}$ is the **Eigen vector** and $\lambda$ is the **Eigen value**

$$ A \vec{v} = \lambda \vec{v} $$

$$ A \vec{v} - \lambda I \vec{v} = 0 $$

$$ I = \begin{bmatrix}
       1 & 0 & 0 \\
       0 & 1 & 0 \\
       0 & 0 & 1 
     \end{bmatrix}$$


$$ (A - \lambda I) \vec{v} = 0 $$

$$ det (A - \lambda I) = 0 $$

**Derivative** is linear :

$$ L(\vec{v} + \vec{w} ) = L \vec{v} + L\vec{w} $$

$$\frac{d}{dx} (x^3 + x^2) = \frac{d}{dx} (x^3) + \frac{d}{dx} (x^2) $$



vector multiplication 
$$\[ \vec{v} = \begin{pmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{pmatrix} \]$$

$$\(\vec{v} = \begin{bmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{bmatrix}\)$$

$$\(\vec{v} = (v_1, v_2, \ldots, v_n)\)$$

$$\overrightarrow{AB}$$
$$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$


