# Breakingbadquotes
api for breakingbadquotes.xyz breaking bad quotes site
# main
```cpp
#include "Breakingbadquotes.h"
#include <iostream>

int main() {
   Breakingbadquotes api;

    auto quote = api.random_quote().then([](json::value result) {
        std::cout << "Search results: " << result.serialize() << std::endl;
    });
    quote.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```

