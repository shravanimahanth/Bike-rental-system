#include <stdio.h>
#include <conio.h>
#include <ctype.h>
#include <windows.h>
#include <stdlib.h>
#include <time.h>

void WelcomePage();
void Title();
void Thankyou();
void registerMenu();
void UserMenu();
void login();
void loginForAdmin();
void adminMenu();
void RentBike();
void listOfRentals();
void UserRentedList(char[]);
void edit();
void delete ();
void search();
void UserSearch(char []);
void ViewFares();
void EditFares();
void generateBill(char[],char[], int);
void gotoxy(int,int);

struct CustomerDetails
{
	char bikename[30];
    char username[30];
	char password[30];
	char fullname[30];
	char address[30];
	char phonenumber[15];
	char nationality[15];
	char email[35];
	char license[30];
	int period;
} s, s1;

int main()
{
	system("color 70");
	WelcomePage();
}

void Title()
{
	printf("\n\t\t\t\t\t");
	for (int i = 0; i < 81; i++)
		printf("-");
	printf("\n\t\t\t\t\t   ---------------------->>>>  BIKE RENTAL SYSTEM  <<<<------------------------ ");
	printf("\n\t\t\t\t\t");
	for (int i = 0; i < 81; i++)
		printf("-");
}

void Thankyou()
{
	system("cls");
	printf("\n\n\n");
	Title();
	printf("\n\n\n\n\n\t\t\t\t\t=============================================================================");
	printf("\n\n\t\t\t\t\t\t\t\tTHANKYOU FOR USING OUR SERVICES\n");
	printf("\n\t\t\t\t\t=============================================================================\n\n\n\n\n");
}

void WelcomePage()
{
	time_t t;
	time(&t);
	int i = 0, choice;
	system("cls");
	printf("\n\t\t\t\t\t\t\t%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c",201,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,187);
	printf("\n\t\t\t\t\t\t\t%c                                                %c",186,186);
	printf("\n\t\t\t\t\t\t\t%c     	  _______________________________        %c",186,186);
	printf("\n\t\t\t\t\t\t\t%c                                                %c",186,186);
	printf("\n\t\t\t\t\t\t\t%c          WELCOME TO BIKE RENTAL SYSTEM         %c",186,186);
	printf("\n\t\t\t\t\t\t\t%c         _______________________________        %c",186,186);
	printf("\n\t\t\t\t\t\t\t%c                                                %c",186,186);
	printf("\n\t\t\t\t\t\t\t%c                                                %c",186,186);
	printf("\n\t\t\t\t\t\t\t%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c\n\n",200,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,205,188);
	printf("\n\t\t\t\t\t");
	for (i = 0; i < 80; i++)
		printf(">");
	printf("\n\t\t\t\t\t\t\tCurrent date and time : %s", ctime(&t));
	printf("\t\t\t\t\t");
	for (i = 0; i < 80; i++)
		printf("<");
	printf(" \n\n\n\t\t\t\t\t Press any other key to continue:");
	getch();
	system("cls");
	printf("\n\n\n");
	Title();
	printf("\n\n\n\n\n\t\t\t\t\t\t\t=================================================");
	printf("\n\n\t\t\t\t\t\t\t\t1. REGISTER/ CREATE AN ACCOUNT");
	printf("\n\n\t\t\t\t\t\t\t\t2. LOGIN TO EXISTING ACCOUNT");
	printf("\n\n\t\t\t\t\t\t\t\t3. LOGIN AS ADMIN");
	printf("\n\n\t\t\t\t\t\t\t\t4. EXIT");
	printf("\n\n\t\t\t\t\t\t\t=================================================");
	printf("\n\n\t\t\t\t\t\t\tENTER YOUR CHOICE : ");
	scanf("%d", &choice);
	fflush(stdin);
	switch (choice)
	{
		case 1:
				registerMenu();
				break;
		case 2:
				login();
				break;
		case 3:
				loginForAdmin();
				break;
		case 4:
				Thankyou();
				exit(0);
				break;
		default:
				printf("\nINVALID CHOICE!!!");
				break;
	}
}

