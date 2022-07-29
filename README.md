# Simple-ATM-Machine
This is my first learning with Github

import java.util.*;
class ATM   
{
    public static void  main()
    {
    Scanner cin=new Scanner(System.in);
    
    int a=0,b=0,c=0,i,j,n1=0,n2=0,count=0;
    int blnc=5000,depo=0,wtdw=0;
    
    /////////////////////////////////////////////////////////////////////////////Database
    
    int ac_no[]=new int[]{12,21,98,56,78,98,45,67,66,90};
    int pin_no[]=new int[]{123,213,983,563,783,983,453,673,663,903};
    
    //User Atm input
    
    System.out.println("Enter the Account Number");
    a=cin.nextInt();
    System.out.println("Enter the Pin");
    b=cin.nextInt();
    
    ///////////////////////////////////////////////////////////////////////// //position matching
    
    for(j=0;j<10;j++)
    {
        if(ac_no[j]==a)        
        n1=j;
        if(pin_no[j]==b)
        n2=j;
    }
    
    if(n1==n2) // operation 1
        {
            System.out.println("Press 1 For -> Check Account Balance");
            System.out.println("Press 2 For -> Deposit");
            System.out.println("Press 3 For -> Withdraw");
            System.out.println("Press 4 For -> Exit");
            c=cin.nextInt();
        }
    else
        System.out.println("Wrong Credential Please Check Again !");
        
        
    ////////////////////////////////////////////////////////////////////////////////operation 2  
    
    switch(c)
    {
        case 1:
            System.out.println("Your Account Balance -> "+blnc);
            break;
        case 2:
            System.out.println("Deposit Your Money");
            depo=cin.nextInt();
            blnc=blnc+depo;
            System.out.println("Now Your Balance -> "+blnc);
            break;
        case 3:
            System.out.println("Enter Your Withdraw Money");
            wtdw=cin.nextInt();
            blnc=blnc-wtdw;
            System.out.println("Processing...");
            System.out.println("Now Your Balance -> "+blnc);
            break;
           
        case 4:
        
            System.out.print("Please take Your card  [|||||] ");
            count++;
            break;
        
    }
    
    if(count>0)
     System.out.print("");   
    else
     System.out.print(" Please Take Your Card [|||||] ");
    }
    }        



        
