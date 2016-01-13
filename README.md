# Star-Display
This program will ask a user how many lines they would like to use when displaying a pyramid of ascending then descending number of stars. It has all been placed inside a loop, allowing the user to get multiple displayed pyramids of varying numbers, then enter 0 if they would like to quit.


// Author: Roel Cuellar
// File Name: TT10_L2_Cuellar.cpp 

#include <iostream>
#include <iomanip>
using namespace std;


int main()
{   
    //Here is the users input for how many lines will be used
    int numberlines = 0;
    cout << "How many lines would you like to use in this diamond \ndrawing? Enter "\
    "0 to quit the program. ";
    cin >> numberlines;
    
    //This if else statement will take modulus of the number of lines we are using
    //And sets the variable number, equal to 1 or 0 depending if odd or even.
    int number=0;
    int odd_finder = 0;
    odd_finder = (numberlines % 2);
    if (odd_finder > 0){
    	number = 1;
    }
	else{
		number = 0;
	} 
    
    //initializing variables for upcoming loops
    int linecounter=0, stars=0;
    while (numberlines !=0){
    //This for loop controls the top half of the displayed pyramid
    for (linecounter = 1; linecounter <= (numberlines / 2) + number; linecounter++){
        //This for loop will control the number of spaces displayed
        for (int spaces = (numberlines / 2); spaces >= linecounter; spaces--){
        	cout << " ";
       }
           //This portion of the for loop controls number of stars displayed
           for (stars = 1; stars < linecounter; stars++){
               cout << "*";
           }
           //This portion of the for loop controls number of stars displayed
           for (stars = 0; stars < linecounter; stars++)
           {
               cout << "*";
           } 
           cout << "\n";
    }
    //This for loop controls the top half of the displayed pyramid
    for (linecounter = 1; linecounter <= numberlines; linecounter++){
        //This for loop will control the number of spaces displayed
       	for (int spaces = 0; spaces < linecounter; spaces++){
            cout << " ";
        }
        //This portion of the for loop controls number of stars displayed 
		for (stars = (numberlines / 2) - 1; stars >= linecounter; stars--){
            cout << "*";
        }
        //This portion of the for loop controls number of stars displayed
        for (stars = (numberlines / 2); stars >= linecounter; stars--){
            cout << "*";

        }
        cout << "\n";
     }
     //Here we ask how many lines the user would like again, without asking again,
     //this while loop will run forever
     cout << "How many lines would you like to use in this diamond \ndrawing? Enter "\
     "0 to quit the program. ";
     cin >> numberlines;
     }  
system ("pause");
return 0;  
}


/* Here is the programs output
How many lines would you like to use in this diamond
drawing? Enter 0 to quit the program. 8
    *
   ***
  *****
 *******
 *******
  *****
   ***
    *




How many lines would you like to use in this diamond
drawing? Enter 0 to quit the program. 7
   *
  ***
 *****
 *****
  ***
   *




How many lines would you like to use in this diamond
drawing? Enter 0 to quit the program. 4
  *
 ***
 ***
  *


How many lines would you like to use in this diamond
drawing? Enter 0 to quit the program. 0
Press any key to continue . . .
*/