void registerMenu()
{
	system("cls");
	char user_name[30], password[20], UName[20], Pass[20];
	int valid=0;
	FILE *usp, *read;
	usp = fopen("Register.txt", "a+");
	read = fopen("Register.txt", "r");
	printf("\n\n\n\t\t\t-------------------------------------------------------  SIGNUP  -------------------------------------------------------\n");
	A:
		printf("\n\t\t\t\t\t\tENTER USERNAME : ");
		gets(user_name);
		while (fscanf(read, "%s %s %s %s %s %s %s %s\n", s.username,s.password,s.fullname,s.address,s.phonenumber,s.nationality,s.email,s.license) != EOF)
		{
			if (strcmp(s.username, user_name) == 0)
			{
				printf("\n\t\t\t\t\t\tUSERNAME ALREADY EXISTS!!");
				goto A;
			}
		}
		fclose(read);

	printf("\n\t\t\t\t\t\tENTER PASSWORD : ");
	gets(s.password);
	B:
		printf("\n\t\t\t\t\t\tENTER FULL NAME : ");
		gets(s.fullname);
		for (int b=0;b<strlen(s.fullname);b++)
		{
			if(isalpha(s.fullname[b]))
			{
				valid=1;
			}
			else
			{
				valid=0;
				break;
			}
		}
		if(!valid)
		{
			printf("\n\t\t\t\t\t\t Full Name contains an Invalid character...Enter again.");
			goto B;
		}
	C:
		printf("\n\t\t\t\t\t\tENTER ADDRESS : ");
		gets(s.address);
		s.address[0]=toupper(s.address[0]);
		if(strlen(s.address)>30||strlen(s.address)<5)
		{
			printf("\n\t\t\t\t\t\tInvalid...The address should be in range of 5 to 30");
			goto C;
		}
	D:
		printf("\n\t\t\t\t\t\tContact no: ");
		gets(s.phonenumber);
		if(strlen(s.phonenumber)>10||strlen(s.phonenumber)!=10)
		{
			printf("\n\t\t\t\t\t\t Invalid...Contact must contain 10 digits.");
			goto D;
		}
	E:
		printf("\n\t\t\t\t\t\tENTER NATIONALITY : ");
		gets(s.nationality);
	F:
		printf("\n\t\t\t\t\t\tENTER EMAIL : ");
		gets(s.email);
	G:
		printf("\n\t\t\t\t\t\tENTER DRIVING LICENSE NUMBER : ");
		gets(s.license);

	fprintf(usp, "%s %s %s %s %s %s %s %s\n", user_name,s.password,s.fullname,s.address,s.phonenumber,s.nationality,s.email,s.license);
	printf("\n\n\n\t\t\t--------------------------------------------  ACCOUNT SUCCESSFULLY CREATED  -------------------------------------------------\n");
	getch();
	fclose(usp);
	WelcomePage();
}

void login()
{
	Title();
	int a = 0, i = 0, counter = 0, flag = 0;
	char ch;
	char un[30],pw[30];
	FILE *fp;
	fp = fopen("Register.txt", "r");
	system("cls");
	printf("\n\n\t\t\t\t\t\t************************  LOGIN FORM  ************************");
	printf("\n\n\n\t\t\t\t\t\t\tENTER USERNAME:- ");
	gets(un);
	printf("\n\n\t\t\t\t\t\t\tENTER PASSWORD:- ");

	while (ch != 13)
	{
		ch = getch();
		if (ch != 13 && ch != 8)
		{
			printf("*");
			pw[i] = ch;
			i++;
		}
		else if (ch == 8)
		{
			if (i > 0)
			{
				i--;
				pw[i] = '\0';
				printf("\b \b");
			}
		}
		if (ch == 13)
		{
			break;
		}
	}
	pw[i] = '\0';

	while (fscanf(fp, "%s %s %s %s %s %s %s %s\n", s.username,s.password,s.fullname,s.address,s.phonenumber,s.nationality,s.email,s.license) != EOF)
	{
		if (strcmp(s.username, un) == 0)
		{
			flag = 1;
			if (strcmp(s.password, pw) == 0)
			{
				printf("\n\n\n\t\t\t\t\t\t\t      ---------- LOGIN SUCCESSFUL ----------");
				getch();
				fclose(fp);
				UserMenu(un);
			}
			else
			{
				counter++;
				printf("\n\n\n\t\t\t\t\t\t\t\t-----WRONG PASSWORD!!!-----");
				printf("\n\n\t\t\t\t\t\t\t\t    ----- TRY AGAIN -----");
				getch();
				fclose(fp);
				login();
			}
		}
	}
	if (flag != 1)
	{
		printf("\n\n\n\t\t\t\t\t\t\t\t\tUSERNAME NOT FOUND!!");
		getch();
		fclose(fp);
		login();
	}
}

