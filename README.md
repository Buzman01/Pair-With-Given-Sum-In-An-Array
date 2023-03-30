# Pair-With-Given-Sum-In-An-Array
Given an integer array of size n and an integer X, we need to determine if there exist two unique elements in the array such that their sum is X. If there are no such elements, we should print There is no such pair.
#include <bits/stdc++.h>
using namespace std;
void isPairAvailable(int n,int X,int input_array[])
{
    int i,j;
    for(i=0;i<n;i++)
    {
        for(j=i+1;j<n;j++)
        {
            if(input_array[i]+input_array[j]==X)
            {
                cout <<"The two numbers are "<< input_array[i]<<" and "<< input_array[j]<< endl;
                return;
            }
        }
    }
    cout<<"There is no such pair"<<endl;
}
int main()
{
    int X=7,input_array[]={1, 5, 3, -2, 4, 7};
    int n=sizeof(input_array)/sizeof(input_array[0]);
    isPairAvailable(n, X, input_array);//calling the function
    return 0;
}

{tab title="Java" class="red"}

/* This code is contributed by Tammisetti Naveen*/
Import java.util.*;
public class PairSum
{
	public static void isPairAvailable(int n,int X,int input_array[])
	{
		//iterating the first element from 0 to n-1
		for (int i = 0; i< n; i++)
		{
			for (int j = i+1; j < n; j++) //iterating the second element from i+1 to n-1
			{
				if (input_array[i] + input_array[j] == X)//checking the sum of each pair
				{
					System.out.print("The two numbers are "+input_array[i] +" and "+ input_array[j]);
					return;
				}
			}
		}
		System.out.print ("There is no such pair");//if there is no pair with given sum
	}
	public static void main(String arg[])
	{
		int X = 7, input_array[] = { 1, 5, 3, -2, 4, 7};
		int n = input_array.length;
		isPairAvailable(n, X, input_array);//calling the function
	}
}
{tab title="Python" class="green"}

''' This code is contributed by Arun Reddy'''
def isPairAvailable(input_array, X):
    n=len(input_array)
    for i in range(n):
        for j in range(i+1,n):
            if input_array[i]+input_array[j]==X:
                print("The two numbers are "+str(input_array[i])+" and "+str(input_array[j]))
                return
    print("There is no such pair")
if __name__=="__main__":
    X = 7
    input_array = [1, 5, 3, -2, 4, 7]
    input_array.sort()
    isPairAvailable(input_array,X)
