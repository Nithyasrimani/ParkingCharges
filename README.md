# ParkingCharges
import java.util.Scanner;

public class ParkingCharges {
   public static void main(String[] args) {
      
      double hours, parkingfee;    
      double totalparkingfee = 0.00;
      int sentinel = -1;  
      Scanner in = new Scanner(System.in);

      
      System.out.print("Enter the hours parked (-1 to end): " );
      hours = in.nextDouble();   

      while (hours != sentinel) {
        
         if (hours <= 3) {
            parkingfee = 2.00;
         } else {
            parkingfee = 2.00 + (Math.ceil(hours - 3))*0.5;
         }

         if (parkingfee <= 10.00) {
            parkingfee = parkingfee;
         } else {
            parkingfee = 10.00;
         }

         System.out.printf("Parking fee is: $" + String.format("%.2f", parkingfee));


         totalparkingfee += parkingfee;

         System.out.printf("Enter the hours parked (-1 to end): " );
         hours = in.nextDouble();
      }
      System.out.printf ("Your total parking fee is: $" + String.format("%.2f", totalparkingfee));
      System.out.printf("bye");
      in.close();
   }
}
