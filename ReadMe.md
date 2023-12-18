# Vector Operations

This repository contains algorithms for vector operations, including the dot product and determination of vector orthogonality.

## Algorithms

### 1. Dot Product Algorithm

The dot product algorithm calculates the dot (scalar) product of two vectors. The procedure `dot_product` takes two vectors (`v1` and `v2`) as input and calculates the dot product, storing the result in the variable `ps`.

#### Pseudocode

plaintext
ALGORITHM DotProductFunction

FUNCTION dot_product(v1, v2) :
VAR
    n := Length(v1)
    ps := 0

    FOR i FROM 0 TO n - 1 DO
        ps := ps + v1[i] * v2[i]
    END_FOR

    RETURN ps
END


To use these algorithms, include the provided pseudocode in your programming environment. You can adapt the algorithms to your preferred programming language.

// Dot Product Example
var v1 = [2, 3, 4];
var v2 = [1, -1, 2];
var resultDotProduct = dot_product(v1, v2);
console.log('Dot Product:', resultDotProduct);

// Orthogonality Determination Example
var areOrthogonal = AreVectorsOrthogonal(v1, v2);
console.log('Are Vectors Orthogonal?', areOrthogonal);



# Set Operations

This repository contains algorithms for set operations, including finding the sum of all distinct elements from two sets.

## Algorithm

### Sum of Distinct Elements

The "Sum of Distinct Elements" algorithm calculates the sum of all distinct elements from two sets. The procedure iterates through each element in both sets, adding elements to the sum only if they are not present in the other set.

#### Pseudocode

plaintext
ALGORITHM SumOfDistinctElements

PROCEDURE CalculateDistinctSum(VAR sum, set1, set2) :
VAR
    i, j
    elements := Array[BOOLEAN]
    maxSize := Max(Max(Length(set1), Length(set2)), 1)

    FOR i FROM 0 TO maxSize - 1 DO
        elements[i] := False
    END_FOR

    FOR i FROM 0 TO Length(set1) - 1 DO
        IF NOT elements[set1[i]] THEN
            elements[set1[i]] := True
            sum := sum + set1[i]
        END_IF
    END_FOR

    FOR i FROM 0 TO Length(set2) - 1 DO
        IF NOT elements[set2[i]] THEN
            elements[set2[i]] := True
            sum := sum + set2[i]
        END_IF
    END_FOR

END
