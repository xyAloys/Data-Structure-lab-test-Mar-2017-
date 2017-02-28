# Data-Structure-lab-test-Mar-2017-

#include <stdio.h>
int numDigits1(int num);
void numDigits2(int num, int *result);
int main()
{
	int number, result = -1;
	printf("Enter the number:\n");
	scanf("%d",&number);
	printf("numDigits1() : %d\n", numDigits1(number));
	numDigits2(number, &result);
	printf("numDigits2(): %d\n", result);
	scanf("\n");
	return 0;
}
int numDigits1(int num)
{
	int count = 0;
	do {
		num = num / 10;
		count++;		
	} while (num != 0);
	return count;
}
void numDigits2(int num, int *result)
{
	int count = 0;
	do
	{
		num=num / 10;
		count++;
	} while (num!= 0);
	*result = count;
	return;
}
