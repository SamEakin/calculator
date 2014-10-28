calculator
==========

#include <stdio.h>
#include <stdlib.h>
#include <math.h>

#define PI 3.14159 //define PI for use in calculations
#define height 2.54 //constant for inches to cm

//void circle(void);
//void cyclinder(void);
//void square(void);
//void cube(void);

int main(void){
	int i = 0;
	float r;
	float h;
	float w;
	float l;
	float volume;
	
	while (i != 5) {
		puts("Welcome to my Calculator:");
		puts("Select a shape to find volume:");
		puts("------------------------------");
		puts("1.Circle");
		puts("2.Cylinder");
		puts("3.Square");
		puts("4.Cube");
		puts("------------------------------");
		puts("5.Your height in cm");
		puts("6.Temperature in C");
		puts("==============================");
		puts("Any Number.EXIT");
		scanf("%d", &i);


		if (i == 1) { //circle
			puts("Enter radius of the circle: ");
			scanf("%f", &r);
			volume = PI * r * r;
			printf("The Area of the circle is: %.2f\n\n", volume);
		}
		else if (i == 2) { //cylinder
			puts("Enter radius of the cylinder: ");
			scanf("%f", &r);
			puts("Enter height of the cylinder: ");
			scanf("%f", &h);
			volume = PI * r * r * h;
			printf("The Volume of the cylinder is: %.2f\n\n", volume);
		}
		else if (i == 3) { //square
			puts("Enter width of the square: ");
			scanf("%f", &w);
			puts("Enter height of the square: ");
			scanf("%f", &h);
			volume = w * h;
			printf("The Area of the Square is: %.2f\n\n", volume);
		}
		else if (i == 4) { //cube
			puts("Enter dimensions of the cube: ");
			scanf("%f%f%f", &l, &w, &h);
			volume = l * w * h;
			printf("The Volume of the Cube is: %.2f\n\n", volume);
		}
		else if (i == 5) {
			puts("How many feet / inches tall are you (i.e. 5 10) : ");
			scanf("%f%f", &h, &w);
			r = h * 12;
			r = r + w;
			l = r * height;
			printf("Your Height in Centimeters is %.2fcm.", l);
		}
		else if (i == 6) {
			puts("Enter temp in Fahrenheit: ");
			scanf("%f", &w);
			w = w - 32;
			h = w / 1.8;	
			printf("The temperature in Celsius is %.2f degrees\n\n", h);		
		}
		else {
			puts("Cya Later.\n\n");
		}
	}

	return 0;
}
