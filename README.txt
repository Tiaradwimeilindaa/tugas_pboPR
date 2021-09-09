#nomer 1
import java.util.Scanner;
public class PrimeNumber {
    public static void main(String[] args) {  
        boolean bilanganPrima = true;
        Scanner input = new Scanner(System.in);
        System.out.println ("masukkan angka : ");
        int angka = input.nextInt();
        for (int index=2; index<=angka/2; index++){
            if (angka%index == 0){
                bilanganPrima = false ;
                break;
            }
        } 
        if(bilanganPrima){
            System.out.println(angka+" : bilangan prima");
        }
        else {
            System.out.println(angka+" : bukan bilangan prima");
        }
    }
}


#nomer 2
import java.util.Scanner;
public class GanjilGenap {
    public static void main (String args[])
    {
        Scanner input = new Scanner(System.in);
        System.out.println("masukkan angka :");
        int angka;
        angka = input.nextInt();
        
        if (angka % 2 ==0 ){
            System.out.println(angka + " bilangan genap");
        }else{
            System.out.println(angka + " bilangan ganjil");
        }
    }
}


#nomer 3:
import java.io.*;

public class binary {
    public static void main(String[] args) {
        BufferedReader input = new BufferedReader(new InputStreamReader(System.in));
        try {
            System.out.print("Input Number : ");
            int index = 0;
            int number = Integer.parseInt(input.readLine());
            int[] binary = { 1, 7, 14, 25, 50, 43, 66, 88, 91};
            int binaryLen = binary.length; // len(array)
            for (int x : binary) { // for x in array
                if (number == x) {
                    System.out.println("Number is in array at index - " + index);
                    break;
                }
                index++;
            }
            if (index == binaryLen) {
                System.out.println("Number is not in array!");
            }
        } catch (IOException exception) {
            System.out.println("Error input!");
        }
    }
}


#nomer 4 :
import java.io.*;
import java.util.Arrays;

public class dragon {
    public static void main(String[] args) {
        BufferedReader input = new BufferedReader(new InputStreamReader(System.in));
        try {
            System.out.print("input number of Knight : ");
            int number = Integer.parseInt(input.readLine());
            int Knight[] = new int[number];
            for( int i = 0; i < Knight.length; i++ ){
                int y = i+1;
                System.out.print("Knight ke-" + y + ": ");
                Knight[i] = Integer.parseInt(input.readLine());
            }
            System.out.print("input number of Dragon : ");
            int numberin = Integer.parseInt(input.readLine());
            int[] dragon = new int[numberin];
            for( int i = 0; i < dragon.length; i++ ){
                int x = i+1;
                System.out.print("dragon ke-" + x + ": ");
                dragon[i] = Integer.parseInt(input.readLine());
            }
            Arrays.sort(Knight); 
            Arrays.sort(dragon); 
            int indeksDragon = 0; 
            int power = 0; 
            for (int x : Knight) {
                if (indeksDragon < dragon.length) {
                    if (x >= dragon[indeksDragon]) { // dragon[1]
                        power += x;
                        indeksDragon++;
                    }
                }
            }
            System.out.println("---------------------------");
            if (indeksDragon == dragon.length) { // len(dragon)
                System.out.println("Minimum power : " + power);
            } else {
                System.out.println("Knight Fall");
            }
        } catch (IOException exception) {
            System.out.println("Error input!");
        }

    }
}


