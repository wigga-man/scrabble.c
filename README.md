#include <cs50.h>
#include <stdio.h>
#include<ctype.h>
#include<string.h>
// Points assigned to each letter of the alphabet
int POINTS[] = {1, 3, 3, 2, 1, 4, 2, 4, 1, 8, 5, 1, 3, 1, 1, 3, 10, 1, 1, 1, 1, 4, 4, 8, 4, 10};

int compute_score(string word);

int main(void)
{
    
    string word1 = get_string("Player 1: ");
    string word2 = get_string("Player 2: ");

    // Score both words
    int score1 = compute_score(word1);
    int score2 = compute_score(word2);

    if(score1>score2) {
    printf("Player1 wins\n");
    }
    else if (score2>score1) {
    printf("Player2 wins\n");
    }
    else {
    printf("TIE\n");
}

int compute_score(string word)
{
    // TODO: Compute and return score for string
    int index,sum=0;
    for(int i=0;i<strlen(word);i++) {
    index=(int)word[i];
    
    if(index>=65 && index<=90) {
    sum=sum+POINTS[INDEX-65];
    }
    else {
    sum=sum+POINTS[INDEX-97];
    }
    return sum;
    
    
}
