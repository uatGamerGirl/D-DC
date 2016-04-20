#include <iostream>
#include <cstdlib>
#include <iomanip>
#include <vector>
#include <string>
#include <fstream>
#include <algorithm>
//#pragma warning(disable: 4996)
using namespace std;

string features[3][88];
string races[8] = { "Dragonborn", "Dwarf", "Eladrin", "Elf", "Half-Elf", "Halfling", "Human", "Tiefling" };

ifstream featsFile, raceFile;


int main(){
	string line = " ";
//	featsFile.open("feats.txt");		//file with all the feats info

	/*

	//feats multi-array
	for (int x = 0; x < 88; x++){		//keeps track of which ability in the list
		for (int y = 0; y < 3; y++){	//while all three spots for that ability is being written, (name, race avaiable, and effect)
			getline(featsFile, line);
			features[y][x] = line;
		}	
	}

	

	for (int x = 0; x < 88; x++){		//keeps track of which ability in the list
		for (int y = 0; y < 3; y++){
			cout << features[y][x] << ", " ;
			if (y == 2){
				cout << endl;
			}
		}
	}
	*/
	//featsFile.close();

	
	raceFile.open("Races.csv");

	//Read in the whole line and then pars it by the ','s

	for (int x = 0; x < 9; x++){		//keeps track of which ability in the list
		for (int y = 0; y < 5 ; y++){	//while all three spots for that ability is being written, (name, race avaiable, and effect)
			getline(raceFile, line);
			features[y][x] = line;
		}
	}



	for (int x = 0; x < 9; x++){		//keeps track of which ability in the list
		for (int y = 0; y < 5; y++){
			cout << features[y][x] << ", ";
			if (y == 9){
				cout << endl;
			}
		}
	}
	//race array
	//race array is completed above when it is initalized.


	/*
	cout << features[0][0] << "-" << features[1][0] << "-" << features[2][0] << endl << endl;
	cout << features[0][1] << "-" << features[1][1] << "-" << features[2][1] << endl << endl;
	cout << features[0][2] << "-" << features[1][2] << "-" << features[2][2] << endl << endl;
	*/
	system("pause");
	return 0;
}
