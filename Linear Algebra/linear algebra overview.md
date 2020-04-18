* Euclidean space
* Hypercube
* Differentiate matrix equations
* Nonsingular
* Mixture of Gaussians/Generative Model vs. bivariate Gaussian distributions
* Voronoi tessellation
* The Four Fundamental Subspaces of the Data Matrix
* Relationship between Affine space, Vector Space, Subspace with Solutions of linear sysotems, and matrix's column space


1. One of the most fascinating theorems of linear algebra proves that every square matrix, no matter what numbers it contains, must map a certain set of vectors back to themselves with some scaling. In the general case of a rectangular matrix, it maps a set of input vectors into a corresponding set of output vectors, and its transpose maps those outputs back to the original inputs. The technical terminology is that square matrices have eigenvectors with eigenvalues, and rectangular matrices have left and right singular vectors with singular values.

```
Let  A be a rectangular matrix. If there are vectors u and v and a scalar σ such that Av = σu and ATu = σv, then u and v are called left and right singular vectors and σ is a singular value of A.

```
1. The ordered set of singular values of a matrix is called its spectrum, and it reveals a lot about the matrix. The gap between the singular values affects how stable the solutions are, and the ratio between the maximum and minimum absolute singular values (the condition number) affects how quickly an iterative solver can find the solution. Both of these properties have notable impacts on the quality of the solution one can find.



# Vector Space
## Why we need vector space? [1]
Loosely speaking mathematicans invented vector space to mean any type of mathematical object that can be multiplied by numbers and added together.

