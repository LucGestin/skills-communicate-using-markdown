
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

**Data types**:
```
* string "Hello World!" or 'Hello World!'
* int 12
* float 3.12
* list \['hello', 12, 3.12]
* dict {'name': 'Ben', 'age':31 } 
* tuple (2, 3)
* range(5)
* True and False
```

**Strings** are sequence of characters

Casting:
*int() to transform string into integer
*float() to transform string into float

```
claims = 'pluto is a planet!'
words = claims.split
' 👏 '.join([word.upper() for word in words]) 
the output is 'PLUTO 👏 IS 👏 A 👏 PLANET!'
"{}, you'll always be the {}th planet to me.".format(planet, position)
interpolation print(f"I am {age} years old)
```

**''.join(reversed(word))** to reverse the letters in a string

```
def create_phone_number(n):
	return "({}{}{}) {}{}{}-{}{}{}{}".format(*n)

def create_phone_number(n):
    n = ''.join(map(str,n))
    return '(%s) %s-%s'%(n[:3], n[3:6], n[6:])

roman = 'IVXM'
for i,v in enumerate(roman): ##i: index , v: character
        if i not in index_pairs:
            convertion+=codex[v]
```

**Integer and Float**
```
str() to transform string into integer

10 / 3 equals 3.33
10 // 3 equals 3
% modulo operator, (10 % 3)==0 equals False but (9 % 3)==0 equals True
round (12.4)
```

**Special Values**
```
Everything is True, except:
* None
* False
* Empty value. [], {}, '', 0, 0.0, (), range(0)...

casting bool() returns True or False.
```

**or** and **and** are the logical OR and AND.
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

**dogs.append("Paul")** method for adding an item to the end

*dogs.remove("Paul") method removes and returns the last element of a list
*dogs.pop() method removes and returns the last element of a list
*list.index("Syd") method returns its index
*del dogs[0]
*sorted (dogs) or dogs.sort()

staff = ["Ben", "Alex", "Lucien", "Arthur", "Anne", "Blair", "Sam"]
for index, staff_member in enumerate(staff):
    print(f"{index + 1} - {staff_member}")
```
List comprehension
```
squares = [n**2 for n in range(10)]
upcase_list = [letter.upper() for letter in letters]
fruits = ['Orange', 'Mango', 'Banana', 'Pineapple', 'Kiwi']
short_name_fruits = [fruit for fruit in fruits if len(fruit) < 6]
mixed_case_fruits = [fruit.upper() if len(fruit) < 6 else fruit.lower() for fruit in fruits]

def wave(people):
    return [people[:i] + people[i].upper() + people[i+1:] for i in range(len(people)) if people[i].isalpha()]
```
![image](https://github.com/LucGestin/skills-communicate-using-markdown/assets/164859028/7b6c1eed-969b-463d-9ae6-f058f75f52ff)

**Tuples**, immuable group of objects, often used for functions that have multiple return values.
```
names = ("Roger", "Syd")
```

**Sets**, like Tuples but a set is an unordered collection with no duplicate elements, they are mutable.
```
set1 = {"Roger", "Syd"}
set2 = {"Roger"}
intersect = set1 & set2 #{'Roger'}
union = set1 | set2
difference = set1 - set2 #{'Syd'}
isSuperset = set1 > set2 # True
```
**Dictionnaries**, to create collections of key / value pairs.
```
london = {
    "country": "England",
    "population": 8_982_000,
    "star_monument": "Big Ben"
}

london["country"]     #=> "England"
london["population"]  #=> 8982000
london['star_monument'] = "Big Ben"

del london['star_monument']

for key in london:
    print(key)
output:
country
population

for value in london.values():
    print(value)
output:
England
8982000

for key, value in london.items():
    print(f"{key} -> {value}")
output:
country -> England
population -> 8982000

london.get('country', "no key country") #=> "England"

students = ['Peter', 'Mary', 'George', 'Emma']
student_ages = [24, 25, 22, 20]
for student, age in zip(students, student_ages):
    print (f'student:{student}, age: {age}')
```
dict comprehension:
```
student_ages_dict = {key: value for key, value in zip(students, student_ages)}
```


**Objects** : If the object provides methods to change its content, then it's mutable. Otherwise it's immutable.

**Ternary operator** if ... else
```
value_if_true if condition else value_if_false
is_nice = True
state = "nice" if is_nice else "not nice"
```

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


**code example : is_colorful**
```
def is_colorful(number):
    # Convert number to a list of digits ==> List comprehension
    digits = [int(digit) for digit in str(number)]

    # Set to store products of consecutive subsequences
    products = set()

    # Iterate over the digits to generate all the consecutive subsequences
    for i in range(len(digits)):
        product = 1
        for j in range(i, len(digits)):
            product *= digits[j]
            if product in products:
                return False
            products.add(product)

    return True
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
**Object Oriented Programming (OOP)**

