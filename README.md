

#include<iostream>
#include<conio.h>
#include<ctime>
using namespace std;

int main() {
    system("cls");
    int a, b;
   
    
    
    
     srand(time(0));
     a = rand() % 100 + 1;
    if (a < 1 || a > 100)
    {
        cout << "Invalid Input! please enter the number between 1 and 100"<< endl;
        
        cin >> a;

    }
    
    system("cls");
    for (int i = 0; i < 5; i++) {
        cout << "Enter the number: " << endl;
        cin >> b;
        if (cin.fail())
        {
            cout << "Invalid Input! please enter the number between 1 and 100"<< endl;
            cin.clear(); // clear the error flags
            cin.ignore(numeric_limits<streamsize>::max(), '\n'); // ignore the wrong input
            i--;
            continue;
        }
        if (b < 1 || b > 100)
    {
        cout << "Invalid Input! please enter the number between 1 and 100"<< endl;
        i--;
        continue;
    }

        if (b == a) {
            cout << "Congratulations you won!!!!!" << endl<< endl;
            break;
        } else if (b < a) {
            cout << "The number entered is smaller. Try again" << endl<<endl;;
        } else if (b > a) {
            cout << "Entered number is greater than previous number entered. Try again" << endl<<endl;
        }else if (i == 3)
        {
            cout << "You have only 2 chances left"<< endl<<endl;;
            
        }
        
        } 
        if (b != a){
            cout<<"You lost!! The number was "<< a << endl;
         }
getch();
    return 0;
}