## Definition of vector space?
[In mathematics, and more specifically in linear algebra, a **linear subspace**](https://en.wikipedia.org/wiki/Linear_subspace), also known as a vector subspace is a vector space (The term linear subspace is sometimes used for referring to **flats** and **affine subspaces**. In the case of vector spaces over the reals, linear subspaces, flats, and affine subspaces are also called **linear manifolds** for emphasizing that there are also **manifolds**.) that is a subset of some larger vector space. A linear subspace is usually called simply a subspace when the context serves to distinguish it from other kinds of subspace.


### Field
* A not so rigor definition of Field
```
A field is a set F of numbers with the property that if a, b ∈ F, then a+b, a−b, ab and a/b are also in F (assuming, of course, that b <> 0 in the expression a/b).
```

### Definition of Vector Space[1][2, Chapter 6]
```
A vector space consists of a set V (elements of V are called vectors), a field F (elements of F are called scalars), 
and two operations :
• An operation called vector addition that takes two vectors v, w ∈ V, and produces a third vector, written v+w ∈ V.
• An operation called scalar multiplication that takes a scalar c ∈ F and a vector v ∈ V, and produces a new vector, written cv ∈ V.
```

### Examples of Vector Space[2, Chapter 6]

## Affine Space
### [Why do we need affine space? ](http://www.cis.upenn.edu/~cis610/geombchap2.pdf)
1. One reason is that the point in a vector space corresponding to the zero vector(0), called the origin, plays a special role, when there is really no reason to have a privileged origin. 
1. The other reason is that certain notions, such as parallelism, are handled in an awkward manner in vector space. 
1. But the deeper reason is that vector spaces and affine spaces really have **different geometries**. 
   * The geometric properties of a vector space are invariant under **the group of bijective linear maps**. 
   * The geometric properties of an affine space are invariant under **the group of bijective affine maps**.
   * These two groups are **not isomorphic**. **Roughly speaking, there are more affine maps than linear maps.**
1. Affine spaces provide a better framework for doing geometry. In particular, it is possible to deal with points, curves, surfaces, etc., in an **intrinsic manner**, that is, independently of any specific choice of a coordinate system. **Use coordinate systems only when needed!** Affine spaces are the right framework for dealing with motions, trajectories, and physical forces, among other things.

### Linear Maps vs. Affine Maps
### Isomorphic

### Examples of Affine Space
1. The solutions of the system ```Ax=b``` is an affine space, but not a vector space (linear space) in general.

### Affine Space Definitions
1. Almost every affine concept is the counterpart of some concept in linear algebra.


## Affine Sets and Hyperplane
### Hyperplane
1. [A hyperplane in an n-dimensional Euclidean space is a flat, n-1 dimensional subset of that space](https://www.quora.com/Support-Vector-Machines-What-is-an-intuitive-explanation-of-hyperplane) that divides the space into two disconnected parts. 
For example, a point in real line, a line in 2d plane, a plane in 3d space.
1. [A hyperplane is something you can shift parallel to itself, by all possible amounts, and by so doing, fill up all of space.](https://math.stackexchange.com/questions/292066/intuition-about-hyperplane) Of course, all the lines parallel to a given line also fill 3-space; the shifts have to all be in one chosen direction for this to work. Also, one generally excludes curvy sets (like y=cos(x) in the plane) which nonetheless fill up space with their translations.
1. [If V is a vector space, one distinguishes **"vector hyperplanes"**](https://en.wikipedia.org/wiki/Hyperplane) (which are linear subspaces, and therefore must pass through the origin) and **"affine hyperplanes"** (which need not pass through the origin; they can be obtained by translation of a vector hyperplane).

### Affine Space

## [Homogeneous Coordinates](https://hackernoon.com/programmers-guide-to-homogeneous-coordinates-73cbfd2bcc65)

# Isotropic
1. Isotropy is uniformity in all orientations.
1. In mathematics, an isotropic manifold is a manifold in which the geometry does not depend on directions. 
1. Examples are the simply-connected space forms (the n-sphere, hyperbolic space, and R<sup>n</sup>) are isotropic.

# Homomorphism
1. In algebra, a [homomorphism](https://math.stackexchange.com/questions/242348/intuition-on-group-homomorphisms) is a structure-preserving map between two algebraic structures of the same type. 
1. The concept of homomorphism has been generalized, under the name of morphism, to many other structures that either do not have an underlying set, or are not algebraic. This generalization is the starting point of category theory.
1. Homomorphisms of vector spaces are also called **linear maps**, and their study is the object of linear algebra.

## isomorphic
1. In mathematics, an **isomorphism** is a **homomorphism** or **morphism** (i.e. a mathematical mapping) that can be reversed by an inverse morphism. Two mathematical objects are **isomorphic** if an isomorphism exists between them. An **automorphism** is an isomorphism whose source and target coincide. 
1. The interest of isomorphisms lies in the fact that two isomorphic objects cannot be distinguished by using only the properties used to define morphisms; thus isomorphic objects may be considered the same as long as one considers only these properties and their consequences.
1. For most algebraic structures, including groups and rings, a homomorphism is an isomorphism if and only if it is **bijective**.

### Examples
1. Since **log**  is a homomorphism that has an inverse (i.e. **exp**) that is also a homomorphism, **log**  is an isomorphism of groups.

## Homomorphism vs. Isomorphism
1. If there is an isomorphism ```h:A→B``` from an algebraic structure (monoid, group, ring, etc.) ```A``` onto another algebraic structure ```B``` of the same kind, then ```B``` is essentially just ```A``` ‘in disguise’: the two structures are essentially the same structure. In other words, Isomorphisms are the maps that preserve the structure exactly.
1. **Homomorphisms preserve some of the structure**. (Here some may be all, since every isomorphism is a homomorphism. That is, it’s some in the sense of ⊆, not ⫋) They preserve the operations, but they may allow elements that ‘look enough alike’ to be collapsed to a single element. 
   1. For instance, the usual **group homomorphism** from ```Z``` to ```Z/2Z``` (for which you use the notation *Z<sub>2</sub>*) ‘says’ that all even integers are essentially the same and collapses them all to the ```0``` of ```Z/2Z```. Similarly, it ‘says’ that all odd integers are essentially the same and collapses them all to the ```1``` of ```Z/2Z```. It wipes out any finer detail than odd versus even. When you learn in grade school that even + even = even, odd + even = odd, and so on, you’re essentially doing the same thing.)
   1. The fact of being odd or even is called the **parity of integers**. In other words, as we pass from ```Z``` to ```P``` we deliberately lose every aspect of the integers except their parity; their parity alone (with its arithmetic) is retained, and faithfully preserved.

1. The kernel of the homomorphism is a measure of how much detail is wiped out: the bigger the kernel, the more detail is lost. In the example of the last paragraph, the kernel is the entire set of even integers: the fact that all even integers are in the kernel says that they’re all being seen as somehow ‘the same’, and even more specifically, ‘the same’ as ```0```. An isomorphism has a trivial kernel: the only thing that it sees as looking like ```0``` is ```0``` itself, and no detail is lost.

1. Another way to put it is that a homomorphic image of an algebraic structure is a kind of approximation to that structure. If the homomorphism is an isomorphism, it’s a perfect approximation; otherwise, it’s more or less crude approximation. As the kernel of the homomorphism gets bigger, the crudeness of the approximation increases. In the case of groups, if the kernel is the whole group, then the homomorphic image is the trivial group, and all detail is lost: all that’s left is the fact that we started with a group.

1. Group homomorphisms are maps between groups which respect structure. This is easy to picture in the context of isomorphisms between groups. The size of the two groups is the same (even if they are infinite), and their structure behaves the same (even if the underlying sets and binary operations are different). So finding an isomorphism is basically like translating a passage between two languages.









### References
1. What is a Vector Space? Geoffrey Scott
1. Mathematical Tools for Physics, James Nearing. 
1. Linear Algebra for Computer Vision, Robotics, and Machine Learning, Jean Gallier and Jocelyn Quaintance, 2019
