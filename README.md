# Simple-tasks-on-JAVA-Task-1
Создайте программу, которая будет принимать две группы параметров:  * - количество циклов выполнения программы;  * - 3 числа a, b, n  * и выводить на экран последовательность результатов вычисления следующего выражения  * (a + 2^0*b),(a + 2^0*b + 2^1*b),(a + 2^0*b + 2^1*b + 2^2*b)..., (a+2^0*b + 2^1*b + 2^2*b +...+ 2^(n-1)*b)  * где ^ обозначает возведение в степень, и эта операция выполняется до умножения.  *  * Пример:  *  Please enter the number of iterations  *   2  *  Enter the group of 3 numbers  *   0 2 10  *  Output:  *   2 6 14 30 62 126 254 510 1022 2046  *  Enter the group of 3 numbers  *   5 3 5  *  Output:  *  8 14 26 50 98  *  *  Пример:  *  a=5, b=3, n=5  *  (5+2^0*3)=8,(5+2^0*3 + 2^1*3)=14,(5+2^0*3 + 2^1*3 + 2^2*3)=26,(5+2^0*3 + 2^1*3 + 2^2*3 + 2^3*3)=50,  *  (5+2^0*3 + 2^1*3 + 2^2*3 + 2^3*3 + 2^4*3)=98  *  */


import java.util.Scanner;
public class homewprk {
    public static void main(String[] args) {
        System.out.print("Enter a ");
        Scanner in = new Scanner(System.in);
        int a =in.nextInt();
        System.out.println("Enter b ");
        int b =in.nextInt();
        System.out.println("Please enter the number of iterations " );
        int n =in.nextInt();
        Expr(a,b,n);
         }

    public static void Expr(int a, int b, int n) {

        int result_temp = 0;
        for (int i =0 ; i<n; i++)
        {
            result_temp = result_temp + (int)Math.pow(2,i)*b;
            System.out.println(a+result_temp);
        }
    }
}