void UserMenu(char username[30])
{
	int i = 0;

	time_t t;
	time(&t);
	char customername;
	int choice;
	system("cls");
	while (1)
	{
		system("cls");
		printf("\n\t\t\t\t\t");
		for (i = 0; i < 80; i++)
			printf("-");
		printf("\n\n\t\t\t\t\t   ---------------------->>>>  |MAIN MENU|  <<<<------------------------ \n");
		printf("\n\t\t\t\t\t");
		for (i = 0; i < 80; i++)
			printf("-");
		printf("\n");
		printf("\t\t\t\t\t\t *Select and Enter Your Choice From Menu*:");
		printf("\n\n");
		printf("\n\t\t\t\t\t\t==========================================");
		printf(" \n\t\t\t\t\t\t  Enter 1 ->> Rent a bike");
		printf("\n\t\t\t\t\t\t==========================================");
		printf(" \n\t\t\t\t\t\t  Enter 2 ->> View Vehicle Fares");
		printf("\n\t\t\t\t\t\t==========================================");
		printf(" \n\t\t\t\t\t\t  Enter 3 ->> View Your Rental Record");
		printf("\n\t\t\t\t\t\t==========================================");
		printf(" \n\t\t\t\t\t\t  Enter 4 ->> Search Your Rental Record");
		printf("\n\t\t\t\t\t\t==========================================");
		printf(" \n\t\t\t\t\t\t  Enter 5 ->> Logout");
		printf("\n\t\t\t\t\t\t==========================================");
		printf("\n \n\t\t\t\t\t");
		for (i = 0; i < 80; i++)
			printf(">");
		printf("\n\t\t\t\t\tCurrent date and time : %s", ctime(&t));
		printf("\t\t\t\t\t");
		for (i = 0; i < 80; i++)
			printf("<");
		scanf("%d", &choice);
		fflush(stdin);
		switch (choice)
		{
			case 1:
					RentBike(username);
					break;
			case 2:
					ViewFares();
					break;
			case 3:
					UserRentedList(username);
					break;
			case 4:
					UserSearch(username);
					break;
			case 5:
					system("cls");
					WelcomePage();
					break;
			default:
					system("cls");
					printf("Incorrect Input");
					printf("\n Press any key to continue");
					getch();
					break;
		}
	}
}

void adminMenu()
{
	int choice, i = 0;
	time_t t;
	time(&t);
	system("cls");
	while (1)
	{
		system("cls");
		printf("\n\n\n\t\t\t\t\t\t");
		for (i = 0; i < 80; i++)
			printf("-");
		printf("\n\t\t\t\t\t\t");
		printf("   ---------------------->>>>  |MAIN MENU|  <<<<------------------------ ");
		printf("\n\t\t\t\t\t\t");
		for (i = 0; i < 80; i++)
			printf("-");
		printf("\n");
		printf("\t\t\t\t\t\t\t\t *Select and Enter Your Choice From Menu*:");
		printf("\n\n");
		printf("\n\t\t\t\t\t\t\t========================================");
		printf(" \n\t\t\t\t\t\t\t Enter 1 ->> View Rental Record");
		printf("\n\t\t\t\t\t\t\t========================================");
		printf(" \n\t\t\t\t\t\t\t Enter 2 ->> View Vehicle Fares");
		printf("\n\t\t\t\t\t\t\t========================================");
		printf(" \n\t\t\t\t\t\t\t Enter 3 ->> Edit Fares and stock");
		printf("\n\t\t\t\t\t\t\t========================================");
		printf(" \n\t\t\t\t\t\t\t Enter 4 ->> Remove A User");
		printf("\n\t\t\t\t\t\t\t========================================");
		printf(" \n\t\t\t\t\t\t\t Enter 5 ->> Search a User");
		printf("\n\t\t\t\t\t\t\t========================================");
		printf(" \n\t\t\t\t\t\t\t Enter 6 ->> Edit Record");
		printf("\n\t\t\t\t\t\t\t========================================");
		printf(" \n\t\t\t\t\t\t\t Enter 7 ->> Exit");
		printf("\n\t\t\t\t\t\t\t========================================");
		printf("\n \n\t\t\t\t\t\t");
		for (i = 0; i < 80; i++)
			printf(">");
		printf("\n\n\t\t\t\t\t\t\t\tCurrent date and time : %s", ctime(&t));
		printf("\t\t\t\t\t\t");
		for (i = 0; i < 80; i++)
			printf("<");

		scanf("%d", &choice);
		fflush(stdin);
		switch (choice)
		{
            case 1:
					listOfRentals();
					break;
            case 2:
					ViewFares();
					break;
            case 3:
					EditFares();
					break;
            case 4:
					delete();
					break;
            case 5:
					search();
					break;
            case 6:
					edit();
					break;
            case 7:
					WelcomePage();
					break;
            default:
					system("cls");
					printf("\n\t\t\t\t\t\t\t      Incorrect Input");
					printf("\n\t\t\t\t\t\t\t Press any key to continue");
					getch();
					adminMenu();
		}
	}
}

