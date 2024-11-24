# Interest-Rate-Calculator
Class Assignment 

// Week 8 Lab - Interest Rate Calculator Part 1
// Programmed by: Cortez Beaver, Student
// November 24, 2024

package interestRateCalculatorPart1;

import java.util.Scanner;
import java.util.Locale;
import java.text.NumberFormat;

public class InterestRateCalculatorPart1
{
	public static void main(String[] args)
	{
		System.out.println("Welcome to the Interest Calculator");
		
		//  Assume the user has more inputs
		  char keepGoing = 'y';
		
		// Get a Scanner object for user inputs
		Scanner input = new Scanner(System.in);
		  
		// Keep getting new inputs until the user says no more 
	      while ( keepGoing != 'n' && keepGoing != 'N')
	      {
	    	  
	    	  System.out.print("\nEnter loan amount: ");
	    	  int loanAmount = input.nextInt();
	    	  System.out.print("Enter interest rate: ");
	    	  double interestRate = input.nextDouble();
	    	  
	    	 // Calculate interest amount
	    	 Locale usa = new Locale("en", "US");
	    	 double interestAmount = interestRate/100.0 * loanAmount;
	    	 NumberFormat dollarFormat = NumberFormat.getCurrencyInstance(usa);
	    	      	  
	    	  // Output results
	    	  System.out.println("\nLoan amount:\t\t" + dollarFormat.format(loanAmount));
	    	  if ((double)((int) interestRate) == interestRate)
	    	  {
	    		  System.out.println("Interest rate:\t\t" + (int) interestRate + "%");
	    	  }
	    	  else
	    	  {
	    		  System.out.println("Interest rate:\t\t" + interestRate + "%");
	    	  }
	    	  System.out.println("Interest:\t\t" + dollarFormat.format(interestAmount));
	    	  
	    	  // See if user has more inputs
	    	  System.out.print("\nContinue? (y/n): ");
	    	  keepGoing =input.next().charAt(0);
	      }
  	      // All done
	      input.close(); // Note inputs
	      System.out.println("\nBye!!");
	}
}


