#include<stdio.h>
#include<stdlib.h>
//strutures
struct User{
        int accountNumber;
        char name[50];
        char accounttype[20];
        float balance;
        int adharno;
    };
#define MAX_USERS 100
struct User users[MAX_USERS];
int usercount = 0;
//Functions declaration
void displaymenu();
void checkbalance();
void openbankaccount();
void withdrawmoney();
void depositmoney();
void applyforaloaan();
void viewbankstatement();
int main()
{ 
    int choice;
    int accnumber;
    printf("\n!!! Welcome to our BANK MANAGEMENT SYSTEM !!!\n");
   do{
    displaymenu();
    printf("\nEnter your choice:");
    scanf("%d",&choice);

    switch (choice) {
        case 1:
              printf("Enter account number:");
              scanf("%d",&accnumber);
              checkbalance(accnumber);
              break;
        case 2:
              printf("Enter account number:");
              scanf("%d",&accnumber);
              withdrawmoney();
              break;
        case 3:
              printf("Enter account number:");
              scanf("%d",&accnumber);
              depositmoney();
              break;
        case 4:
              openbankaccount();
              break;
        case 5:
              printf("Enter account number:");
              scanf("%d",&accnumber);
              viewbankstatement();
              break;
        case 6:
              applyforaloaan();
              break;
        case 7:
              printf("Have a Goodday,Thank You!!!!");
              exit(0);
        default:
               printf("Invalid Choice!!!! Please try again!!!!\n");
    }
    }while(choice!=7);
    return 0;
}
void displaymenu(){
    printf("1.Check Bank Balance.\n");
    printf("2.Withdraw money.\n");
    printf("3.Deposit money.\n");
    printf("4.Open a Saving account.\n");
    printf("5.View Bank Statement.\n");
    printf("6.Apply for a Loan.\n");
    printf("7.Exit.\n");

}
void checkbalance(int accountNumber){
    for (int i=0; i < usercount; i++){
        if(users[i].accountNumber == accountNumber) {
        printf("<<<<< Account Exhits >>>>>");
        printf("\nACcount holder's name:%d.\n",users[i].name);
        printf("\nAccount type:%s.\n",users[i].accounttype);
        printf("\nYour Bank Balance is:%f.\n",users[i].balance);

        }
        
    }
    
    }
  
void withdrawmoney(){
    int arr[11],n;
    int m=7277;
    printf("Enter your account number:");
    for (int i = 0; i<11; i++){
        scanf("%d",&arr[i]);
    printf("Welcome Pranav Gawande\n");
    printf("Enter amount to be withdrawn:");
    scanf("%d",&n);
    printf("Take cash from Cash Counter.\n");
    printf("Current Balance is:%d.\n",m-n);
}
}
void depositmoney(){
    int arr[11],n;
    int m=7277;
    printf("Enter your account number:");
    for (int i = 0; i<11; i++){
    scanf("%d",&arr[i]);
    printf("Welcome Pranav Gawande\n");
    printf("Enter Amount to be Depositted:");
    scanf("%d",&n);
    printf("Your money deposited successfully.\n");
    printf("Current Balance is:%d.",m+n);
}
}
void applyforaloaan(){
    char a[10],c[10],d[10],e[10];
    int b;
    printf("PERSONAL INFORMATION\n");
    printf("1.Full Name (as per ID proof):\n");
    scanf("%s",a);
    printf("2.Date of Birth:\n");
    scanf("%d",&b);
    printf("3.Gender:\n");
    scanf("%s",c);
    printf("4.Contact Number (Mobile/Landline):\n");
    scanf("%s",d);
    printf("5.Email Address:\n");
    scanf("%s",e);
    printf("IDENTITY VERIFICATION");

}
void viewbankstatement()
{
    int arr[11],n;
    int m=7277;
    printf("Enter your account number:");
    for (int i = 0; i<11; i++){
    scanf("%d",&arr[i]);
    printf("Welcome Pranav Gawande\n");
    printf("dt.12/11/2024 \t\tRs.2000 to Bhavik Dumore.\n");
    printf("dt.11/11/2024 \t\tRs.2000 to Bhushan Kakde.");
}
}
void openbankaccount()
{
    if (usercount >= MAX_USERS){
        printf("Maximum user limit reached.\n");
    }
    struct User newUser;
    printf("\nEnter Name: ");
    scanf(" %[^\n]s", newUser.name); // To read strings with spaces.
    printf("\nEnter Account Type: ");
    scanf(" %[^\n]s", newUser.accounttype);
    printf("\nEnter your adhar no:");
    scanf("%d",&newUser.adharno);
    printf("\nEnter account no as your wish:");
    scanf("%d", &newUser.accountNumber);
    users[usercount++] = newUser;
    printf("\nAccount Created successfully!\n");
    printf("\nWelcome to our Bank!!!!");
}