void RentBike(char username[30])
{
	FILE *f,*fp,*fp1,*fp2;
	time_t t;
	time(&t);
	int i, n, valid = 0, flag = 0;
	char test, bikename[50];
	char vehicle[30], price[7], stock[7],stockLeft1[7],time[50];
	char tempBike[20];
	char tempPrice[5];
	int stockLeft;
	Title();
	f = fopen("Rentals.txt", "a+");
	system("cls");
	printf("\n\t\t\t\t\t\t\t\t--------------------------");
	printf("\n\t\t\t\t\t\t\t\t      ENTER DETAILS");
	printf("\n\t\t\t\t\t\t\t\t--------------------------\n");

bikename:
	printf("\n\t\t\t\t\t===================================================================================");
	printf("\n\t\t\t\t\t\t\t ENTER BIKE NAME\t: ");
	gets(s.bikename);
	/*for (i = 0; s.bikename[i] != '\0'; i++)
	{
		if (s.bikename[i] >= 'a' && s.bikename[i] <= 'z')
		{
			s.bikename[i] = s.bikename[i] - 32;
		}
	}*/
	fp = fopen("viewFares.txt", "r");
	while (fscanf(fp, "%s %s %s\n", tempBike, tempPrice,stock) != EOF)
	{
		if (strcmp(tempBike, s.bikename) == 0)
		{
			flag = 1;
		}
	}
	fclose(fp);
	if (flag != 1)
	{
		printf("\n\t\t\t\t\t\t\t  PLEASE ENTER A VALID BIKE NAME!");
		goto bikename;
	}
	fp = fopen("viewFares.txt","r");
	fp2 = fopen("newFares.txt","w+");
	flag = 0;
	while (fscanf(fp, "%s %s %s\n", vehicle, price, stock) != EOF)
	{
		if (strcmp(vehicle, s.bikename) == 0)
		{
			stockLeft = atoi(stock);
			if(stockLeft>0)
			{
				flag = 1;
				stockLeft--;
				itoa(stockLeft,stockLeft1,10);
				fprintf(fp2, "%s %s %s\n", vehicle, price,stockLeft1);
			}
			else
			{
				itoa(stockLeft,stockLeft1,10);
				printf("\n\t\t\t\t\t\t\t\tNO STOCK OF THIS VEHICLE !\n");
				fprintf(fp2,"%s %s %s\n", vehicle, price,stockLeft1);
			}
		}
		else
		{
			fprintf(fp2,"%s %s %s\n", vehicle, price,stock);
		}
	}
	fclose(fp);
	fclose(fp2);
	remove("viewFares.txt");
	rename("newFares.txt","viewFares.txt");
	if(flag != 1)
	{
		goto bikename;
	}
	do
	{
		printf("\n\t\t\t\t\t===================================================================================");
		printf("\n\t\t\t\t\t\t\t ENTER TIME PERIOD('x'days)\t: ");
		scanf("%i", &s.period);
		if (s.period > 10 || s.period <= 0)
		{
			printf("\n\t\t\t\t\t\t\t\t\tINVALID!!\n\t\t\t\t\t\t\tTHE MAXIMUM PERIOD TO RENT IS 10 DAYS.\n\n");
		}
	} while (s.period > 10 || s.period <= 0);

	for(int i = 0;i<strlen(ctime(&t))-1;i++)
    {
		if(ctime(&t)[i] == ' ')
		{
			time[i] = '-';
		}
		else
		{
			time[i] = ctime(&t)[i];
		}
    }

	fprintf(f,"%s %s %i %s\n", s.bikename, username, s.period,time);
	printf("\n\n\t\t\t\t\t===================================================================================");
	printf("\n\n\t\t\t\t\t\t\t---- YOUR DESIRED BIKE IS RENTED SUCCESSFULLY! ----");
	fclose(f);
	printf("\n\n\n\t\t\t\t\t\t\tPRESS ANY KEY TO GO TO BILLING : ");
	getch();
	generateBill(username, s.bikename, s.period);
}

void listOfRentals()
{
	FILE *f,*fp;
	int i, q = 9;
	char user_name[30],time[50];
	if ((fp = fopen("Rentals.txt", "r")) == NULL)
		exit(0);
	system("cls");
		Title();
	gotoxy(0,5);
	for (i = 0; i < 155; i++)
	{
		printf("-");
	}
	gotoxy(1, 6);
	printf("BIKENAME ");
	gotoxy(15, 6);
	printf("NAME ");
	gotoxy(30, 6);
	printf("ADDRESS ");
	gotoxy(45, 6);
	printf("PHONENUMBER ");
	gotoxy(63, 6);
	printf("NATIONALITY ");
	gotoxy(83, 6);
	printf("EMAIL ");
	gotoxy(105, 6);
	printf("PERIOD \n");
	gotoxy(130, 6);
	printf("RENTED TIME \n");

	for (i = 0; i < 155; i++)
	{
		printf("-");
	}
	printf("\n");
	while(fscanf(fp,"%s %s %i %s\n", s.bikename, user_name, &s.period,time) != EOF)
	{
		f = fopen("Register.txt","r");
		while (fscanf(f, "%s %s %s %s %s %s %s %s\n", s.username,s.password,s.fullname,s.address,s.phonenumber,s.nationality,s.email,s.license) != EOF)
		{
			if(strcmp(user_name,s.username) == 0)
			{
				gotoxy(1, q);
				printf("%s", s.bikename);

				gotoxy(15, q);
				printf("%s", s.fullname);

				gotoxy(30, q);
				printf("%s", s.address);

				gotoxy(45, q);
				printf("%s", s.phonenumber);

				gotoxy(66, q);
				printf("%s", s.nationality);

				gotoxy(82, q);
				printf("%s", s.email);

				gotoxy(107, q);
				printf("%i", s.period);

				gotoxy(122, q);
				printf("%s",time);
				q++;
			}
		}
		fclose(f);
	}
	printf("\n\n");
	for (i = 0; i < 155; i++)
		printf("-");
	fclose(fp);
	getch();
}

