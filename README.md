# TheJavaGuesser
import java.util.*;

public class Guesser {
	public static void main(String[] args){
		int guess;
		int correct;
		int turns = 0;
		boolean keepGoing = true;

		Scanner sc = new Scanner(System.in);
		System.out.println("1.) Exit");
		System.out.println("2.) Human Guesser");
		System.out.println("3.) Computer Guesser");
		System.out.println();
		System.out.println("Please enter 1-3: ");
		String choice = sc.nextLine();

		if (choice.equals("2")){
			System.out.println("Human Guesser");
			correct = (int)(Math.random() * 100) + 1;
			System.out.println(correct);
			
			while (keepGoing){
				System.out.print((turns++) + ") Please enter a number: ");
				guess = sc.nextInt();

				if (guess == correct){
					System.out.println("Correct!");
					keepGoing = false;
				}
				else if (guess < correct){
					System.out.println("Too low. Try again.");
				}
				else{
					System.out.println("Too high. Try again.");
				}
			}

		}
		else if(choice.equals("3")){
			System.out.println("Computer Guesser");
		}
		else{
			System.out.println(":(");
		}

	}
}