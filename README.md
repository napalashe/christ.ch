# christ.ch
## HOW I WENT ABOUT PROJECT
I tried to create this program in a variety of different ways until I realized the array function was simply the most optimal way to go about the project.
Using the array to store countries I could then perform the switch statements to hold language and specilaiztion until the rand function assigned a country.
My programming approach was solo, so I failed many times writing the code until I finally was able to model something that could be built upon.
I first attemped to do the blackjack project but without any one to help me I wasted a lot of time until I switched as I could not get everything to work perfectly before the deadline.
The switch function was taken out multiple times to add the boolean structure butI could not function the rand without it, such I ended up abondoning the idea entirley and created a simple program that functions all the materials.
## AUTHORS
Me, myself and I. Working solo is not optimal and I would have appreciated feedback throughout the process.
## HOW TO USE CODE
I set up the code to be very user friendly, it guides you through the process and even tries to engage with you depending on your selection. One thing I wish I added was a return function however with switch I would have to creat an if else functions instead.
Other than that the function should operate perfectly! It guides you through and will display the probability at the end.
## CODE
[main.final.cpp]
//Christopher Mireles
//UCR MEDICAL CENTER VOLUNTEERS



//includes our random number generator as well as string function
#include <iostream>
#include <ctime>
#include <string>
#include <cstdlib>
using namespace std;



int main ()
{
  //variables to select choices later
  int option;
  int secondOption;
  string y;
  string n;
  string answer;

  //2D array to form together countries with language
  //array is 10/5 which allows for a lot of variation
  string countries [10] [5] = {{"Estonia", "Canada", "China", "Australia", "Haiti"},
    {"Argentina","Bolivia","Chile","Colombia","Costa Rica"},
     {"Ireland","taiwan","Singapore","Macau","Hong Kong"},
     {"Egypt","Sudan","Algeria","Iraq","Morocco"},
     {"Luxembourg","Armenia","United Kingdom","Latvia","Ukraine"},
     {"Fiji","Pakistan","India","Nepal","Guyana"},
     {"India","Bangladesh","Bengal","Tripura","Assam"},
     {"Austria","Belgium","Jamaica","Madagascar","Monaco"},
     {"Brazil","Portugal","Mozambique","Angola","Macau"},
     {"Germany","France","Switzerland","Belgium","Russia"}};



  
//greets user
  cout <<"Hello! Welcome to UCR Medical Center Volunteer program!\n";
//This part is neccesary to simulate user engagement
cout << "Please help us find the best spot for you by answering\na few questions below!\n";
  
//creating space
  cout <<" \n";


  
  
  //question for user to input
  cout << "What language do you feel comfortable in? " << endl;




  
//prints out display of countries
cout << "Select language below: " << endl;
cout << "----------------------\n";

  cout <<"1. English\n";
  cout <<"2. Spanish\n";
  cout <<"3. Russian\n";
  cout <<"4. Italian\n";
  cout <<"5. German\n";
  cout <<"6. Mandarin\n";
  cout <<"7. Portugese\n";
  cout <<"8. Arabic\n";
  cout <<"9. French\n";
  cout <<"10. Vietnamese\n";  
  cout <<"-----------------\n";
//user selects option from below
  cin >> option;
  
//switch statement will display output based on selection
  switch (option-1)
    {

case 0:
    cout << "You have chosen English!\n";
    break;

     case 1:
    cout << "You have chosen Spanish!\n";
    break;

     case 2:
    cout << "You have chosen Russian!\n";
    break;

    case 3:
    cout << "You have chosen Italian!\n";
    break;

     case 4:
    cout << "You have chosen German!\n";
    break;

     case 5:
    cout << "You have chosen Mandarin!\n";
    break;

    case 6:
    cout << "You have chosen Portugese!\n";
    break;

    case 7:
    cout << "You have chosen Arabic!\n";
    break;

     case 8:
    cout << "You have chosen French!\n";
    break;

     case 9:
    cout << "You have chosen Vietnamese!\n";
    break;
      
    }

  cout << "------------------------------\n";
  cout <<"Great! Now what is your specilization?\n";
  cout <<"--------------------------------------\n";
 cout << "1. Cardiology\n";
  cout <<"2. Dermatology\n";
  cout <<"3. Gastroenterology\n";
  cout <<"4. Nuerology\n";
  cout <<"5. Pediatrics\n";
cout <<  "-------------------\n";
//user inputs a specialization
  cin >> secondOption;

  switch(secondOption)
  {
    case 1:
    cout << "A cardiologist is always needed!\n";
    break;

     case 2:
    cout << "Dermatology will be very helpful!\n";
    break;

     case 3:
    cout << "Gastroenterology! Great selection.\n";
    break;

    case 4:
    cout << "Nuerology! Someone here is smart.\n";
    break;

     case 5:
    cout << "Pediatrics! Always needed!\n";
  }

  //small detail
  //using === now to highlight finale
cout << "====================================\n";
  //this is fun part
  //randome number generator, used so countries are paired together
  srand(time(0));

  int index = (rand() % 5);
  
  //Lets user know what country they are assigned to
  cout <<"Based on what you have told us the country\nchosen for you is: \n\n";

  //code to print out final place
  cout << countries[option-1][index]<< "!\n" << endl;

//letting user know how we came to conclusion
  cout << "\nWe multiplied the languages by specializations to reach\nthis conclusion\n"; 
  cout <<"\n10 * 5 = 50\n";
//simple math but needs to be displayed conclusivly for user
  cout << "Would you like to know the statistical odds of this selection?\n";
  cout << "Type Y for yes and N for no\n\n";


  //yes or no
  cin >> answer;
  if (answer == "y")
  {
     cout << "\nProbability factors for your selection were 1 out of 50\n which is 2.0%!\n";
    cout << "\nWe hope you enjoyed the program! Please come back again!\n";
  }
  if (answer == "n")
  {
    cout << "awkward...here is it anyways: \n";
     cout << "\nProbability factors for this program were 1 out of 50\nwhich is 2.0%!\n";
    cout << "\nWe hope you enjoyed the program! Please come back again!\n";
    }
  

}
    
  
  
    
  




  
  
