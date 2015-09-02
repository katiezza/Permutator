# Permutator


import java.util.Arrays;

public class Permutator {

	public static void main(String[] args) {
		int[] arr = {1, 2, 3};
		permute(arr, 0);
	}

	public static void permute(int[] arr, int idx) {
		if(idx == arr.length - 1) {
			System.out.println(Arrays.toString(arr));
			return;
		}
		for(int i = idx; i < arr.length; i++){
			swap(arr, i, idx);
			permute(arr, idx + 1);
			swap(arr, idx, i);
		}
	}
	public static void swap(int[] arr, int a, int b){
		int tmp = arr[a];
		arr[a] = arr[b];
		arr[b] = tmp;
	}
}

