# CS-532-Count-Keywords-in-a-file

This is a C program to count the number of keywords in a given text file.

I have used a structure with two entries keyword and count.
struct table{
char* keyword;
int count;

};

I have taken a number of keywords and the keywords as main function arguments.
int main(int argc, char** argv)

The bellow statement "malloc" is used to allocate memory for the keywords, and the abc holds the address. Also used free() to release the space.
abc = (struct table*) malloc(argc* sizeof(struct table));

Here C library function getline function is used to read a line at a time from text file.
char *line=NULL;
size_t maxlen=0;
ssize_t n;
while ( (n = getline(&line, &maxlen, stdin)) > 0) {
}

C library function called strtok(), which is used for splitting a string with any given delimiter.
char * linewords = strtok(line, " ");

C library function "strstr" has been used. generally, this function finds the substring in a string. Here I used to find substring null value in a string.
strstr(linewords, "\n")

String functions strlen() and strcmp() are used to the length of the string and to compare the strings respectively.

#How to Compile:
gcc filename.c

"gcc numkeywords.c"

#how to Execute:
./.a.out keywords < filename.txt

"./a.out an the from it was and for or < tale.txt"

#Author
Gowtham Peddineni
