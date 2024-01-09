# Matrix-Commands
Project Description
In order to familiarize you with matrix transformations and operations, you will be completing the empty methods that are modeled on the corresponding commands from OpenGL. Your versions will use slightly different names to distinguish them from the built-in routines. You will write code to do the following:

1. Write the code for Init_Matrix() that initializes the matrix stack. After this command is called, the only matrix on the stack should be the 4x4 identity matrix.  Note that the transformations we create will be for manipulating objects in 3D, hence the need for 4x4 matrices.

2. Print the current transformation matrix (the top of the stack) to the Processing console. Make sure your matrix prints on four separate rows. For output that is easier to read, have this command print an empty line after the last row.  The command for this is Print_CTM().

Example:

1 0 0 0
0 1 0 0
0 0 1 0
0 0 0 1

3. Create your own routine that performs 4x4 matrix multiplication, to be used in the next step.

4. Create 4x4 scale, translate, and simple rotation matrices, and multiply the matrix on the top of the stack with this newly-created matrix. The names of the commands that you will implement are Scale, Translate, RotateX, RotateY, RotateZ. For instance, Scale (x, y, z) will create a new scale_matrix, and then change to the top of the matrix stack in this way: new_ctm = old_ctm * scale_matrix.  Note that the three Rotate commands each take a single floating point angle in degrees, so you will have to convert these values to radians before you invoke sin() and cos(), which use radians.  Each rotate command should create a rotation matrix that rotates a given 3D point counter-clockwise around the appropriate axis (X, Y, or Z).

5. Implement Push_Matrix and Pop_Matrix. The Push_Matrix command duplicates the current transformation matrix and places this copy on the top of the matrix stack. The Pop_Matrix command pops the current transformation matrix off the top of the stack. If there is just one matrix on the stack, calling Pop_Matrix should print an error message.
