# Bir sayidizisindeki tekrar eden çift sayilari
import javax.xml.stream.events.StartDocument;
import java.sql.SQLOutput;
import java.util.Arrays;

public class Main {

    static boolean isFind(int[] arr, int value) {


        for (int i : arr) {
            if (i == value) {
                return true;
            }
        }
        return false;
    }
    public static void main(String[] args) {

        int[] list = {4, 7, 4, 4, 3, 2, 2, 10, 10, 1, 33, 9, 1};

        int[] dublicate = new int[list.length];
        int startIndex = 0;


        for (int i = 0; i < list.length; i++) {

            for (int j = 0; j < list.length; j++) {

                if ((i != j) && list[i] == list[j] && list[i]%2==0) {
                    if(!isFind(dublicate, list[i])){
                        dublicate[startIndex++]=list[i];
                    }
                    break;
                }
            }
        }

        for(int x:dublicate){
            if(x!=0){
                System.out.println(x);
            }
        }
   }
}
