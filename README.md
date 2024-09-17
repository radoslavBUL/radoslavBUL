package Demo;

import java.util.Scanner;

public class Demo {
    public static void main(String[] args) {
        Scanner scanner=new Scanner(System.in);

        double budget = Double.parseDouble(scanner.nextLine());
        int extras = Integer.parseInt(scanner.nextLine());
        double clothing = Double.parseDouble(scanner.nextLine());

        double extrasAndClothing= extras*clothing;
        double decor = budget - (budget*0.90);
        if (extras >= 150){
            clothing = clothing-(clothing*0.10);
        }
        double decorAndClothing = decor + clothing;
        double diff = Math.abs(decorAndClothing-budget+extrasAndClothing);
        if(decorAndClothing > budget){
            System.out.println("Not enough money!");
            System.out.printf("Wingard needs %.2f leva more.", diff);
        }else{
            System.out.println("Action!" );
            System.out.printf("Wingard starts filming with %.2f leva left.", diff);
        }

    }
}

