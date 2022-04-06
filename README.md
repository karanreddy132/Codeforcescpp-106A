# Codeforcescpp-106A
#include <bits/stdc++.h>
using namespace std;
 
int main() {
	string trump_card, first, second;
	map<string, int> m;
	m["6"] = 1;
	m["7"] = 2;
	m["8"] = 3;
	m["9"] = 4;
	m["T"] = 5;
	m["J"] = 6;
	m["Q"] = 7;
	m["K"] = 8;
	m["A"] = 9;
	cin >> trump_card >> first >> second;
	if ((first.substr(1, 1) == trump_card &&
		 trump_card != second.substr(1, 1)) ||
		(first[1] == second[1] &&
		 m[first.substr(0, 1)] > m[second.substr(0, 1)]) ||
		(first.substr(1, 1) == trump_card &&
		 trump_card == second.substr(1, 1) &&
		 m[first.substr(0, 1)] > m[second.substr(0, 1)]))
		cout << "YES";
	else
		cout << "NO";
	return 0;
}
