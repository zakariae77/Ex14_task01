#include <iostream>
#include "golf.h"
#include <string.h>
using namespace std;
void setgolf(golf& g, const char* name, int hc) 
{
	strcpy(g.fullname, name);
	g.handicap = hc;
}

//interactive version:
int setgolf(golf& g) 
{
	cout << "*** The name is nessecary !!! : ";
	cin.getline(g.fullname,len);
	cout << "Enter handicap number : ";
	cin >> g.handicap;
	cout << "\n";
	if (strlen(g.fullname) == 0)return 0;
	return 1;
}

//reaset handicap
void handicap(golf& g, int hc)
{
	g.handicap = hc;
}

//display contents of golf
void showGolf(golf& g) 
{
	cout << "\n+++++++++   Golf data   +++++++\n" << endl;
	cout << "Name     : " << g.fullname << endl;
	cout << "Handicap : " << g.handicap << endl;
}