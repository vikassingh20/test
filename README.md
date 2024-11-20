# Vector Dot Product Implementation

The vector dot product is a mathematical operation that takes two vectors and produces a scalar (a single number).

---


Geometrically, the dot product represents the product of the magnitudes (Euclidean lengths) of two vectors and the cosine of the angle between them.

## Mathematical Expression
The dot product of two vectors
**a** = \[a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub>\] and **b** = \[b<sub>1</sub>, b<sub>2</sub>, ..., b<sub>n</sub>\]**


$$a \cdot b = \sum_{i=1}^{n} a_i \cdot b_i$$


---

>The dot product operation calculates how aligned two vectors are.

Here are the four key properties of the dot product:

## Vector Dot Product Properties

1. **Commutative Property**:
    The dot product is commutative
   - Formula: `a . b = b . a`
   
2. **Distributive Property**:
   - The dot product distributive
   - Formula: `a . (b + c) = a . b + a . c`

3. **Scalar Multiplication**:
   - The dot product of a vector and a scalar can be factored out.
   - Formula: `k * (a . b) = (k * a) . b = a . (k * b)`

4. **Orthogonality and Angle Between Vectors**:
   - If two vectors are **orthogonal** (perpendicular), their dot product is zero: `a . b = 0`
     - `a . b = |a| * |b| * cos(θ)`
     - Where `|a|` and `|b|` are the magnitudes of vectors `a` and `b`, and `θ` is the angle .

Here I have only covered 
- [x] normal algorithm
- [ ] SIMD Optimization
- [x] Multi-threaded Approach

<!-- This is an example snippet --->
## Example Code in Python

```
def dot_product(a, b):
    result = 0.0
    for i in range(len(a)):
        result += a[i] * b[i]
    return result

vec1 = [1 2 3]
vec2 = [3 2 1]

result = dot_product(vec1, vec2)
print("Dot Product:", result)

```
![dot_product_components](https://github.com/user-attachments/assets/0c399caf-afe8-498f-bb54-5ccfcb4ec3bf)

> [!Note]
> Dot product of two orthogonal vectors is zero.


| **Version**               | **Time Complexity** |
|---------------------------|---------------------|
| normal algorithm          |  O(n)          |
| SIMD Optimization          |  O(n)          |
| Multi-threaded Approach    |  O(n/p)        |

View More about [dot product](https://math.libretexts.org/Bookshelves/Calculus/Calculus_(OpenStax)/12%3A_Vectors_in_Space/12.03%3A_The_Dot_Product#:~:text=The%20dot%20product%20of%20two%20vectors%20is%20the%20product%20of,%E2%80%96%E2%87%80v%E2%80%96cos%CE%B8.)

[^1]: https://en.wikipedia.org/wiki/Euclidean_vector#Length
