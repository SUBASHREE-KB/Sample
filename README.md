### C Program - Palindrome or not
```c
//Program to check if the string is palindrome or not
#include<stdio.h>
#include<string.h>
int main()
{
        char str1[20],str2[20],temp;
        int len=0,i=0,j=0;
        printf("Enter string: \n");
        scanf("%s",str1);
        strcpy(str2,str1);
        len=strlen(str1);
        j=len-1;
        while(i<len/2)
        {
                temp=str1[i];
                str1[i]=str1[j];
                str1[j]=temp;
                i++;j--;
        }
        if((strcmp(str1,str2))==0)
                printf("%s is a palindrome",str1);
        else
                printf("%s is not a palindrome",str1);
        return 0;
}
```
