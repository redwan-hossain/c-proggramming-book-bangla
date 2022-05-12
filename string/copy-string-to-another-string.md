# copy string to another string

<mark style="color:red;">`#include <string.h>`</mark> এবং  `strcpy(new_array, old_array);` ব্যবহার করে এক string কে আরেক string এ কপি করা যায় তবে এখানেও buffer overflow আছে। তাই এই সমস্যা এড়াতে `strncpy(new_array, old_array, size);` ব্যবহার করতে হয়।&#x20;

```c
#include <stdio.h>
#include <string.h>

int main() {
    char string[] = "hello world again";
    char string2[6];
    strncpy(string2, string, 6);
    //copying string
    string2[5] = '\0';

    printf("%s", string2);


    return 0;
}

```
