
import java.util.ArrayList;
import java.util.Scanner;


public class ReverseArrayToM {

    public static void reverseArray(ArrayList<Integer> arr, int m)
    {
    	int start = m+1;
    	if (start>arr.size()) {return;}
    	int end = arr.size()-1;
    	while(start<=end) {
    		int temp = arr.get(start);
    		arr.set(start,arr.get(end));
    		arr.set(end,temp);
    		start+=1;
    		end-=1; 
    	}
    	System.out.println(arr);
    	

    }
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in); 
		ArrayList<Integer> arr = new ArrayList<>(); 
		int size = sc.nextInt();
		int M = sc.nextInt(); 
		for(int i = 0; i<size;i++) {
			arr.add(sc.nextInt()); 
		}
		reverseArray(arr,M);
		
		
	}

}