void UserRentedList(char username[30])
{
	char user_name[50],time[50];
    FILE *f,*fp;
	int i, q = 9;
	fp = fopen("Rentals.txt","r");
	Title();
	system("cls");
	gotoxy(1, 6);
	printf("BIKENAME ");
	gotoxy(15, 6);
	printf("NAME ");
	gotoxy(30, 6);
	printf("ADDRESS ");
	gotoxy(45, 6);
	printf("PHONENUMBER ");
	gotoxy(63, 6);
	printf("NATIONALITY ");
	gotoxy(83, 6);
	printf("EMAIL ");
	gotoxy(105, 6);
	printf("PERIOD \n");
	gotoxy(130, 6);
	printf("RENTED TIME \n");
	printf("\n");
	for (i = 0; i < 155; i++)
	{
		printf("-");
	}
	while(fscanf(fp,"%s %s %i %s\n", s.bikename, user_name, &s.period,time) != EOF)
	{
		if(strcmp(user_name,username) == 0)
		{
			f = fopen("Register.txt", "r");
			while (fscanf(f, "%s %s %s %s %s %s %s %s\n", s.username,s.password,s.fullname,s.address,s.phonenumber,s.nationality,s.email,s.license) != EOF)
			{
				if(strcmp(user_name,s.username) == 0)
				{
					gotoxy(1, q);
					printf("%s", s.bikename);

					gotoxy(15, q);
					printf("%s", s.fullname);

					gotoxy(30, q);
					printf("%s", s.address);

					gotoxy(45, q);
					printf("%s", s.phonenumber);

					gotoxy(66, q);
					printf("%s", s.nationality);

					gotoxy(82, q);
					printf("%s", s.email);

					gotoxy(107, q);
					printf("%i", s.period);

					gotoxy(122, q);
					printf("%s",time);
					q++;
				}
			}
			fclose(f);
		}
	}
	gotoxy(0,q);
	for (i = 0; i < 155; i++)
		printf("-");
	fclose(fp);
	getch();
	UserMenu(username);
}

void delete()
{
	FILE *f, *t;
	int flag = 0;
	char custUserName[50], custName[50];
	if ((f = fopen("Register.txt", "r")) == NULL)
	{
		Title();
		printf("\n\n\n\t\t\t\t\t\t\tNO RECORD ADDED.");
		getch();
	}
	else
	{
		system("cls");
		Title();
		t = fopen("temp.txt", "w+");
		printf("\n\n\n\n\t\t\t\t\t\t\tENTER USERNAME OF COSTUMER TO DELETE : ");
		gets(custUserName);
		while (fscanf(f, "%s %s %s %s %s %s %s %s\n", s.username,s.password,s.fullname,s.address,s.phonenumber,s.nationality,s.email,s.license) != EOF)
		{
			if (strcmp(custUserName, s.username) == 0)
			{
                flag = 1;
			}
			else
			{
                fprintf(t, "%s %s %s %s %s %s %s %s\n", s.username,s.password,s.fullname,s.address,s.phonenumber,s.nationality,s.email,s.license);
			}
		}
		fclose(f);
		fclose(t);
		if (flag != 1)
		{
			printf("\n\n\n\t\t\t\t\t\t\t RECORDS OF THIS COSTUMER ARE NOT FOUND !");
			getch();
		}
		else
		{
			printf("\n\n\n\n\t\t\t\t\t\t\t---------- SUCCESSFULLY DELETED ----------\n");
		}

		remove("Register.txt");
		rename("temp.txt", "Register.txt");
		getch();
	}
	adminMenu();
}

void ViewFares()
{
	system("cls");
	FILE *fp;
	char vehicle[20];
	char price[7];
	char stock[7];
	int y=12;
	Title();
	fp = fopen("viewFares.txt", "r");
	printf("\n\n\n\t\t\t\t\t   ------------------ FARES OF VEHICLES PER DAY AND STOCK ------------------");
	gotoxy(55,10);		printf("VEHICLE");
	gotoxy(75,10);		printf("FARE");
	gotoxy(90,10);		printf("STOCK LEFT");
	printf("\n\t\t\t\t\t\t---------------------------------------------------------");
	while (fscanf(fp,"%s %s %s\n", vehicle,price,stock) != EOF)
	{
		gotoxy(55,y);	printf("%s",vehicle);
		gotoxy(75,y);	printf("%s",price);
		gotoxy(95,y);	printf("%s",stock);
		y++;
	}
	fclose(fp);
	printf("\n\n\n\n\t\t\t\t\t\tENTER ANY KEY TO CONTINUE");
	getch();
}

