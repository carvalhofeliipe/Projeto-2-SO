//Felipe Carvalho de Alencar, RA:10409804 
//Helen Beatriz Motta, RA:10403718 
//Priscila Tomé dos Santos, RA: 10403649

#include <stdlib.h>
#include <stdio.h>

int main(){
    int n;
    int c;
    int m;
    int s;
    int t;
    int ca;
    int v;
    char a;
    char d;
    
    a = '4';
    m = 1;
    s = 0;
    t = 0;
    v = 0;

    scanf("%d", &n);
    for(int i = 0; i < n; i++) {
        scanf("%d %c", &c, &d);
        if(d != a){
            if(v > 0){
                if((c - ca) > 10){
                    s += c - ca - 10;
                }
                m++;
                v--;    
            }
            if(i == 0) t = c;
            else v++;
            ca = t;
            a = d;
        }
        t = c;
    }

    int r = c + (10 * m) - s;
    printf("%d\n", r); 

    return 0;
}
