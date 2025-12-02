# Task 1 – Number Guessing Game

This folder contains the C++ program for the Number Guessing Game.
#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    srand(time(0));          // Seed for random number 
    int number = rand() % 100 + 1;   // Random number between 1–100
    int guess;
    int attempts = 0;

    cout << "===== NUMBER GUESSING GAME =====" << endl;

    while (true) {
        cout << "Enter your guess (1-100): ";
        cin >> guess;
        attempts++;

        if (guess > number) {
            cout << "Too High! Try again.\n";
        }
        else if (guess < number) {
            cout << "Too Low! Try again.\n";
        }
        else {
            cout << "\n🎉 Congratulations! You guessed the number " 
                 << number << " correctly!\n";
            cout << "Total Attempts: " << attempts << endl;
            break;
        }
    }

    return 0;
}
