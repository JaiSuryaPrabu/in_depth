# 1. Scalars and Vectors

## Scalars
* Scalars are regular numbers like 1,2,3...
* They have only magnitude
* Scalars are denoted as $a,b,c ...$

## Vectors
* Vectors are described by various ways.
* In physics, vectors are pointing arrows
* In computer science, vectors are ordered list of numbers
* In general, vectors are n-dimensional value that contains direction and magnitude.
* Vectors are denoted as $\vec{a},\vec{b},...$
* In vector, there are two main operations :
    * Vector addition
    * Vector multiplication
 
### Vector Addition
* Vector addition is the sum of two vectors.
* For example,

$$\vec{a} = \left[ \begin{array}{c} 1 \\ 2 \end{array} \right]$$

$$\vec{b} = \left[ \begin{array}{c} 3 \\ -1 \end{array} \right]$$

$$\vec{c} = \vec{a} + \vec{b}$$

Where $\vec{c}$ is calculated as,

$$\vec{c} = \left[ \begin{array}{c} 1+3 \\ 2-1 \end{array} \right]$$

$$\vec{c} = \left[ \begin{array}{c} 4 \\ 1 \end{array} \right]$$

### Scalar Multiplication
* Scalar multiplication is where a scaler `a` is multiplied with a vector $\vec{a}$ to form a scaled vector

# 2. Linear Equations

## Terminologies
> 1. The set of all possible vactors that you can reach with a linear combination of a given pair of vectors is called **span** of vectors
> 2. The **basis** of a vector space is a set of linear independent vectors that span the full space.

## Basis vectors
For an example, let 
$$\vec{a} = \left[ \begin{array}{c} 3 \\ -1 \end{array} \right]$$

where `a` is a vector and 3 and -1 are scalars. It can visualized in a 2d space like 3 as x and -1 as y then the vector points the (3,-1). In mathematical term, x is denoted as $\hat{i}$ and y as $\hat{j}$. The vector can be written as $\vec{a} = 3 * \hat{i} + (-1) * \hat{j}$. Here the $\hat{i}$ and $\hat{j}$ are called as **basis vectors** because the basis vectors helps to reach any point in the vector space and the given example is the **linear combination**.

There are three possiblities in a 2d space:
1. If a single scalar only moves freely then it can only move in a straight line. It is like : $y = m * x + c$ which is used in linear regression
2. If both the scalars can move freely then it can move any direction.
3. There is an *unlucky* possible way, where the both basis vectors lies on same line.

The unlucky case is the **linear dependent** and possiblity 2 is the **linear independent**.

# 3. Linear Transformations
> In linear algebra, transformation is a function that gets a vector as input and produce the transformed function as output
* Linear transformation has a direct link to the matrices
* Linear transformation is changing the direction of the vector from one direction to the another with corresponding to the vector space and this happens when **two matrices multiplied** together.
* For example, let a matrix points a direction of parallel to x axis and this matrix is multiplied to another matrix then the resultant vector points another direction like perpendicular to the x axis.

* The transformations is linear when
  * All lines must remain lines without getting curved
  * Origin must remained fixed in its place
  * The transformations must evenly spaced when it shrinks or expands
 
# 4. Matrix Multiplication
> Matrix multiplication is mainly used in the robotics, graphics and deep learning
* In matrix multiplication, one transformation  happens after the another transformation from right to left.
* For example, let there be `A`.`B` transformations and `X` be the matrix, if `A` is a rotation and `B` makes the matrix `X` to shear ( a transformation slants or distorts an object along thier x-axis or y-axis)
* The Matrix multiplication happens from `B` and then `A` like this : `A * B * X = C * X`
* Here `C` is the composition and it is the result of matrix multiplication of `A` and `B`.

# 5. Determinant
* After the transformation , the area of $\hat{i}$ and $\hat{j}$ is called **determinant**
* It tells the timSes the area before transformations
* If the vectors are dependent then the determinant is 0.
* If the determinant is negative, then the transformation flipped the whole vector space like turning the page in the book
* Let the matrix be,
$$ \left[ \begin{array}{cc} a & b \\ c & d \end{array} \right] = (a * d) - (b * c)$$
* Here ,
  * The `a` denotes the length,
  * `d` denotes the breath and
  * `b` denotes the rotation on x-axis and
  * `c` denotes the rotation on y-axis
 
# 6. Linear System of equations
* Equation that has variables one sied and values (*constants*) on other side like this,
  $$ 2 * x + 5 * y = -3 $$
  $$ 4 * x + 0 * y = 0 $$
  And this can be represented with matrices like,
  $$ left[ \begin{array}{cc} 2 & 5 \\ 4 & 0 \end{array} \right] * left[ \begin{array}{c} x \\ y \end{array} \right] = left[ \begin{array}{c} -3 \\ 0 \end{array} \right]$$
* The Identity matrix is the result of the no transformation , $A^-1 * A = I$
* The condition for the matrix inversion is that, the determinant for the matrix that to be inversed should not be zero.
* `Rank` - it is the number of dimensions in the output
* The set of all possible outputs is called column space of the matrix
* Column space tells that the solution that exists or not
* After the transformation, the vectors squished into the origin then it is called **null space** or **kernel**

# 7. Dot Product
> When a vector placed in 2d space is converted into 1d space then to find the position of the vector in the 1d space is calculated with the help of dot product

* To understand the dot product, let us consider an example,
  Let a vector named `a` be $[1,2]$ and another vector named `b` be $[3,4]$ then if `a` projected on `b` or vice versa, then the product of the length of `a` and `b` vector is the dot product. Here the order `a` on `b` or `b` on `a` doesn't matters as $(2 * a).b = 2 * (a .b)$.
* The general formula is : $$left[ \begin{array}{c} a \\ b \end{array} \right] \bullet left[ \begin{array}{c} c \\ d \end{array} \right] = left[ \begin{array}{c} a * c \\ b * d \end{array} \right]$$
$$Dot product  = a * c + b * d $$

* There are three kind of results in dot product based on the scenarios,
  * If the a and b are projected on the same direction then the dot product is positive
  * If the a and b are projected on the opposite direction then the dot product is negative
  * If the a and b are perpendicular to each other then dot product is 0
 
* The main usage of the dot product is to convert the multi-dimension space into one dimension space.
* It is calculated when, a series of vectors are placed in the 2d space and it needs to be converted into one dimensional space
* The one dimensional space can be represented as a number line that placed diagonally, the group of vectors are represented as dots.
* The diagonal has a unit vector and let it be $\hat{u}$ and it is placed in the 2d space
* To find the projection , we need to know where the $\hat{i}$ and $\hat{j}$ are placed in the 2d plane
* Thus the transformation can be as `1X2` matrix like this $left[ \begin{array}{c} u_x \\ u_y \end{array} \right]$ and it is used to transform the vector.
* The matrix multiplication of the transform matrix and the vector is same as dot product of the transform matrix and the vector
* The dot product of the vector with the diagonal line provides the transformation 2d to 1d is called as duality
* At last, the dot product is the projection of vectors (multi-dimension) on a line (1 dimension)