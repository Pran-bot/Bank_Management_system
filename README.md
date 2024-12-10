# Bank_Management_system
First C project
#include<stdio.h>
#include<stdlib.h>
//Functions declaration
void displaymenu();
void checkbalance();
void openbankaccount();
void withdrawmoney();
void depositmoney();
void applyforaloaan();
void bankstatement();
int main()
{ 
    int choice;
    printf("\n!!! Welcome to our BANK MANAGEMENT SYSTEM !!!\n");
   do{
    displaymenu();
    printf("\nEnter your choice:");
    scanf("%d",&choice);

    switch (choice) {
        case 1:
              checkbalance();
              break;
        case 2:
              withdrawmoney();
              break;
        case 3:
              depositmoney();
              break;
        // case 4:
        //       applyforaloaan();
        //       break;
        case 4:
              printf("Have a Goodday,Thank You!!!!");
              exit(0);
        default:
               printf("Invalid Choice!!!! Please try again!!!!\n");
    }
    }while(choice<=3);
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
void checkbalance(){
    int arr[11];
    printf("Enter your account number:");
    for (int i = 0; i<11; i++){
        scanf("%d",&arr[i]);
    printf("Welcome Pranav Gawande\n");
    printf("\nYour Bank Balance is:");
    printf("\n7,277.20");
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
// void applyforaloaan(){
//     char a[10],c[10],d[10],e[10];
//     int b;
//     printf("PERSONAL INFORMATION\n");
//     printf("1.Full Name (as per ID proof):\n");
//     scanf("%s",a);
//     printf("2.Date of Birth:\n");
//     scanf("%d",&b);
//     printf("3.Gender:\n");
//     scanf("%s",c);
//     printf("4.Contact Number (Mobile/Landline):\n");
//     scanf("%s",d);
//     printf("5.Email Address:\n");
//     scanf("%s",e);
//     printf("IDENTITY VERIFICATION");

// }