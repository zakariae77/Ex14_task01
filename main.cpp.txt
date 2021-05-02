// Exercise_14_task_01.cpp : This file contains the 'main' function. Program execution begins and ends there.
//

#include <iostream>
#include "golf.h"
using namespace std;

int main()
{
    const int n = 5;
    golf g[5];
    char name[len];
    int hc=0;
    
    for (int i = 0; i < n; i++) 
    {
        cout << "Enter name (q to quit):";
        cin.getline(name, len);
        if (name[0] == 'q' && strlen(name) == 1) { break; }
        cout << "Enter handicap number: ";
        cin >> hc;
        cin.get();
        //if the user mess to enter name we use showgolf overloaded function
        if (strlen(name) == 0) { setgolf(g[i]); }
        //else if the user enter the name we use the original function showgolf
        else {
            setgolf(g[i], name, hc);
        }
        showGolf(g[i]);
        cout << "\nDo u want to modify handicap value ( y/n ): ";
        cin >> name[0];
        if (name[0]=='y') {
            cout << "Enter new handicap number: ";
            cin >> hc;
            handicap(g[i], hc);
            cout << "\n++++++++++   Updated data    ++++++++++" << endl;
            showGolf(g[i]);
        }
        cout << "\n*************     Record number " << i + 1 << " done       ***********\n" << endl;
        cin.get();
    }
    
    cout << "\n***********    Good bey    ************" << endl;
    
}

