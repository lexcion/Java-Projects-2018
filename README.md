# potential-octo-waddle
package guessGame;

import java.util.Scanner;


//guess number between 1-100 

public class GGame {
	
	private Scanner scanner;


	public GGame() 
	{
		boolean Playing = true;
		while (Playing == true){
			int guess = 1;
			int guessCount = 0; //keeps track of guesses
			int randomInt = (int)(Math.random()*101); //generate random number 1-100
			System.out.println("Welcome to the guessing game, please guess a number (1-100 integers only please)");
			while (guess != randomInt)
			{
				guessCount += 1;
				
				scanner = new Scanner(System.in);
				String input; 
				input = scanner.nextLine();
				System.out.println("You typed "+ input + ":");
				
				guess = Integer.parseInt(input);
				if (guess < randomInt){
					System.out.println("That is less than what im thinking of");
				}
				else if(guess > randomInt){
					System.out.println("That is higher than what im thinking");
				}
				else {
					System.out.println("That is correct");
				
			}
		}
		System.out.println("It took you " + guessCount + " tries");
		if (guessCount >= 10){
			System.out.println("You can do better than that!");
		}
		else if (guessCount <= 3){
			System.out.println("Wow you are very good at guessing");
		}
		System.out.println("Want to play again? (yes or no)");
		String YorN = scanner.nextLine();
		if (YorN.equals("yes")|| YorN == "y"){
			Playing = true;
		}
		else if(YorN.equals ("no") || YorN == "n"){
			System.out.println("Oh okay");
			}
		else {
			System.out.println("what?");
		}
		}
}


	public static void main(String[] args) {
		new GGame();
	
		
	}

}
