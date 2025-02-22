//Code on NAVIE base string matching


#include <stdio.h>



#include <string.h>

void sort(char *txt, char *pat);

int main()


{
    
    
    char txt[] = "AABAABABAABAABA"; 
    
    
    char pat[] = "AABA";             
    
    
    sort(txt, pat);
    
    
    return 0;
}

void sort(char *txt, char *pat)


{
   
    int m = strlen(pat);
    
    int n = strlen(txt);
    
    int i, j;

    
    for(i = 0; i <= n - m; i++) 
    {
        for(j = 0; j < m; j++)   
        {
            if(txt[i + j] != pat[j])
            {
                break;
            }
        }
        
        if(j == m)
        {
            printf("The pattern is found at index %d\n", i);
        }
    }
}


//Output:




![image](https://github.com/user-attachments/assets/1b1e8395-d50e-4e6a-b8d0-4545752a8afc)
