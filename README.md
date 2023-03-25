# Stack
package basic.dev;

import java.util.Scanner;
import java.util.Stack;

public class MainApp {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
       Scanner sc = new Scanner(System.in);
       Stack<Integer> s = new Stack<Integer>();
       s.push(1);
       s.push(2);
       s.push(3);
       
       int count = s.size();
       System.out.println("số phần tử của stack:" + count);
       
       System.out.println("Nhap phan tu muon xuat");
       int n = sc.nextInt();
       System.out.println("phần tử trong stack :" + s.get(n+1));
       
       System.out.println("nội dung của stack: " + s);
       
       System.out.println("Nhập phần tử muốn loại");
       int indexToRemove = sc.nextInt();
       int removedElement = s.remove(indexToRemove);
       System.out.println("loại phần tử " + indexToRemove+":" + removedElement);
       
       
       System.out.println("Phần tử gốc:" + s);
       
       Stack<Integer> tempStack = new Stack<Integer>();
       while (s.isEmpty()) {
    	   tempStack.push(s.pop());
       }
       s= tempStack;
       System.out.println("Phần tử đảo" + s);
	}

}
