# Pointers_functions-C-
#include<stdio.h>

//Q1. Addition
/*
int sum(int a,int b){
	int c = a+b;
	return c;
}

int main(){
	int a,b;
	printf("Enter Two Numbers with a Gap Between: ");
	scanf("%d %d",&a,&b);
	printf("The Answer is : %d",sum(a,b));
}
*/
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
//Q2. Permutation and combination
/*
int factorial(int x){
	int fact =1;
	for(int i=2;i<=x;i++){
		fact = fact*i;
	}
	return fact;
}

int main(){
	int n;
	printf("Enter n: ");
	scanf("%d",&n);
	int r;
	printf("Enter r: ");
	scanf("%d",&r);
	
	int ncr = factorial(n)/(factorial(r)*factorial(n-r));
	printf("%d",ncr);
	return 0;
}
*/
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
//Q3. Pascal Triangle half above
//int factorial(int x){
//	int fact =1;
//	for(int i=2;i<=x;i++){
//		fact = fact*i;
//	}
//	return fact;
//}
//int combination(int n,int r){
//	int ncr = factorial(n)/(factorial(r)*factorial(n-r));
//	return ncr;
//}

//Pascal Triangle
//int main(){
//	int n;
//	printf("Enter n: ");
//	scanf("%d",&n);
//	for(int i=0;i<=n;i++){
//		int first = 1;
//		for(int j=0;j<=i;j++){
//			printf("%d ",first);
//			first = first*(i-j)/(j+1);
//			
//		}
//		printf("\n");
//	}
//	return 0;
//}
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
//Q4. Swap Numbers with Third Variables

//int main(){
//	int a,b,temp;
//	printf("Enter the values of A and B : ");
//	scanf("%d %d",&a,&b);
//	temp = a;
//	a=b;
//	b=temp;
//	printf("The Swapped Values of A: %d and B: %d",a,b);
//	return 0;
//}
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
//Q5.Swap Numbers without Third Variable
/*
int main(){
	int a,b;
	printf("Enter the values of A and B : ");
	scanf("%d %d",&a,&b);
	a=a+b;
	b=a-b;
	a=a-b;
	printf("The Swapped Values of A: %d and B: %d",a,b);
}
*/
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
// Q6. Swap By Reference 
/*
void swap(int* x,int* y){
	int temp;
	temp=*x;
	*x=*y;
	*y=temp;
	return;
}

int main(){
	int a,b;
	printf("Enter the values of A and B : ");
	scanf("%d %d",&a,&b);
	swap(&a,&b);
	printf("The Swapped Values of A: %d and B: %d",a,b);
}
*/
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------
//Q7. To find GCD(Greatest Common Divisor)

int min(int a,int b){
	if (a<b) return a;
	else return b;
}
int gcd(int a,int b){
	int hcf;
	for (int i=min(a,b);i>=1;i--){
		if(a%i==0 && b%i==0){
			hcf=i;
			break;
		}
	}
	return hcf;
}

int main(){
	int a,b;
	printf("Enter Two numbers : ");
	scanf("%d %d",&a,&b);
	int hcf = gcd(a,b);
	printf("The HCF/GCD of %d and %d is : %d",a,b,hcf);
	return 0;
}
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------