Class and Instances
![image](https://intellipaat.com/mediaFiles/2019/03/python10.png)

```
class Car:
    def __init__(self):
        self.engine_started = False

    def is_engine_started(self):
        return self.engine_started

    def start_engine(self):
        self.engine_started = True

my_car = Car()
my_car.engine_started      #=> False  - Calling the attribute
my_car.is_engine_started() #=> False  - Calling the method therefore using ()
my_car.start_engine()      #=> Calling the method, therefore using ()
my_car.engine_started      #=> True   - Calling the attribute

class Castle:
  def __init__(self, name, ruler):
    self.name = name
    self.ruler = ruler

  def castle_details(self):
    return f"{self.name} is ruled by {self.ruler_name()}"

  def ruler_name(self):
    return self.ruler.capitalize()

dragonstone = Castle("Dragonstone", "targaryen")
dragonstone.castle_details() # => "Dragonstone is ruled by Targaryen"
```

Chaining:
In this example, the .arange() method creates a matrix from 1 to 32 with step count of 2, .reshape adjusts the matrix into a 4x4 configuration and .clip is used to set minimum element to 9 and maximum to 25 in the matrix.
```
import numpy as np
# Chaining different methods of numpy
chained_numpy = np.arange(1, 32, 2).reshape(4, 4).clip(9, 25)
print(chained_numpy)
```
Summary:
* Everything in Python is an object.
* OOP is about data (or state) and behavior.
* State is stored in instance attributes (self.engine_started)
* Behavior is defined by instance methods (def is_engine_started(self): in the class definition)
* self refers to the instance on which the instance method has been called

Inheritance:
```
class Building:
  def __init__(self, name, width, length):
    self.name = name
    self.width = width
    self.length = length

  def floor_area(self):
    return self.width * self.length

class Castle(Building):
    def __init__(self, name, width, length):
        super().__init__(name, width, length)
        self.butler = None
```
Specific behavior Only a castle may have a butler
```
    def has_a_butler(self):
        return self.butler is not None
```
Change an inherited method with the **super** keyword, which calls the parent’s method with the same name.
```
    def floor_area(self):
        return super().floor_area() + 300  # `super` calls `floor_area` of `Building`
```
Summary
* Inheritance is used when classes need to share behavior and properties
* Subclasses inherit functions and instance attributes from parents
* On top of that, subclasses can define more instance attributes and functions
* Use **super()** to access the parent class

Class functions:
```
class House:
  @classmethod
  def price_per_square_meter(self, city):
      if city is "Paris":
          return 9000
      elif city is "Brussels":
          return 3000
      else:
        return f"No data for {city}"

print(House.price_per_square_meter("Paris")) # => 9000
```
* You create a class function if it does not need/is not relevant to a single instance
* You will use class function more than you define them.


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

**Calculus**

the fundamental theorem of calculus ties together the ideas of integrals and derivatives, each one is the inverse of the other.

$$\frac{dA}{dx} = x^2$$

$$\frac{ds}{dt} (t)= \frac {s(t+dt)-s(t)} {dt} \\ when \\ dt-> 0 $$

$$f(x)= x^2 \\ => \\ \frac{df}{dx} (x) = 2x$$

$$f(x)= x^3 \\ => \\ \frac{df}{dx} (x) = 3x^2$$

$$f(x)= x^4 \\ => \\ \frac{df}{dx} (x) = 4x^3$$

$$f(x)= x^n \\ => \\ \frac{df}{dx} (x) = nx^{n-1}$$

$$f(x)= \frac{1}{x} \\ a.k.a. \\ x^{-1} => \\ \frac{df}{dx} (x) = TBD $$

$$f(x)= \sqrt{x} \\ => \\ \frac{df}{dx} (x) = TBD $$

$$f(x)= \sin\theta \\ => \\ \frac{df}{dx} (x) = \cos\theta$$

$$sum: \\ \frac{d}{dx} (g(x)+h(x)) => \frac{dg}{dx} + \frac{dh}{dx}$$

$$product: \\ \frac{d}{dx} (g(x) *h (x)) => g(x) * \frac{dh}{dx} + h(x) * \frac{dg}{dx} (x) \\ a.k.a. Left  d(Right) + Right  d(Left)$$

$$Composition \\ \frac{d}{dx} (g(h(x)) => \frac{dg}{dx} (h(x)) * \frac{dh}{dx}(x) \\ a.k.a. \\Chain \\ rule$$


**END**


