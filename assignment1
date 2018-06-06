//
//  main.c
//  3120A1
//
//  Created by Al Brink on 2018-06-01.
//  Copyright © 2018 Al Brink. All rights reserved.
//

#include <stdio.h>
#include <unistd.h>

#define MAX_LINE 80 /* Maximum length command */

int main(void) {
    
    
    /* Variables and arrays */
    
    char *args[MAX_LINE/2 + 1]; /* Command line argument */
    int should_run = 1; /* Flag to determine when to exit program */
    char userCommand[81]; /* The user command to be executed */
    char userCommandHistory[100][80]; /* History of user commands  */
    int userCommandIndex = 0; /* Current # of commands issued by user */
    
    
    /* Shell */
    
    while (should_run) {
        
        printf("CSCI3120>");
        fflush(stdout);
        
        /* Read in and process user command */
        fgets(userCommand, 81, stdin);
        
        printf("%s", userCommand);
        printf("\n");

        if (userCommand[strlen(userCommand) - 1] != '\n') {
            printf("Input too long.\n");
            fflush(stdin);
        }
        else {
            //store string for history function
            strcpy(userCommandHistory[userCommandIndex], userCommand);
            userCommandIndex++;
            
            //tokenize string and input into args
            
            //fork here and have child process command by passing in args
            
        }
        
        /* History function */
        

        if(strcmp(userCommand, "history\n")==0){
            
            int i=userCommandIndex;
            while (1){
                printf("%d", i);
                printf(" ");
                printf("%s", userCommandHistory[i]);
                printf("\n");
                i--;
                if(i==0){
                    break;
                }
            }
        }

        fflush(stdin);

    }
    return 0;
}