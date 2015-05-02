# mario.c
Pset 1 for Cs50x from edX through harvard

#include <cs50.h>
#include <stdio.h>

int main(void)
{
    // n = height, h = hashes, s = spaces, r = rows
    int n;
    
    
    do //This asks for input till a valid int is given
    {
        printf ("How tall would you like your pyramid?: ");
        n = GetInt();
    }     
    while  (n < 0 || n > 23);
    
    for (int r = 0; r < n; r++)    
    {
        //this determintes spaces
        for (int s = 0; s < n-r-1; s++)
        {
            printf (" ");
        }
        //this determines hashes
        for (int h = 0; h < n+2; h++)
        {
            printf ("#");
        }
        //new line
        printf ("\n");
    }       
}