void EditFares()
{
	system("cls");
	Title();
	FILE *fp, *r;
	int flag = 0;
	char vehicle[20], price[7], editVehicle[20], editPrice[7],stock[7],editStock[7];
	fp = fopen("viewFares.txt", "r");
	r = fopen("temp.txt", "w+");
	printf("\n");
	while (fscanf(fp, "%s %s %s\n", vehicle, price,stock) != EOF)
	{
		printf("\n\t\t\t\t\t\t\t\t%s\t: %s\n", vehicle, price);
	}
	fclose(fp);
	printf("\n\t\t\t\t\t");
	for (int i = 0; i < 80; i++)
		printf("-");
	fp = fopen("viewFares.txt", "r");
	printf("\n\n\t\t\t\t\t\tENTER VEHICLE TO EDIT : ");
	gets(editVehicle);
	printf("\n\t\t\t\t\t\tENTER UPDATED PRICE : ");
	gets(editPrice);
	printf("\n\t\t\t\t\t\tENTER UPDATED STOCK : ");
	gets(editStock);

	while (fscanf(fp, "%s %s %s\n", vehicle, price,stock) != EOF)
	{
		if (strcmp(vehicle, editVehicle) == 0)
		{
			flag = 1;
			fprintf(r, "%s %s %s\n", editVehicle, editPrice,editStock);
		}
		else
		{
			fprintf(r, "%s %s %s\n", vehicle, price,stock);
		}
	}
	if (flag != 1)
	{
		printf("\n\n\t\t\t\t\t\t\t\t\tTHE VEHICLE DOESN'T EXIST!!!");
	}
	fclose(fp);
	fclose(r);
	remove("viewFares.txt");
	rename("temp.txt", "viewFares.txt");
	getch();
}

void search()
{
	system("cls");
	FILE *f,*fp;
	char username[50],name[50];
	char user_name[30],time[50];
	int flag = 1;
	fp = fopen("Rentals.txt","r");
	Title();
	if (f == NULL)
	{
		printf("\n\n\t\t\t\t\t\t\tNO RECORD ADDED.");
		getch();
	}
	else
	{
		printf("\n\n\t\t\t\t\t\t\tENTER USERNAME OF COSTUMER TO SEARCH : ");
		gets(username);
        printf("\n\t\t\t\t\t\t\tENTER FULLNAME OF COSTUMER : ");
        gets(name);
		while(fscanf(fp,"%s %s %i %s\n",s.bikename,user_name,&s.period,time) != EOF)
		{
			f = fopen("Register.txt", "r");
			while (fscanf(f, "%s %s %s %s %s %s %s %s\n", s.username,s.password,s.fullname,s.address,s.phonenumber,s.nationality,s.email,s.license) != EOF)
			{
				if(strcmp(username,s.username) == 0 &&strcmp(user_name,username) == 0)
				{
					flag = 2;
					if(strcmp(name, s.fullname) == 0)
					{
						flag = 0;
						printf("\n\n\t\t\t\t\t\t\t=======================================================");
						printf("\n\n\t\t\t\t\t\t\t\t\tRECORD FOUND\n");
						printf("\n\t\t\t\t\t\t\t\tBIKE NAME\t: %s", s.bikename);
						printf("\n\t\t\t\t\t\t\t\tNAME\t\t: %s", s.fullname);
						printf("\n\t\t\t\t\t\t\t\tADDRESS\t\t: %s", s.address);
						printf("\n\t\t\t\t\t\t\t\tPHONE NUMBER\t: %s", s.phonenumber);
						printf("\n\t\t\t\t\t\t\t\tNATIONALITY\t: %s", s.nationality);
						printf("\n\t\t\t\t\t\t\t\tEMAIL\t\t: %s", s.email);
						printf("\n\t\t\t\t\t\t\t\tLICENSE NO\t: %s", s.license);
						printf("\n\t\t\t\t\t\t\t\tPERIOD\t\t: %i",s.period);
						printf("\n\t\t\t\t\t\t\t\tRENTED TIME     : %s",time);
					}
				}
			}
			fclose(f);
		}
		if (flag == 1)
		{
			printf("\n\t\t\t\t\t\t\tREQUESTED USERNAME COULD NOT BE FOUND !");
		}
        else if(flag == 2)
        {
            printf("\n\t\t\t\t\t\t\t THIS PERSON DID NOT RENT ANY BIKE WITH THE USERNAME YOU ENTERED !");
        }
		getch();
	}
	fclose(fp);
	fclose(f);
	adminMenu();
}

