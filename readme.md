#include<stdio.h>
//#include<conio.h>
#include<math.h>
#define pi 3.14159
//BASIC OPERATIONS
void addition();
void subtraction();
void multiplication();
void division();
//ALGEBRIC OPERATIONS
 void exponentiation();
 void squareroot();
 void cuberoot();
 void nthroot();
 void factorial();
 void absolutevalue();
//TRIGONOMETRIC FUNCTIONS
void sine();
#define pi 3.14159
void cosine();
void tangent();
void arcsine();
void arccosine();
void arctangent();
//LOGARITHMIC OPERATIONS
void logarithm();
void natural_logarithm();
void custombase_logarithm();


int main(){
	printf(" \t\t Welcome to scientific calculator! \n\n ");
	int choice;
	
	printf("\n ** press 0 to quit the program ** \n");
	printf(" Enter 1 for addition \n");
	printf(" Enter 2 for subtraction \n");
	printf(" Enter 3 for multiplication \n");
	printf(" Enter 4 for division \n");
	printf(" Enter 5 for exponention \n");
	printf(" Enter 6 for squareroot \n");
	printf(" Enter 7 for cuberoot \n");
	printf(" Enter 8 for nthroot \n");
	printf(" Enter 9 for factorial \n");
	printf(" Enter 10 for absolutevalue \n");
	printf(" Enter 11 for sine \n");
	printf(" Enter 12 for cosine \n");
	printf(" Enter 13 for tangent \n");
	printf(" Enter 14 for arcsine \n");
	printf(" Enter 15 for arccosine \n");
	printf(" Enter 16 for arctangent \n");
	printf(" Enter 17 for logarithm(base 10) \n");
	printf(" Enter 18 for natural_logarithm(base n) \n");
	printf(" Enter 19 for custombase_logarithm \n");
	while(1){
		printf("\n \n  Enter the operation you want to do: \n");
		scanf("%d",&choice);
		switch(choice){
			case 1:
				addition();
				break;
			case 2:
				subtraction();
				break;
			case 3:
				multiplication();
				break;
			case 4:
				division();
				break;
			case 5:
				exponentiation();
				break;
			case 6:
				squareroot();
				break;
			case 7:
				cuberoot();
				break;
			case 8:
				nthroot();
				break;
			case 9:
				factorial();
				break;
			case 10:
				absolutevalue();
				break;	
            case 11:
				sine();
				break;
			case 12:
				cosine();
				break;
			case 13:
				tangent();
				break;
			case 14:
				arcsine();
				break;
			case 15:
				arccosine();
				break;
			case 16:
				arctangent();
				break;
			case 17:
				logarithm();
				break;	
			case 18:
				natural_logarithm();
				break;			
			case 19:
				custombase_logarithm();
				break;			
																										
			
			default:
				printf(" sorry enter the valid option \n");
				
		}
	}
	return 0; 
}
void addition(){
	printf(" Enter the two numbers you want to add :\n");
	int a,b;
	scanf("%d %d",&a,&b);
	printf("The sum of two given numbers are %d \n",a+b);
}
void subtraction(){
	printf(" Enter the two numbers you want to subtract :\n");
	int a,b;
	scanf("%d %d",&a,&b);
	printf("The difference of two given numbers are %d \n",a-b);
}
void multiplication(){
	printf(" Enter the two numbers you want to multiply :\n");
	int a,b;
	scanf("%d %d",&a,&b);
	printf("The product of two given numbers are %d \n",a*b);
}
void division(){
	printf(" Enter the two numbers you want to divide :\n");
	int a,b;
	scanf("%d %d",&a,&b);
	printf("The division of two given numbers are %f \n",(float)a/(float)b);
}
void exponentiation(){
	double b;
	double p;
	printf(" Enter the base and the power :\n");
	scanf("%lf %lf",&b,&p);
	double e=pow(b,p);
	printf("The power is %lf \n",e);
}
void squareroot(){
		double b;
	printf(" Enter the  numbers you want to squareroot :\n");
    scanf("%lf",&b);
    double p=pow(b,2);
	printf("The square root of  given number is  %lf \n",p);
}
void cuberoot(){
		double b;
	printf(" Enter the  numbers you want to squareroot :\n");
    scanf("%lf",&b);
    double p=pow(b,3);
	printf("The square root of  given number is  %lf \n",p);
}
void nthroot() {
    double base;
    int n;
    printf(" Enter the base and the root index (n) :\n");
    scanf("%lf %d", &base, &n);
    
    if (n > 0) {
        double result = pow(base, 1.0 / n);
        printf("The %dth root of %.2lf is %.4lf\n", n, base, result);
    } else {
        printf("Invalid input. Root index  must be greater than 0.\n");
    }
}
void factorial(){
	int n,factorial;
	printf(" Enter the  numbers you want the factorial of  :\n");
	scanf("%d",&n);
	factorial=1;
	for(int i=1;i<=n;i++){
		factorial=factorial*i;
	}
	printf(" the factorial of %d is %d \n",n,factorial);
}

