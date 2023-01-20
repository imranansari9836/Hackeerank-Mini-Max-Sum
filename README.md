import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

class Result {

    /*
     * Complete the 'miniMaxSum' function below.
     *
     * The function accepts INTEGER_ARRAY arr as parameter.
     */

    public static void miniMaxSum(List<Integer> arr) {
    // Write your code here
//total_sum=25
//25-1=24 min
//25-9=16 max
int min=arr.get(0);
int max=arr.get(0);
long total_sum=arr.get(0);
for(int i=1;i<arr.size();i++)
{
    total_sum=total_sum+arr.get(i);//25
    if(arr.get(i)<min)
    {
        min=arr.get(i);//1
    }
     if(arr.get(i)>max)
    {
        max=arr.get(i);//9
    }
}
System.out.println((total_sum-max)+" "+(total_sum-min));//16 24
   }

}


public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        String[] arrTemp = bufferedReader.readLine().replaceAll("\\s+$", "").split(" ");

        List<Integer> arr = new ArrayList<>();

        for (int i = 0; i < 5; i++) {
            int arrItem = Integer.parseInt(arrTemp[i]);
            arr.add(arrItem);
        }

        Result.miniMaxSum(arr);

        bufferedReader.close();
    }
}
