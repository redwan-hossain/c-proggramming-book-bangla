# structure variable

```c
struct student {  // student is a struct tag and user defined type
  char name[50];
  int marks;
  int roll;
}; // no structure variable is declared here

struct {  // here type is missing
  char name[50];
  int age;
} englishTeacher, mathTeacher;  // these are the structure variables
```

. operator দিয়ে structure variable এর member গুলোকে access করা যায়।
