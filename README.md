# 1d-chararray
holds chars in an array 20  off sets between them
/*
 * Alaa Harajli 
 * EMU COSC 471 Susan haynes 
 * 9/13/18
 * https://github.com/AHarajli/1d-chararray/new/master?readme=1
 * 
 * 
 * 
 */

import java.util.Scanner;

public class driver {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		char[]e;
		Scanner input = new Scanner(System.in);
		int number=0;
		record dat = new record( e=new char[200]);
		dat.INSERT("A", "a", "0");
		dat.INSERT("B", "b", "1");
		dat.INSERT("C", "c", "2");
		System.out.println(dat.toString());
		System.out.println("pick record 0,1 or 2");
		number=input.nextInt();
		dat.outRec(number);
	}

}
/*
 * Alaa Harajli 
 * EMU COSC 471 Susan haynes 
 * 9/13/18
 * https://github.com/AHarajli/1d-chararray/new/master?readme=1
 * 
 * 
 * 
 */

import java.util.Arrays;

public class record {
	char[] rec = new char[200];
	int offSet = 0;
	int count = 20;
	int i = 0;

	public record(char[] rec) {
		super();
		this.rec = rec;
	}

	public void setOffSet(int offSet) {
		this.offSet = offSet;
	}

	/*
	 * prints the records the user selects
	 */
	public void outRec(int t) {
		if (t == 0) {
			for (int z = 0; z < 60; z++) {
				System.out.print(rec[z]);
			}
		}
		if (t == 1) {
			for (int z = 60; z < 120; z++) {
				System.out.print(rec[z]);
			}
		}
		if (t == 2) {
			for (int z = 120; z < 180; z++) {
				System.out.print(rec[z]);
			}
		}
	}

	/*
	 * places the chars at the proper offsets
	 */
	public void INSERT(String a, String b, String c) {
		rec[offSet] = a.charAt(i);
		setOffSet(offSet + count);
		rec[offSet] = b.charAt(i);
		setOffSet(offSet + count);
		rec[offSet] = c.charAt(i);
		setOffSet(offSet + count);
	}

	@Override
	public String toString() {
		return Arrays.toString(rec);
	}

}
