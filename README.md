#include <stdio.h>
#include <string.h>

int main() {
    char word[] = "computer";      // Word to guess
    char guess[20];
    int chances = 7;
    int correct = 0;
    int length = strlen(word);

    // Initialize guess array with underscores
    for (int i = 0; i < length; i++) {
        guess[i] = '_';
    }
    guess[length] = '\0';

    printf("🎮 Welcome to Guess the Word Game!\n");
    printf("Hint: It is related to CSE\n");

    while (chances > 0 && correct < length) {
        char letter;
        int found = 0;

        printf("\nWord: %s", guess);
        printf("\nEnter a letter: ");
        scanf(" %c", &letter);

        for (int i = 0; i < length; i++) {
            if (word[i] == letter && guess[i] == '_') {
                guess[i] = lette…
