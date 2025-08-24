1. Definition and Declaration

A pointer is a variable that stores the address of another variable.

Declaration:

int *p;     // pointer to int
char *c;    // pointer to char


Example:

int a = 10;
int *p = &a;   // p holds the address of a

🔹 2. Address vs Value

p → stores the address of the variable.

*p → gives the value stored at that address (dereferencing).

Example:

int a = 10;
int *p = &a;
cout << p;   // prints address of a
cout << *p;  // prints value of a (10)

🔹 3. Common Mistakes (and Corrections)

❌ Mistake: Confused when to use *.

✅ Use *p to get the value, p (without *) gives the address.

❌ Mistake: Thought array needs * to get values.

✅ Correction: arr[i] already gives the value.

arr[i] == *(arr+i)

❌ Mistake: Tried to increment arr directly.

✅ Correction: arr is fixed (points to start). Only a pointer variable (p = arr) can be incremented.

🔹 4. Pointers and Arrays

The name of an array (arr) acts like a pointer to its first element.

int arr[4] = {10, 20, 30, 40};
int *p = arr;     // same as &arr[0]


Accessing elements:

arr[i]

*(arr+i)

p[i] (if p = arr)

🔹 5. Pointer Arithmetic with Arrays

p++ moves the pointer to the next element.

Example:

int *p = arr;
cout << *p;   // 10
p++;
cout << *p;   // 20


Pointer arithmetic automatically accounts for data type size (e.g., +4 bytes for int).

🔹 6. Using Pointers in Loops

With indexing:

for(int i=0; i<4; i++) cout << arr[i];


With pointer arithmetic:

for(int i=0; i<4; i++) cout << *(arr+i);


By incrementing pointer itself:

int *p = arr;
for(int i=0; i<4; i++) {
    cout << *p;
    p++;
}

✅ Key Takeaways

arr = address of first element.

*arr = first element.

*(arr+i) = arr[i].

Pointers let us traverse arrays without explicit indices.

Always distinguish between address (p) and value (*p).
