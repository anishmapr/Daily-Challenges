## Daily Challenges

## DC - 25-12-2019(Update the time)
    #include<stdio.h>
    #include <stdlib.h>
    int main(){
    long long int x,y,k;
    scanf("%lld:%lld",&x,&y);
    scanf("%lld",&k);
    while(k>0)
    {
        y++;
        if(y==60)
        {
            y=0;
            x++;
            if(x==24)
            {
                x=0;
            }
        }
        k--;
    }
    if(x<10){ 
    printf("0%d:",x);
    }
    else{
        printf("%d:",x);
    }
    if(y<10){
        printf("0%d",y);
    }
    else{
        printf("%d",y);
        }
    }


## DC - 24-12-2019 (Repeat First/Last X)
    #include<stdio.h>
    int main(){
    int num,x;
    scanf("%d %d",&num,&x);
    if(x>0){
    int ctr=1+x;
    for(int i=1;i<=num;i++){
    if(i<ctr){
    printf("%d %d ",i,i);}
    else{
    printf("%d ",i);}
    }}
    else{
    for(int i=1;i<=num;i++){
    if(i>=n+x){
    printf("%d ",i);}
    else{
    printf("%d %d ",i,i);}
    }}
    }
    

## DC - 23-12-2019 (Smallest Integer in C)
    #include<stdio.h>
    int main(){
    int x,y,z;
    scanf("%d %d %d",&x,&y,&z);
    int num=1;
    while(num){
    if(num%z==0 && !(num>=x && num<=y)){
    printf("%d",num);
    break;
    }
    num++;
    }
    }
