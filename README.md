This lets me declare 2D matrices as slices.
It allocates all the space for data as one lump and puts it in fullData which is not exported.
It then allocates a slices of slices ands sets up the indexing.

Normally you say

    m := newFMatrix2c (n_r, n_c)

where `n_r` and `n_c` are the number of rows and columns respectively.
But to access elements like a matrix, you need to say `m.Mat[i][j]` to get to elements `i` and `j`.

We need to have different functions for different types, so `newFMatrix(n, m)` gives us a float32 matrix, but `newBMatrix` gives a boolean matrix.

