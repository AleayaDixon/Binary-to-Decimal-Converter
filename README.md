/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package binary.to.decimal.converter;
import java.util.Scanner;
import java.lang.Math;

/**
 *
 * @author Aleaya
 */
public class BinaryToDecimalConverter {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Scanner keyboard;
        keyboard = new Scanner(System.in);
        int binToDec[] = new int[20];
        System.out.println("Please insert the first digit of a binary number starting from the right.");
        int bin = keyboard.nextInt();
        int exp = 0;
        int dec = 0;
        int num;
        while(bin == 1 || bin == 0)
        {
            binToDec[exp] = bin;
            if (bin == 1)
            {
                num = (int)Math.pow(2,exp);
                //num = 2^exp;
                dec += num;
                System.out.print(dec);
                exp +=1;
            }
            else
            {
                dec += 0;
                exp +=1;
                System.out.print(dec);
                //System.out.print(dec);
            }
            //exp +=1;
            System.out.println("Please insert the next digit of a binary number. Enter a number other that 0 or 1 to calculate the decimal number.");
            bin = keyboard.nextInt();
        }
        for(int i = (exp-1); i>=0; i--)
        {
            System.out.print(binToDec[i]);
        }
        System.out.print(" in decimal is " + dec);
        keyboard.close();
    }
    
}
