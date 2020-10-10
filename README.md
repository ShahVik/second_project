/*
 ============================================================================
 Name        : conditional-statement.c
 Author      : VIKRAM
 ============================================================================
*/
/*
 Problem Statement

A restaurant gives a discount of 10% if the total customer bill including 5% tax is greater than or equal to Rs. 1000.
Write a program for the problem statement mentioned above and print the next payable amount as applicable.

Note: The customer bill needs to be entered by the user and total bill including 5% tax needs to be calculated in the program. 
      If the customer is eligible for the discount, then calculate the net payable amount and print it.
 */

#include <stdio.h>
int main()	{
	float bill,totalBill, netPayableAmount;
	setbuf(stdout,NULL);

	printf("Enter the bill:");
	scanf("%f",&bill);
	 totalBill = bill + 0.05*bill;
	if(totalBill>=1000)	{
		 netPayableAmount= totalBill - 0.1*totalBill;
		 printf("Net Payable Amount is %f", &netPayableAmount);
	 }
	else if (totalBill>=0 && totalBill<=1000)	{
		 netPayableAmount= totalBill;
		 printf("Net Payable Amount is %f", &netPayableAmount);
	 }
	else
		 printf("Invalid Input");
	return 0;
}

