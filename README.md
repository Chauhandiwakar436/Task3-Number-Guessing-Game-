# Task3-Number-Guessing-Game-
Number Guessing Game
#include <cstdlib> 
#include <ctime>    

using namespace std;

int main() {
   
    srand(static_cast<unsigned int>(time(0)));
  
    int randomNumber = rand() % 100 + 1;
    int userGuess = 0;
    int numberOfTries = 0;

    cout << "Welcome to the Number Guessing Game!" << endl;
    cout << "I have chosen a number between 1 and 100. Can you guess it?" << endl;

 
    do {
        cout << "Enter your guess: ";
        cin >> userGuess;
        numberOfTries++;

        if (userGuess > randomNumber) {
            cout << "Too high! Try again." << endl;
        } else if (userGuess < randomNumber) {
            cout << "Too low! Try again." << endl;
        } else {
            cout << "Congratulations! You guessed the correct number in " << numberOfTries << " tries." << endl;
        }

    } while (userGuess != randomNumber);

    return 0;
}
