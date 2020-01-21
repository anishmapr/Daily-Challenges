## Daily Challenges...  
## DC - 21-01-2020 (N odd/even numbers) 
    int *getOddEvenNum(int N) { 
    int *a=malloc(N*size(int));  
    int c=0,k=0,i=1;
    if(N&1) { 
        while(c<=N) { 
            if(i&1) { 
            a[k++]=i;
            c++; 
            } 
            i++; 
        } 
    } 
    else{ 
        while(c<=N){ 
            if(i&1==0) { 
            a[k++]=i; 
            c++; 
            }
            i++; 
         } 
    }  
    return a; 
    } 
     
   Input : 5 
    
   Output : 1 3 5 7 9 
    
   Explanation : 5 is odd so first five odd numbers are printed
## DC - 20-01-2020 (SQL select Query)  
  Table user: 
    
    create table user(id INT,name VARCHAR(10),role VARCHAR(10)); 
      
  Query: 
  
    select id,role,name from user order by role,id desc; 
    
## DC - 19-01-2020 (double even and quad odd)
    #include<stdio.h>
    #include<stdlib.h>
    int main(){
        int len,num,sum=0;
        scanf("%d",&len);
        for(int index=0;index<len;index++)
	    {
            scanf("%d",&num);
            if(num%2==0)
                sum+=(num*2);
            else
                sum+=(num*4);
        }
        printf("%d",sum);
    }
    
   Input :
   
    4
    5 2 8 7
    
   Output : 68
   
   Explanation : 
   
    odd  - 5*4=20
    even - 2*2=4
    even - 8*2=16
    odd  - 7*4=28
    sum = 68
   
   
## DC - 18-01-2020 (Sum of integers ending with x)
    import java.util.*;
    public class Hello {
    public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		int n=sc.nextInt();
		String x=sc.next();
		int l=x.length();
		int sum=0,f=0;
		for(int i=0;i<n;i++)
		{
		    String s=sc.next();
		    int len=s.length();
		    int a=len-1,c=0;
		    for(int j=l-1;j>=0 && len>l;j--)
		    {
		        if(s.charAt(a)==x.charAt(j))
		        {
		            c++;
		        }
		        a--;
		    }
		    if(c==l)
		    {
		        sum+=Integer.parseInt(s);
		    }
		}
		System.out.print(sum);
	}
    }
    
  Input :
     
      4 40
      140 230 540 100
      
  Output : 680
  
  Explanation : The integers ending with 40 is 140 and 540 so the sum = 140+540 = 680
	  
## DC -17-01-2020 (Find side of Rectangle)
    #include<stdio.h>
    #include<stdlib.h>
    int main(){
    long int length,peri;
    scanf("%ld %ld",&length,&peri);
    double breadth=(peri/2.0)-length;
    printf("%0.2lf",breadth);
    }
    
   Input : 4 12
   
   Output : 2.00
   
   Explanation:
   
     Perimeter = 2*(length+breadth)
     breadth = (perimeter/2)-length
     
     
## DC - 16-01-2020 (SQL Select Query)
 TABLE EVENT:
 
    create table event(id int,title varchar[100],type varchar[10],attendeescount int,active boolean);
    
 Select Query:
 
    select id,title,attendeescount from table where active=true and type='TECH' and attendeescount>50
    order by id asc;
    
## DC - 15-01-2020 (Toogle char in string) 
    #include<stdio.h> 
    #include<string.h>
    #include<ctype.h>
    int main(){ 
    char s1[1000],s2[1000]; 
    scanf("%s\n%s",s1,s2); 
    for(int i=0;i<strlen(s1);i++) { 
    if(tolower(s2[i])=='u'){ 
    printf("%c",toupper(s1[i])); 
    } 
    else{ 
    printf("%c",tolower(s1[i])); 
    } 
    } 
    }  
    
  Input: 
  
    cRaTMatE 
    ulULuLuL
       
   Output: 
     
     CrAtMaTe 
      
   Explanation : 
    
    if s2 char has u or U toogle s1 char to uppercase 
    if s2 char has l or L toogle s1 char to lowercase
   
## DC - 14-01-2020 (getStringfromInteger) 
    #include<stdio.h>
    #include<stdlib.h>
    char* getStringfromInteger(int num){
    int k=0;
    char *str=malloc(sizeof(char)),c='a';
    while(num>0){
    str[k]=c++;
    if(c=='d'){
    c='a';
    }
    k++;
    num--;
    }
    str[k]='\0';
    return str;
    }
    int main(){
    int num;
    scanf("%d",&num);
    char *str=getStringfromInteger(num);
    printf(str);
    free(str);
    return 0;
    }
    
   Input : 5
   
   Output : abcab
   
   
## DC - 13-01-2020 (Flowchart -> Code)
    #include<stdio.h>
    #include <stdlib.h>
    int main() {
    int x,y;
    scanf("%d %d",&x,&y);
    int ctr1=1,ctr2=y;
    while(ctr1<=x || ctr2>=1) {
        if(ctr1<=x) {
            printf("%d ",ctr1);
            ctr1++;
        }
        if(ctr2>=1) {
            printf("%d ",ctr2);
            ctr2--;
        }
    }}

