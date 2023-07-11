# PrintLinkedList
import java.io.*;
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        LinkedList list=new LinkedList();
        while(true){
            int n=sc.nextInt();
            if(n<0)
                break;
            else{
                list.insertAtEnd(n);
            }
        }
        list.display();
    }
}
    class LinkedList{
        Node head,tail;
        LinkedList(){
            head=null;
            tail=null;
        }
        class Node{
            int data;
            Node next;
            Node(int val){
                data=val;
                next=null;
            }
        }
        public void insertAtEnd(int val){
            Node n=new Node(val);
            if(head==null){
                head=n;
                tail=n;
            }
            else{
                tail.next=n;
                tail=n;
            }
        }
        public void display(){
            Node temp=head;
            while(temp!=null){
                System.out.print(temp.data+" ");
                temp=temp.next;
            }
        }
        
    }