void UserSearch(char username[20])
{
    system("cls");
	FILE *f,*fp;
	char bikename[50],user_name[30],time[50];
	int flag = 1;
	fp = fopen("Rentals.txt","r");
	Title();
	if (fp == NULL)
	{
		printf("\n\n\t\t\t\t\t\t\tNO RECORD ADDED.");
		getch();
	}
	else
	{
		printf("\n\n\t\t\t\t\t\t\tENTER BIKENAME YOU WANT TO SEARCH : ");
		gets(bikename);
		while(fscanf(fp,"%s %s %i %s\n",s.bikename,user_name,&s.period,time) != EOF)
		{
			if (strcmp(bikename, s.bikename) == 0)
			{
				f = fopen("Register.txt", "r");
				while (fscanf(f, "%s %s %s %s %s %s %s %s\n", s.username,s.password,s.fullname,s.address,s.phonenumber,s.nationality,s.email,s.license) != EOF)
				{
					if(strcmp(username,s.username)==0 && strcmp(s.username,user_name)==0)
					{
						flag = 0;
						printf("\n\n\t\t\t\t\t\t\t=======================================================");
						printf("\n\n\t\t\t\t\t\t\t\t\tRECORD FOUND\n");
						printf("\n\t\t\t\t\t\t\t\tBIKE NAME\t: %s", s.bikename);
						printf("\n\t\t\t\t\t\t\t\tNAME\t\t: %s", s.fullname);
						printf("\n\t\t\t\t\t\t\t\tADDRESS\t\t: %s", s.address);
						printf("\n\t\t\t\t\t\t\t\tPHONE NUMBER\t: %s", s.phonenumber);
						printf("\n\t\t\t\t\t\t\t\tNATIONALITY\t: %s", s.nationality);
						printf("\n\t\t\t\t\t\t\t\tEMAIL\t\t: %s", s.email);
						printf("\n\t\t\t\t\t\t\t\tLICENSE NO\t: %s", s.license);
						printf("\n\t\t\t\t\t\t\t\tPERIOD\t\t: %i",s.period);
						printf("\n\t\t\t\t\t\t\t\tRENTED TIME     : %s",time);
					}
				}
				fclose(f);
			}
		}
		if (flag == 1)
		{
			printf("\n\t\t\t\t\t\t\t\tTHIS BIKE IS NOT RENTED BY YOU !");
		}
		getch();
    }
	fclose(fp);
	UserMenu(username);
}

void edit()
{
	FILE *f, *r;
	int k = 0,t = 0;
	char ed;
	char username[50],name[50], upName[30], upAddress[30], upPhno[15], upNat[15], UpEm[35],upLicNo[30];
	long int size = sizeof(s);
	r = fopen("temp.txt", "w+");
	if ((f = fopen("Register.txt", "r")) == NULL)
	{
		Title();
		printf("\n\n\n\t\t\t\t\t\t\tNO RECORD ADDED.");
		fclose(f);
		fclose(r);
		getch();
	}
	else
	{
		system("cls");
		Title();
		printf("\n\n\n\t\t\t\t\t\t\tENTER USERNAME OF COSTUMER TO SEARCH : ");
		gets(username);
        printf("\n\n\t\t\t\t\t\t\tENTER FULLNAME OF COSTUMER : ");
        gets(name);
		while (fscanf(f, "%s %s %s %s %s %s %s %s\n", s.username,s.password,s.fullname,s.address,s.phonenumber,s.nationality,s.email,s.license) != EOF)
		{
            if(strcmp(username,s.username) == 0)
            {
                k = 2;
                if (strcmp(name, s.fullname) == 0)
                {
                    t = 1;
                    printf("\n\t\t\t\t\t\t\t\t\t*** Existing Record ***");
                    printf("\n\t\t\t\t\t\t\t\tName\t\t: %s", s.fullname);
                    printf("\n\t\t\t\t\t\t\t\tAddress\t\t: %s", s.address);
                    printf("\n\t\t\t\t\t\t\t\tPhone number\t: %s", s.phonenumber);
                    printf("\n\t\t\t\t\t\t\t\tNationality\t: %s", s.nationality);
                    printf("\n\t\t\t\t\t\t\t\tEmail\t\t: %s", s.email);
					printf("\n\t\t\t\t\t\t\t\tLicense No\t:%s",s.license);

                    printf("\n\n\t\t\t\t\t\t\t\t\t*** New Record ***");
                    printf("\n\t\t\t\t\t\t\t\tEnter New Name           : ");
                    gets(upName);
                    printf("\n\t\t\t\t\t\t\t\tEnter New Address        : ");
                    gets(upAddress);
                    printf("\n\t\t\t\t\t\t\t\tEnter New Phone number   : ");
                    gets(upPhno);
                    printf("\n\t\t\t\t\t\t\t\tEnter New Nationality    : ");
                    gets(upNat);
                    printf("\n\t\t\t\t\t\t\t\tEnter New Email          : ");
                    gets(UpEm);
                    printf("\n\t\t\t\t\t\t\t\tEnter updated license no :");
					gets(upLicNo);
                    fprintf(r, "%s %s %s %s %s %s %s %s\n", s.username,s.password,upName,upAddress,upPhno,upNat,UpEm,upLicNo);
                }
                else
                {
                    fprintf(r, "%s %s %s %s %s %s %s %s\n", s.username,s.password,s.fullname,s.address,s.phonenumber,s.nationality,s.email,s.license);
                }
            }
            else
            {
                fprintf(r, "%s %s %s %s %s %s %s %s\n", s.username,s.password,s.fullname,s.address,s.phonenumber,s.nationality,s.email,s.license);
            }
		}
		if (k == 0)
		{
			printf("\n\nNO RECORD WITH THIS USERNAME !");
		}
        else if((k == 2) && (t != 1))
        {
            printf("\n\nNO BIKES RENTED IN THIS ACCOUNT BY THE NAME YOU ENTERED !");
        }
		fclose(r);
		fclose(f);
		remove("Register.txt");
		rename("temp.txt", "Register.txt");
		getch();
	}
	adminMenu();
}