## DC - 12-01-2020 (Column increment/decrement pattern)
    #include<stdio.h>
    #include <stdlib.h>
    int main(){
    int num,k=1;
    scanf("%d",&num);
    int arr[num][num];
    for(int col=0;col<num;col++){
    for(int row=col;row<num;row++){
    arr[row][col]=k;
    col%2?--k:k++;
    }
    if(col%2)
        k=1;
    else
        k=num;
    }
    for(int row=0;row<num;row++){
    for(int col=0;col<=row;col++){
    printf("%d ",arr[row][col]);
    }
    printf("\n");
    }
    }
    
   Input : 5
   
   Output :
        
    1
    2 5
    3 4 1
    4 3 2 5
    5 2 3 4 1
	
	
## DC - 11-01-2020 (Free sweets exceed x kg)
    #include<stdio.h>
    #include <stdlib.h>
    int main(){
    int n,x,y,sum=0,m;
    scanf("%d %d %d",&n,&x,&y);
    for(int i=0;i<n;i++){
        scanf("%d",&m);
        if(m>x){
            m+=y;
        }
        sum+=m;
    }
    printf("%d",sum);
    }

Input : 
   
    5 10 4
    6 10 13 20 3
    
Output : 60

Explanation : 

    13>10-> 13+4=17
    20>10-> 20+4=24
    total weight = 6+10+17+24+3 = 60kg
       
    
## DC - 10-01-2020 (Rotate clockwise and print largest)
    #include<stdio.h>
    int main(){
    int num;
    scanf("%d",&num);
    int c=(int)(log10(num)+1);
    int power=pow(10,c-1);
    long int max=num;
    for(int i=0;i<c;i++){
    int f=num/power;
    long int r=(num*10)+f;
    long int z=r-(f*power*10);
    if(z>max){
    max=z;
    }
    num=z;
    }
    printf("%ld",max);
    }
    
   Input : 2451
    
   Output : 5124
   
   Explanation :
   
    max = num = 2451
    num = 2451*10 = 24510+2 = 24512-(2*1000*10) = 24512-20000 = 4512 > max => max = 4512
    num = 4512*10 = 45120+4 = 45124-(4*1000*10) = 45124-40000 = 5124 > max => max = 5124
    num = 5124*10 = 51240+5 = 51245-(5*1000*10) = 51245-50000 = 1245 < max => max = 5124
    num = 1245*10 = 12450+1 = 12451-(1*1000*10) = 12451-10000 = 2451 < max => ( max = 5124 )
    
## DC - 09-01-2020 (Integers with same digits)
    #include<stdio.h>
    #include<string.h>
    int main(){
    int num,x=0;
    char str[100000000];
    scanf("%d",&num);
    for(int i=0;i<num;i++){
    scanf("%s",str);
    int len=strlen(str);
    int flag=0;
    char c=str[0];
    for(int i=0;i<len;i++){
    if(c!=str[i]){
    flag=1;
    break;
    }}
    if(flag==0){
    x=1;
    printf("%s",str);
    }}
    if(x==0){
    printf("-1");
    }}
   
  Input :
      
    5
      
    85 234 222 55555 65
      
  Output :
      
    222 55555
   
  Explanation : 
  
    Inputting the array integers as string and comparing first char is equal to all other characters if yes then print
   
## DC - 08-01-2020 (SQL Query-Select) 
   Table bus is given select id and busregnum
   where ac is false sleeper and seater is tru,id should be ordered in asc.
     
      create table bus(id int,busregistrationnum varchar[20],ac boolean,sleeper boolean,seater boolean);
     
   Sql Query : 
   
      select id,busregistrationnum from bus where not ac and sleeper and seater order by id asc; 
   
## DC - 07-01-2020 (Convert c to python)  
  C code :
  
    #include<stdio.h> 
    #include<stdlib.h>  
    int main(){  
    int N;  
    scanf("%i",&N);  
    printf("%i",N);
    } 
     
  Python :
  
    N=input();  
    if(N[0]=='0' and N[1]=='x' or N[1]=='X'): 
        print(int(N,16));    
    elif(N[0]=='0'): 
        print(int(N,8));  
    else: 
        print(N); 
		  
   Input : 012
   
   Output : 10 
    
   Explanation : 
    
    * %i will input integers of octal decimal hexadecimal or binary type and print it in decimal type
    * To input integer of octal type 0 is preceeded ex:012
    * To input integer of hexadecimal type 0X or 0x is preceeded ex:0x12
	 
## DC - 06-01-2020 (Hidepassword) 
    #include<stdio.h>   
    #include<stdlib.h>
    #include<string.h>
    #include<ctype.h>
    void hidePassword(char str[]){ 
    int len=strlen(str); 
    int A=0,D=0; 
    for(int index=0;index<len;index++){ 
    if(isalpha(str[index]))
        A++; 
    if(isdigit(str[index]))
        D++; 
    } 
    for(int index=0;index<len;index++){ 
    if(A>D && isalpha(str[index])) 
         str[index]='*'; 
    if(D>A && isdigit(str[index]))
         str[index]='*';  
    }
    }
    int main() { 
    char str[1000]; 
    scanf("%s",str);
    hidePassword(str); 
    printf("%s",str); 
    } 
    
   Input :   
   
    cratmate123 
     
   Output :   
   
    ********123 
    
   Explanation :  
   
       A-alphabets ; D-digits 
   
       A>D so all alphabets are given * symbol 
   
## DC - 05-01-2020 (Sum of bottom right quad elements in matrix)
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
