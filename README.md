#include <stdio.h>
#include <stdlib.h>

int main()
{
    int z=0;
    printf("Koji zadatak ste dobili unesi 1,2,3?\t");
    scanf("%d",&z);
if(z==1 || z==2){
    int Q,p1,p2,x,t,n=1,P;
    int T1,T2;
    printf("Formule su:\n");
    printf("T1=p1-k1*t+k1*(x+1)*(?-Q)\n");
    printf("T2=p2-k2*t+k2*(x+1)*(?-Q)\n");
    printf("Unesi ?=  ");
    scanf("%d",&P);
    printf("Unesi brindeksa=  ");
    scanf("%d",&x);
    printf("\nUnesi ulog 1.preduzeca p1=  ");
    scanf("%d",&p1);
    printf("\nUnesi ulog 2.preduzeca p2=  ");
    scanf("%d",&p2);
    printf("\nUnesi troskove proizvodnje po komadu =  ");
    scanf("%d",&t);
    int k;
    printf("Unesi koliko ima kolona/redova:");
    scanf("%d",&k);
    printf("Unesi vrednosti\n");
    int niz[k],i=0,k1=k;
    while(k)
    {
        printf(" vrednost=  ");
        scanf("%d",&niz[i]);
        i++;
        k--;
    }
    printf("\n");
    int j=0;
    for(i=0;i<k1;i++)
        printf("| %d ",niz[i]);
printf("\n");
for(int n=0;n<k1;n++){
    for(i=0;i<k1;i++)
        {
    Q=niz[j]+niz[i];
    T1=-p1-niz[j]*t+niz[j]*(x+1)*(P-Q);if(niz[j]==0)T1=0;
    T2=-p2-niz[i]*t+niz[i]*(x+1)*(P-Q);if(niz[i]==0)T2=0;
    printf("|(%d,%d)",T1,T2);

        }
    j++;
    printf("\n");
}

        /*
do{
    printf("\nUnesi k1=\t");
    scanf("%d",&k1);
    printf("\nUnesi k2=\t");
    scanf("%d",&k2);
    Q=k1+k2;
    T1=-p1-k1*t+k1*(x+1)*(P-Q);if(k1==0)T1=0;
    T2=-p2-k2*t+k2*(x+1)*(P-Q);if(k2==0)T2=0;
    printf("\nKoordinate:(%.2lf,%.2lf)",T1,T2);
    printf("\n_________________________________________");

    }while(n);

}/*
else{
  int k1,k2,p1,p2,x,t1,t2,n=1;
    double T1,T2;
    printf("Formule su:\n");
    printf("T1=p1-k1*t+k1*(x+1)*400\n");
    printf("T2=p2-k2*t+k2*(x+1)*400\n");


    printf("Unesi brindeksa=\t");
    scanf("%d",&x);
    printf("\nUnesi ulog 1.preduzeca p1=\t");
    scanf("%d",&p1);
    printf("\nUnesi ulog 2.preduzeca p2=\t");
    scanf("%d",&p2);
    printf("\nUnesi troskove proizvodnje po komadu za 1. preduzece =\t");
    scanf("%d",&t1);
     printf("\nUnesi troskove proizvodnje po komadu za 2. preduzece =\t");
    scanf("%d",&t2);

do{
    printf("\nUnesi k1=\t");
    scanf("%d",&k1);
    printf("\nUnesi k2=\t");
    scanf("%d",&k2);

    T1=-p1-k1*t1+k1*(x+1)*400;if(k1==0)T1=0;
    T2=-p2-k2*t2+k2*(x+1)*400;if(k2==0)T2=0;
    printf("\nKoordinate:(%.2lf,%.2lf)",T1,T2);
    printf("\n_________________________________________");

    }while(n);




*/
}
    return 0;
}
