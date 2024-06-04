import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        System.out.println("Welcome to the math quiz!");
        System.out.println("Enter the name and get ready to answer the following 5 questions: ");
        String fileName;
        fileName = scan.nextLine() + "-answers.txt";

        String pr1 = "13+25 = ";
        System.out.println(pr1);
        int answ1 = 13 + 25;
        int message = scan.nextInt();
        boolean score1 = (message == answ1);
        fileMaker(fileName, pr1 + message + " " + score1);

        String pr2 = "3*14 = ";
        System.out.println(pr2);
        int answ2 = 3*14;
        message = scan.nextInt();
        boolean score2 = (message == answ2);
        fileMaker(fileName, pr2 + message + " " + score2);

        String pr3 = "6 / 3 = ";
        System.out.println(pr3);
        int answ3 = 6 / 3;
        message = scan.nextInt();
        boolean score3 = (message == answ3);
        fileMaker(fileName, pr3 + message + " " + score3);

        String pr4 = "55 - 25 = ";
        System.out.println(pr4);
        int answ4 = 55 - 25;
        message = scan.nextInt();
        boolean score4 = (message == answ4);
        fileMaker(fileName, pr4 + message + " " + score4);

        String pr5 = "3! = ";
        System.out.println(pr5);
        int answ5 = 3*2;
        message = scan.nextInt();
        boolean score5 = (message == answ5);
        fileMaker(fileName, pr5 + message + " " + score5);

        System.out.println("Thank you for playing, go to check your score!");

    }
    public static void fileMaker (String fileName, String content){
        try (FileWriter output = new FileWriter(fileName, true)){
            output.write(content +"\n");
        }

        catch (IOException e){
            System.out.println("opa: " + e);
        }
    }
}
