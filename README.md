# Milestone-4-Application-Release-3
#include<stdio.h>

struct student
{
	union 
	{
		char name[15];
		int roll;
	};
	int mark;
};
int main()
{
	struct student stud;
	char choice;
	printf("\n You can enter your name or roll number ");
	printf("\n Do you want to enter the name (y or n): ");
	scanf_s("%c", &choice);
	if (choice == 'y' || choice == 'Y')
	{
		printf("\n Enter name: ");
		scanf_s("%s", stud.name);
		printf("\n Name:%s", stud.name);
	}
	else
	{
		printf("\n Enter roll number: ");
		scanf_s("%d", &stud.roll);
		printf("\n Roll:%d", stud.roll);
	}
	printf("\n Enter marks: ");
	scanf_s("%d", &stud.mark);
	
	printf("\n Marks:%d", stud.mark);
	return 0;
}
