// This is a program for practice and also to make me understand the concept of resize and padding of BMP file

#include <stdio.h>
#include <stdlib.h>
#include <string.h>


//prompt users to enter
int main(int argc, char *argv[])
{
    if (argc != 4)
    {
        fprintf(stderr, "The right format is: ./resize0 integer char outfile\n");
        return 1;
    }

    char *size = argv[1]; //how many number would you want to print (will be shown in n*n array)
    char *symbol = argv[2]; //what letter (or symbol) would you want to print
    char *outfile = argv[3];//write all these in an .txt file, named by yourself

    int number = atoi(size);

    if (number <= 0)
    {
        fprintf(stderr, "Please enter an integer larger than but not equal to 0\n");
        return 2;
    }

    // open output file
    FILE *outptr = fopen(outfile, "w");
    if (outptr == NULL)
    {
        fprintf(stderr, "Could not create %s.\n", outfile);
        fclose(outptr);
        return 3;
    }

    //print an n*n array
    //also write this n*n array in an file called result.txt
    for (int i = 0; i < number; i++)
    {
        for (int j = 0; j< number; j++)
        {
            printf("%s ", symbol);
            fwrite(symbol, sizeof(char), 1, outptr);
            fwrite(" ", sizeof(char), 1, outptr);
        }
        printf("\n");
        fwrite("\n", sizeof(char), 1, outptr);
    }
    // close output file
    fclose(outptr);
    return 0;
}
