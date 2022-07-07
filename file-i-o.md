# file I/O

manually by terminal- <mark style="color:red;">**`g++ 101.cpp -o 101 && ./101 <in.txt >out.txt`**</mark>

যখন input file থাকবে না তখন read করতে ঝামেলা করবে, কিন্ত output এর সময় file না থাকলেও সমস্যা নেই কারণ তখন write permission থাকে বিধায় file না থাকলেও তৈরি হয়ে যায়।

```cpp
#include "iostream"
#include "string"

using namespace std;

int main() {
  FILE *inputFile;
  FILE *outputFile;

  inputFile = fopen("in.txt", "r");
    if (inputFile == NULL) {
    return 0;
  }
  outputFile = fopen("out.txt", "w");

  while (true) {
    char ch = fgetc(inputFile);
    if (ch == EOF) {
      break;
    }
    fputc(ch, outputFile);
  }

  return 0;
}
```
