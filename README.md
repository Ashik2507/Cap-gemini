# Cap-gemini 
Create a program to accept the five Products name in an array and display the Products in an ascending order

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

class Source {

   public static String[] getProducts(String arr[]) {
      ArrayList<String> input = new ArrayList<String>(Arrays.asList(arr));
      Collections.sort(input);
      String[] result = new String[input.size()];
      for (int i = 0; i < result.length; i++) {
         result[i] = input.get(i);
      }
      return result;
   }

   public static void main(String[] args) {
      Scanner scanner = new Scanner(System.in);
      String inputArray[] = new String[5];
      for (int i = 0; i < inputArray.length; i++) {
         inputArray[i] = scanner.nextLine().trim();
      }
      String result[] = getProducts(inputArray);
      for (String str : result) {
         System.out.println(str);
      }
   }
}
