# Prime-Factors-of-a-number-in-C

Find Prime Factors of a number
Today in this article we will learn about how to find Prime Factors of a number .

Any natural number which is greater than 1 and has only two factors i.e., 1 and the number itself is called a prime number.

Lets understand this with the help of example :- 

Input:- 24
Output:- 2, 2, 2, 3

Here the prime factor of 24 is 2, 2, 2, 3 that is if we multiply 2*2*2*3 = 24. If the input number is 35 then the prime factors  is equal to 5, 7.

Prime Factors of a Number
Algorithm
First take the number lets say num for which we need to find the factors.
Make a function prime factors that will print all the factors of the number.
Start the loop from i = 2 till the value of num > 1
Inside the for loop make a while loop with condition (num%i == 0) this will check if i divides the number. 
Inside the while loop print the value of i and divide num by i.
Prime Factors of a number
Method 1 Code in C :-
Run
#include <stdio.h>
void primefactor(int num) {
    printf("Prime factors of the number : ");     
    for (int i = 2; num > 1; i++) {
                  while (num % i == 0) {
                        printf("%d ", i);             
                        num = num / i;         
                       }     
                   } 
                } 
int main() {
      int num;     
      num=12;
      primefactor(num);     
     return 0; 
}
Output:-
Enter the positive integer: 24
Prime factors of the number : 2 2 2 3
Related Pages
Power of a number

Factor of a number

Finding Prime Factors of a number

Strong number

Perfect number

Perfect Square

Method 2 (Efficient)
 First Print the number of 2s that is n divisible by 2. 
 After step 1, the value of n must be odd. Now start a loop from i = 3 till the square root of n. While i divides n, print i, and divide n by i. 
After i fails to divide n, increment i by 2 and continue. 
 If n is a prime number and is greater than 2, then n will not become 1 by the above two steps. 
So print n if it is greater than 2.
Method 2 Code in C :-
Run
#include <stdio.h>
#include <math.h>

void primefactors(int n) {
// Print the number of 2s that divide n             
while (n % 2 == 0) {                
printf("%d ", 2);                
n = n / 2;                 }
// n must be odd at this point.  So we can skip ne element (Note i = i +2)
for (int i = 3; i <= sqrt(n); i = i + 2) {  
                 // While i divides n, print i and divide n          
while (n % i == 0) {                       
     printf("%d ", i);                   
     n = n / i;                          
   }              
  }          
//This condition is to handle the case when n is a prime number greater than 2   
  if (n > 2)  {
printf("%d ", n);
 }
 int main() {       
 int number = 24;        
printf("Prime factor of the number: ");        
primefactors(number);       
 return 0; 
}
Output:-
Prime factor of the number: 2 2 2 3 
