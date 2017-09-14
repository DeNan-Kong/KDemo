import java.util.Scanner;

public class Main {

    static void magic_coin(int n ,String count){

        if(n == 0){
            System.out.println(count);
        }else if( n%2 == 0 & n != 0){
            count= "2" + count;
            magic_coin((n-2)/2,count);
        } else {
            count = "1" + count;
            magic_coin((n-1)/2,count);
        }
    }

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int coin = in.nextInt();
        //1:1-3-7-15-31-63-
        //2:2-6-14-30-62-126-

        magic_coin(coin,"");
    }
}
