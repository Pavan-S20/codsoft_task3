# codsoft_task3
// ATM Interface

import java.util.*;


public class atmMachine 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int balance = 10000, deposit, withdraw;
        
        while (true) 
        {
            System.out.println("Choose 1 for deposite: ");
            System.out.println("Choose 2 for withdraw: ");
            System.out.println("Choose 3 for check balance : ");
            System.out.println("Choose 4 for exit: ");
            System.out.println("Choose the operation you want to perform: ");
            
            int choice = sc.nextInt();

        switch (choice) {
            case 1:
                System.out.println("Enter amount you want to deposit: ");
                deposit = sc.nextInt();

            balance = balance + deposit;
                System.out.println("your updated balance is:" + balance);
                System.out.println();    
                break;

            case 2:
                System.out.println("Enter amount to withdraw: ");
                withdraw = sc.nextInt();
                
                if(balance >= withdraw)
                {
                    balance = balance - withdraw;
                    System.out.println("your updated balance is: " + balance);
                }
                else
                {
                    System.out.println("insufficient funds...! ");
                }
                break;

            case 3:
                System.out.println("your account balance is: " + balance);
                System.out.println();
                break;

            case 4:
                System.out.println("EXIT! ");
                break;
                
        }    
        }
    }    
}
