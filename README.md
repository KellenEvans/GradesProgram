# GradesProgram

#include <iostream>
using namespace std;

int main() 
{
   double midterm_grade;
   double project_average;
   double homework_average;
   double current_average;
   double minimum_final;
   const int course_goal = 70;
   
   cout << "Please press enter after typing in each number.\n"; 
   cout << "Enter your midterm grade as a number from 0 to 100.\n";
   cin >> midterm_grade; 
   
   cout << "Enter your project average as a number from 0 to 100..\n"; 
   cin >> project_average; 
   
   cout << "Enter your homework average as a number from 0 to 100.\n"; 
   cin >> homework_average; 
   
   if ((midterm_grade > project_average) && (midterm_grade > homework_average))
   {
      cout << "Your highest grade is your midterm at: \n";
      cout << midterm_grade;
      cout << "%\n";
   }
   else if ((project_average > midterm_grade) && (project_average > homework_average))
   {
      cout << "Your highest grade is your project average at: \n";
      cout << project_average;
      cout << "%\n";
   }
   else
   {
      cout << "Your highest grade is your homework average at: \n";
      cout << homework_average;
      cout << "%\n";
   }
   
   if ((midterm_grade < project_average) && (midterm_grade < homework_average))
   {
      cout << "Your lowest grade is your midterm at: \n";
      cout << midterm_grade;
      cout << "%\n";
   }
   else if ((project_average < midterm_grade) && (project_average < homework_average))
   {
      cout << "Your lowest grade is your project average at: \n";
      cout << project_average;
      cout << "%\n";
   }
   else
   {
      cout << "Your lowest grade is your homework average at: \n";
      cout << homework_average;
      cout << "%\n";
   }
   
   current_average = (midterm_grade * 0.20) + (project_average * 0.40) + (homework_average * 0.15);
   cout << "Your current overall average is: \n";
   cout << current_average;
   cout << "% \n";
   
   minimum_final = (course_goal - current_average) * 4;
   
   if (minimum_final < 0)
   {
      cout << "You don't need to take the final to earn a 70% for the course. \n";
   }
   else if (minimum_final > 100)
   {
      cout << "No matter what you score on the final it's impossible to earn a 70% for the course. \n";
   }
   else
   {
      cout << "You need to make a grade of ";
      cout << minimum_final;
      cout << "% on the final to earn a 70% for the course. \n";
   }
   
   return 0;
}