void absolutevalue() {
    double value;
    printf(" Enter the number for absolute value :\n");
    scanf("%lf", &value);

    double result = fabs(value);
    printf("The absolute value of %.2lf is %.4lf\n", value, result);
}



void sine() {
    double angle_degrees;
    printf(" Enter the angle in degrees: ");
    scanf("%lf", &angle_degrees);
    double angle_radians = angle_degrees * (pi / 180.0);
    double result = sin(angle_radians);
    printf("Sine of %.2lf degrees is %.4lf\n", angle_degrees, result);
}
void cosine() {
    double angle_degrees;
    printf("Enter the angle in degrees: ");
    scanf("%lf", &angle_degrees);
    double angle_radians = angle_degrees * (pi / 180.0);
    double result = cos(angle_radians);
    printf("Cosine of %.2lf degrees is %.4lf\n", angle_degrees, result);
}

void tangent() {
    double angle_degrees;
    printf("Enter the angle in degrees: ");
    scanf("%lf", &angle_degrees);
    double angle_radians = angle_degrees * (pi / 180.0);
    double result = tan(angle_radians);
    printf("Tangent of %.2lf degrees is %.4lf\n", angle_degrees, result);
}

void arcsine() {
    double value;
    printf("Enter the value for arcsine (between -1 and 1): ");
    scanf("%lf", &value);

    if (value >= -1 && value <= 1) {
        double result = asin(value) * (180.0 / pi);
        printf("Arcsine of %.4lf is %.2lf degrees\n", value, result);
    } else {
        printf("Invalid input. Value must be between -1 and 1.\n");
    }
}

void arccosine() {
    double value;
    printf("Enter the value for arccosine (between -1 and 1): ");
    scanf("%lf", &value);

    if (value >= -1 && value <= 1) {
        double result = acos(value) * (180.0 / pi);
        printf("Arccosine of %.4lf is %.2lf degrees\n", value, result);
    } else {
        printf("Invalid input. Value must be between -1 and 1.\n");
    }
}

void arctangent() {
    double value;
    printf("Enter the value for arctangent: ");
    scanf("%lf", &value);

    double result = atan(value) * (180.0 / pi);
    printf("Arctangent of %.4lf is %.2lf degrees\n", value, result);
}
void logarithm() {
    double log_, num;
    printf("Enter a number: ");
    scanf("%lf", &num);

    if (num > 0) {
        log_ = log10(num);
        printf("Log base 10 of %.2lf is %.2lf\n", num, log_);
    } else {
        printf("Invalid input number must be greater than 0\n");
    }
}
 void natural_logarithm() {
   double log_, num;
    printf("Enter a number: ");
    scanf("%lf", &num);

    if (num > 0) {
        log_ = log(num);
        printf("Natural logarithm (base e) of %.2lf is %.4lf\n", num, log_);
    } else 
        printf("Invalid input  number must be greater than 0\n");
    }
    void custombase_logarithm() {
    double result, num, base;
    printf("Enter the number and the base for logarithm:\n");
    scanf("%lf %lf", &num, &base);

    if (num > 0 && base > 0 && base != 1) {
        result = log(num) / log(base);
        printf("Logarithm (base %.2lf) of %.2lf is %.4lf\n", base, num, result);
    } else 
        printf("Invalid input. Both the number and base must be greater than 0 and base not to be 1\n");
    
   
}