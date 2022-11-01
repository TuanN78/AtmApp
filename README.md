# AtmApp
test

#include <iostream>
using namespace std;

void show_menu(){
    cout << "\n**************MENU**********" << endl;
    cout << "1. Check balance" << endl;
    cout << "2. Deposit" << endl;
    cout << "3. Withdraw" << endl;
    cout << "4. Quit" << endl;
    cout << "**************MENU************" << endl;
}

int main(){


    char selection;
    long long balance = 500;

    do{
        // display menu
        // cout << "\n1. Check Balance" << endl;
        // cout << "2. Deposit" << endl;
        // cout << "3. Withdraw" << endl;
        // cout << "Q - Quit" << endl;
        show_menu();
        cout << "Enter your choice: ";
        cin >> selection;
        system("clear");

        if(selection == '1'){ 
                cout << "Balance is:" << balance << endl;
        }else if(selection == '2'){
            long long deposit_amount;
            cout << "Deposit amount: ";
            cin >> deposit_amount;
            balance += deposit_amount;
        }else if(selection == '3'){
            long long withdraw_amount;
            cout << "Withdraw amount: ";
            cin >> withdraw_amount;
            if(withdraw_amount <= balance)
                balance -= withdraw_amount;
            else{
                cout << "Not enough money!";
            }  
        }else if(selection == 'Q' || selection == 'q'){
            cout << "GOODBYE!" << endl;
        }else{
            cout << "Unknown selection. Please try again";
        }

    }while(selection != 'q' && selection != 'Q');

    return 0;
}