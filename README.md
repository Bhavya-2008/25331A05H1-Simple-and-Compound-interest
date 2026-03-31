#include <stdio.h>
#include <math.h> // Essential for the pow() function
int main()
{
    float principal, rate, time, si, ci;
    printf("Enter Principal amount: ");
    scanf("%f", &principal);
    printf("Enter Rate of interest: ");
    scanf("%f", &rate);
    printf("Enter Time (in years): ");
    scanf("%f", &time);
    // Calculating Simple Interest
    si = (principal * rate * time) / 100;
    // Calculating Compound Interest
    // pow(base, exponent) calculates (1 + r/100) raised to the power of time
    ci = principal * (pow((1 + rate / 100), time)) - principal;
    printf("\nSimple Interest: %.2f", si);
    printf("\nCompound Interest: %.2f\n", ci);
    return 0;
 }

