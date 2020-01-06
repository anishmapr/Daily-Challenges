## Daily Challenges.  
## DC - 06-02-2020 (Larger with * symbol) 
    #include<stdio.h>   
    #include<string.h>
    void function(String str) { 
    int len=strlen(str); 
    int A=0,D=0; 
    for(int index=0;index<len;index++){ 
    if(isalpha(str[index]) 
        A++; 
    if(isdigit(str[index]) 
        D++; 
    } 
    for(int index=0;index<len;index++){ 
    if(A>D && isalpha(str[index])) 
         str[index]='*'; 
    if(D>A && isdigit(str[index]) 
         str[index]='*';  
    }
    int main() { 
    char str[1000]; 
    function(str); 
    printf("%s",str); 
    }
   Input : cratmate123 
     
   Output : ********123 
    
   Explanation :  A-alphabets ; D-digits 
   
   A>D so all alphabets are given * symbol 
   
## DC - 05-02-2020 (Sum of bottom right quad elements in matrix)
    #include<stdio.h>
    #include <stdlib.h>
    int main() {
    int m,n;
    scanf("%d %d",&m,&n);
    int a[m][n],sum=0;
    for(int i=0;i<m;i++) {
        for(int j=0;j<n;j++) {
            scanf("%d",&a[i][j]);
            if(j>=n/2 && i>=m/2)
            {
                sum+=a[i][j];
            }
        }
    }
    printf("%d",sum); }
   
Input :

    4 4
	
    1 2 3 4

    2 3 4 1

    3 4 1 2

    4 1 2 3
	
Output : 8 

Explanation : Sum of bottom right quad is 1+2+2+3 = 8
       
## DC - 04-01-2020 (Sum of digits in Octal representation) 
     #include<stdio.h> 
     int main() { 
     int num,sum=0; 
     scanf("%d",&num); 
     while(num!='\0'){ 
     sum+=(num%8); 
     num/=8; 
     } 
     printf("%d",sum); 
     } 
      
   Input : 12 
   
   Output : 5. 
   
   Explanation : octal of 12 is 14 sum of digits is 1+4=5;
   
   
## DC - 03-01-2020 (SQL Query)  
Table donor: 

CREATE TABLE donor(id INT,name VARCHAR(20),bloodgroup VARCHAR(3));

(select the id,name and bloodgroup which is not AB+ order by name ascending) 

    select id,name,bloodgroup from donor where bloodgroup!='AB+'order by name asc; 
    
    
## DC - 02-01-2020 (Alternate 1s ans 0s decimal equivalent) 
    #include<stdio.h> 
    #include<stdlib.h> 
    #include<math.h> 
    int main() { 
    long long int num,ctr,dec=0,count; 
    scanf("%lld",&num); 
    if(num&1) { 
    count = (num/2)+1; 
    ctr=0; 
    } 
    else{ 
    count = num/2; 
    ctr=1; 
    } 
    while(count) { 
    dec+=(long long int)(pow(2,ctr)); 
    ctr+=2; 
    count--; 
    } 
    printf("%lld",dec); 
    } 
     
   Input : 5 
    
   Output : 21 
   
   Explanation : (10101)5 is odd so count = (5/2)+1 = 3(1's) and ctr=0 
   dec = 21 
    
    
## DC - 01-01-2020 (Sum of odd digit numbers) 
    #include<stdio.h>  
    #include<math.h>
    int main() { 
    int num,size,sum=0; 
    scanf("%d",&size); 
    for(int i=0;i<size;i++){ 
        scanf("%d",&num);  
        int count=log10(num)+1; 
        if(count%2!=0)
             sum+=num; 
    } 
    printf("%d",sum); 
    }
	
   Input :  
   
   4 
    
   10 200 300 4000 
    
   Output : 500
      
   Explanation : odd digit count numbers are 200 and 300 so the sum is 500
	
	
## DC - 31-12-2019 (Left Right Pattern)
    #include <stdio.h>
    #include<string.h>
    int main(){
    char s[1000];
    scanf("%s",s);
    int len = strlen(s);
    int n=len,flag = 0,x=0,y=len;
    if(n%2==0)
    {
        n=n-1;
    }
    for(int i=0;i<n;i++)
    {
        for(int j=0;j<x;j++)
        {
            printf("#");
        }
        for(int j=x;j<y;j++)
        {
            printf("%c",s[j]);
        }
        for(int j=len-1;j>=y;j--)
        {
            printf("#");
        }
        if((x==len/2 && len % 2!=0)||(x==(len/2)-1 && len%2==0))
        {
            flag = 1;
        }
        if(flag==1)
        {
            x--;
            y++;
        }
        if(flag==0)
        {
            x++;
            y--;
        }
        printf("\n");
    }}

Input : logics

Output:

   logics
   
   #ogic#
   
   ##gi##
   
   #ogic#
   
   logics


## DC - 30-12-2019 (password validation) 
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
     
     
## DC - 29-12-2019 (getNumberOfBinaryOnes in Integer)
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
		
		
## DC - 28-12-2019 (Remove Brackets)
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