void generateBill(char username[20], char bikename[20], int period)
{
	time_t t;
	FILE *fp = fopen("viewFares.txt", "r");
	time(&t);
	char tempBike[20];
	char tempPrice[5],stock[7];
	float bill = 0;
	while (fscanf(fp, "%s %s %s\n", tempBike, tempPrice,stock) != EOF)
	{
		if (strcmp(tempBike, bikename) == 0)
		{
			bill = atoi(tempPrice) * period;
		}
	}
    system("cls");
    printf("\n\t\t\t\t\t|================================================================================|");
	printf("\n\t\t\t\t\t|                          Bike Rental - Customer Invoice                        |");
	printf("\n\t\t\t\t\t|================================================================================|");
    printf("\n\t\t\t\t\t\t	> USER NAME               :          %s\n", username);
	printf("\n\t\t\t\t\t\t	> CUSTOMER NAME           :          %s\n", s.fullname);
	printf("\n\t\t\t\t\t\t	> BIKE MODEL              :          %s\n", s.bikename);
	printf("\n\t\t\t\t\t\t	> ADDRESS                 :          %s\n", s.address);
	printf("\n\t\t\t\t\t\t	> PHONENUMBER             :          %s\n", s.phonenumber);
	printf("\n\t\t\t\t\t\t	> NATIONALITY             :          %s\n", s.nationality);
	printf("\n\t\t\t\t\t\t	> EMAIL                   :          %s\n", s.email);
	printf("\n\t\t\t\t\t\t	> NUMBER OF DAYS          :          %i\n", s.period);
	printf("\n\t\t\t\t\t\t	> RENTED DATE & TIME      :          %s\n", ctime(&t));
	printf("\n\t\t\t\t\t__________________________________________________________________________________\n");
	printf("\n\t\t\t\t\t\t	> TOTAL RENTAL AMOUNT     :            Rs. %f", bill);
	printf("\n\t\t\t\t\t__________________________________________________________________________________");
	printf("\n\n\t\t\t\t\t\tENTER ANY KEY TO PROCEED : ");
	getch();
	fclose(fp);
	UserMenu(username);
}

void loginForAdmin()
{
	system("cls");
	char username[] = "bikerentalsystem";
	char pw[] = "miniproject";
	char UName[20], password[20], ch;
	int i, flag = 0, counter = 0;
	printf("\n\n\n");
	Title();
	printf("\n\n\n\n\n\t\t\t\t\t\t************************  LOGIN FOR ADMIN  ************************");
	printf("\n\n\n\t\t\t\t\t\t\tENTER USERNAME:- ");
	gets(UName);
	printf("\n\n\t\t\t\t\t\t\tENTER PASSWORD:- ");
	gets(password);

	if (strcmp(username, UName) == 0)
	{
		flag = 1;
		if (strcmp(password, pw) == 0)
		{
			printf("\n\n\n\t\t\t\t\t\t\t      ---------- LOGIN SUCCESSFUL ----------");
			getch();
			adminMenu();
		}
		else
		{
			counter++;
			printf("\n\n\n\t\t\t\t\t\t\t\t-----WRONG PASSWORD!!!-----");
			printf("\n\n\t\t\t\t\t\t\t\t    ----- TRY AGAIN -----");
			getch();
			loginForAdmin();
		}
	}
	if (flag != 1)
	{
		printf("\n\n\n\t\t\t\t\t\t\t\t\tUSERNAME NOT FOUND!!");
		getch();
		WelcomePage();
	}
}

void gotoxy(int x, int y)
{
	COORD CR;
	CR.X = x;
	CR.Y = y;
	SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), CR);
}
