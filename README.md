#include <iostream>
using namespace std;

int fibonacci(int n) {
    if (n <= 1)
        return n;
    
    int a = 0, b = 1, fib;
    for (int i = 2; i <= n; i++) {
        fib = a + b;
        a = b;
        b = fib;
    }
    return b;
}

int main() {
    int n;
    cout << "Enter the position (n): ";
    cin >> n;
    cout << "Fibonacci number at position " << n << " is: " << fibonacci(n) << endl;
    return 0;
}
