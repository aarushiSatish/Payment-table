# Payment-table
import java.util.*;

import java.text.*;

public class PaymentTable {

public static void main(String[] args) {

// TODO Auto-generated method stub

DecimalFormat df = new DecimalFormat("0.00");

Scanner inp = new Scanner(System.in);

System.out.println(" Enter the Principal");

double principal = inp.nextDouble();

System.out.println("Enter the Anual Interest Rate");

double IntrRate = inp.nextDouble();

System.out.println("Enter the Monthly Payment");

double monthPayment = inp.nextDouble();

double MonthIntrRate = IntrRate/12;

int MnthNum = 0;

double newBalance = 0.0;

System.out.println("Month"+" "+

"Principal"+ " " +

"Interest"+" " +

"Payment" + " " +

"New Balance");

do

{

MnthNum++;

double mnthIntr = (principal * ( MonthIntrRate / 100));

newBalance = principal + mnthIntr - monthPayment;

System.out.print(MnthNum+ "   " +

df.format(principal)+"    " +

df.format(mnthIntr) + "   " +

monthPayment + "    " +

df.format(newBalance)

);

System.out.println("   " );

principal = newBalance;

} while ( newBalance > monthPayment);

inp.close();

}

}
