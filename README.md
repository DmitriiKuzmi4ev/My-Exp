# TinkoffMobile
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        int A = 100; // стимость трафика за месяц
        int B = 90; // количество трафика за 100 рублей (мегабайт)
        int C = 5; // сумма (рублей) за каждый превышенный мегабайт
        int D = 100; // планируемое колличество мегабайт, которое будет потрачено

        System.out.print("Введите стоимость за тариф: ");
        Scanner scan = new Scanner(System.in);
        int rent = scan.nextInt();

        System.out.print("Введите колличество мегабайт трафика по тарифу: ");
        Scanner scan1 = new Scanner(System.in);
        int number1 = scan.nextInt();

        System.out.print("Введите стоиомсть переплаты за каждый мегабайт сверх тарифа: ");
        Scanner scan2 = new Scanner(System.in);
        int number2 = scan.nextInt();

        System.out.print("Введите планируемое колличество мегабайт трафика по тарифу: ");
        Scanner scan3 = new Scanner(System.in);
        int number3 = scan.nextInt();

        if (number3 > B) {
            int result1 = number3 - B;
            int result2 = result1 * C;
            int result3 = A + result2;
            System.out.println("Плата по тарифу составит: " + result3);
        } else if (number3 < B) {
            int result1 = B - number3;
            int result2 = result1 * C;
            int result3 = A - result2;
            System.out.println("Плата по тарифу составит: " + result3);
        }
    }


}
