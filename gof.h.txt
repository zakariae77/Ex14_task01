#pragma once

const int len = 40;
struct golf
{
	char fullname[len];
	int handicap;
};

//non-interactive version:
void setgolf(golf & g, const char* name, int hc);

//interactive version:
int setgolf(golf & g);

//reaset handicap
void handicap(golf & g, int hc);

//display contents of golf
void showGolf(golf & g);