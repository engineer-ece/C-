
# Chrono

```c++
#include <iostream>
#include <chrono>
#include <unistd.h>


using namespace std;
using namespace chrono;

int main(){
   
    auto start =  steady_clock::now();  
    sleep(3);
    auto end   = steady_clock::now();

    cout << "Nanosecond = " <<duration_cast<nanoseconds>(end - start).count() <<"ns" <<endl;
    cout << "Microsecond = "<<duration_cast<microseconds>(end - start).count() <<"µs" <<endl;
    cout << "Millisecond = "<<duration_cast<milliseconds>(end - start).count() <<"ms" <<endl;
    cout << "Seconds = " <<duration_cast<seconds>(end - start).count() <<"s" <<endl;
    



 
    return 0;
}
```
