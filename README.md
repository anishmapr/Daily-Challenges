## Daily Challenges 
## DC - 30-12-2017 (password validation) 
     #include<stdio.h> 
     #include<stdlib.h>  
     int valid(char c,char* user) { 
     for(int index=0;index<strlen(user);index++){ 
     if(user[index]==c){ 
     return 0; 
     }  
     }
     return 1; 
     }
     int main() { 
     char user[1000],pass[1000];  
     scanf("%s\n%s",user,pass);
     int len=strlen(pass); 
     for(int index=0;index<len;index++) { 
     if(valid(pass[i],user)==0) {  
     flag=1;
     printf("INVALID"); 
     break;
     } 
     } 
     if(f==1){ 
     printf("VALID"); 
     } 
     } 
      
      
  Input :   
  
  cratmates 
  
  123@2000 
	     
  Output : VALID 
  
  Explanation : If password contains username characters print invalid else valid
     
     
## DC - 29-12-2017 (getNumberOfBinaryOnes in Integer)
    #include<stdio.h>
    #include <stdlib.h>
    int getNumberOfBinaryOnes(int N) {
        int count = 0; 
        while(N>0) {
	    count += (N%2);
	    N /= 2;
	    }
	    return count;
    }
    int main()
    {
      int num1,num2;
	  scanf("%d %d",&num1,&num2);
	  int N = num1^num2;
	  printf("%d",getNumberOfBinaryOnes(N));
    }
	
  Input = 15 0
  
  Output = 4
  
  Explanation : num1 = 15 ; num2 = 0 ; N = (15^0) = (1111 ^ 0000) = (1111) = 15
                ; number of ones in binary 15(1111) = 4.
		
		
## DC - 28-12-2017 (Remove Brackets)
    #include<stdio.h>
    #include <stdlib.h>
    int main(){
         char str[1000];
         scanf("%s",str);
	 int len=strlen(str);
         for(int index=0;index<len;index++) {
             if(str[i]!='[' && str[i]!=']' && str[i]!='(' && str[i]!=')' && str[i]!='{' && str[i]!='}') {
	           printf("%c",str[i]);
             }
        }}
	
	
   Input : De(v)o{i}d
  
   Output : Devoid
        
   
## DC - 27-12-2019 (Sum of three digits in number)
    import java.util.*;
    public class Hello {
    public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		String s=sc.next();
		int c=0,sum=0;
		String x="";
		for(int i=0;i<s.length();i++) {
		    if(c!=3) {
		        x+=s.charAt(i);
		        c++;
		    }
		    if(c==3) {
		        int n=Integer.parseInt(x);
		        sum+=n;
		        x="";
		        c=0;
		    }
		}
		System.out.print(sum);
	}}
	
	
   Input : 100100
   
   Output : 200
    
    
## DC - 26-12-2019 (Print N characters clockwise)
    #include<stdio.h>
    #include <stdlib.h>
    int main(){
        int num,ctr=1,i=0;
        scanf("%d",&num);
        char ch[]="abcd";
        while(ctr<=num)
        {
             printf("%c",ch[i]);
             if(i==strlen(ch)-1)
                 i=0;
             else
                 i++;
             ctr++;
         }}
         
   Input : 5
   
   Output : abcda 
   
   
## DC - 25-12-2019 (Update the time)
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
