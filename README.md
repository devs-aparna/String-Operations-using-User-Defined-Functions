# String-Operations-using-User-Defined-Functions
A C program to implement following  operations on string using user-defined functions: Comparison of Two Strings, Copying One String into Another, Finding the String Length, Concatenating Two Strings into One.

    #include<stdio.h>
    int StringCopy(char* a,char* b);
    int StringLength(char* a);
    int StringCompare(char* a, char* b);
    int concatenate(char* str1, char* str2);
    int main()
    {
    char string[20];
    printf("Enter the string:\n");
    scanf("%s",&string);
    int len=StringLength(string);
    printf("The length of the string is: %d\n",len);
    
    char string1[20];
    printf("\nEnter the string to be copied:\n");
    scanf("%s",&string1);
    char string2[20];
    StringCopy(string1,string2);
    printf("The copied string is: %s\n",string2);
    
    char strA[20], strB[20];
    printf("\nEnter first string to compare:\n");
    scanf("%s", strA);
    printf("Enter second string to compare:\n");
    scanf("%s", strB);
    int compare = StringCompare(strA, strB);
    if (compare == 1)
        printf("Strings are equal.\n");
    else
       {
          printf("Strings are not equal.\n");
       }
       
     char str1[100],str2[100];  

    printf("\nConcatenated String: %s", str1);
    printf("\nEnter first string:\n");
    scanf("%s",&str1);
    printf("\nEnter second string:\n");   
    scanf("%s",&str2); 
    concatenate(str1,str2);
    printf("The concatenated string is: %s",str1);
       
    return 0;
    }
    int StringLength(char* a)
    {
    int i=0;
    while(a[i]!='\0')
    {
        i++;
    }
    return i;
    }
    int StringCopy(char* a,char* b)
    {
    int i=0,j=0;
    while(a[i]!='\0')
    {
    b[j]=a[i];
    i++;
    j++;
    }
    
    }
    int StringCompare(char* a, char* b)
    {
    int i = 0;
    while (a[i] != '\0' && b[i] != '\0') {
         if ((int)a[i] != (int)b[i]) {
            return 0; 
        }
        i++;
    }
    if (a[i] == '\0' && b[i] == '\0') {
        return 1; 
    } else {
        return 0; 
    }
    }
    int concatenate(char* str1, char* str2) {
    int i = 0, j = 0;
    while (str1[i] != '\0') i++;
    while (str2[j] != '\0') {
        str1[i] = str2[j];
        i++; j++;
    }
    str1[i] = '\0';
    }

