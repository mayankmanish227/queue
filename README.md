# queue
package com;

public class day2
{
	public static void main(String []args)
	{
		day2 obj=new day2();
		obj.insert(1);
		obj.insert(2);
		obj.insert(3);
		obj.insert(4);
		obj.insert(5);
		obj.delete();
		obj.delete();
		obj.delete();
		obj.delete();
		obj.display();
		
	}
	int size=5;
	int[] arr=new int[size];
	int front=-1;
	int rear=-1;
	void insert(int ele)
	{
		if(rear==size)
		{
			System.out.println("queue is full");
		}
		else
		{
			rear++;
			arr[rear]=ele;
			//rear++;
		}
		
	}
	void delete()
	{
		if(front==-1 && rear==-1)
		{
			System.out.println("queue is empty");
		}
		else
		{
			for(int i=0;i<size;i++)
			{
				int a=arr[front+i+1];
				arr[i]=a;
			}
			rear--;
		}
		
	}
	void display()
	{
		for(int i=0;i<=rear;i++)
		{
			System.out.println(arr[i]);
		}
	}
}
