# Find-HCF-of-a-Number-using-Recursion-in-C

Find the HCF of the Numbers using Recursion in C
Given two integer inputs num1 and num2, The objective is to write a program to Find the HCF of the Numbers using Recursion in C. The HCF is the Highest Common Factor of the two integer inputs num1 and num2.

For instance,

Input : num1 = 15 , num2 = 20
Output : H.C.F of 15 and 20 is 5.
Find HCF of a Number using Recursion in C
Find the HCF of a Numbers using Recursion in C
The objective of the code is recursively find the H.C.F the Highest Common Factor of the given two integer inputs num1 and num2. In order to do so we’ll define a recursive function hfc() which returns an integer data type and accepts two integer values as arguments. We set the base case as num2 == 0, When the num2 = 0 we return num1. We recursively call the function otherwise such that we replace num2 with the remainder of num1/num2 and num1 by num2.

Let’s try and understand this problem in detail using an example. Let the two input integer values be num1 = 15 and num2 = 10. Now we check if num2 ==0, which is false so we recursively call the function but this time the arguments num1 and num2 will be 10 and 5 respectively. We again check if num2 is 0 which is not true, therefore we’ll again recursively call the function with num1 and num2 as 5 and 0. Now when we check if num2 ==0, the base case is satisfied and therefore we return 5 as the output. 

Find H.C.F of the Numbers using Recursion in C
C Code
#include <stdio.h>

int hcf(int n1, int n2) {
    if (n2 != 0)
        return hcf(n2, n1 % n2);
    else
        return n1;
}


int main() {
    int n1 = 202, n2 = 300;
    printf("L.C.M of %d and %d is %d.", n1, n2, hcf(n1, n2));
    return 0;
}
Output
H.C.F of 202 and 300 is 2.
Explanation

The objective of the code is to recursively find the Highest Common Factor H.C.F of the given two integer input num1 and num2. We define a Recursive function with base case as num2 == 0 and keep replacing num2 with the remainder of num1/num2.

The algorithm for the above code is as follows,

Include the required Libraries using include keyword.
Define a Recursive function hcf() which accepts two interger values.
Set the base case as if n2 == 0 return n1. 
With each recursive step call we replace n2 with the remainder of n1/n2 and n1 by n2.
 In the int main() section well initialize the required variables and print out the output returned by the function call.
The output for the above code is H.C.F of 202 and 300 is 2. 
