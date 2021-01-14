# inverse-even-factorials

#include <iostream>
using namespace std;


int main(){
    int n;
    cout << "Enter the value of N: ";
    cin >> n;
    cout << 1;
    for(int i=2; i<=n; i+=2){
        cout << "+ (1/" << i << "!) ";
    }

    cout << "=";

    float sum = 1;

    for(int i=2; i<=n; i+=2){
        int s = 1;
        for(int j=1; j<=i; j++){
                s = j*s;
        }
        sum = sum + (1.0/s);
    }
    cout << sum;
    return 0;
}
