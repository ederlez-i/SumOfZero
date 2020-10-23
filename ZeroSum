/*
multiple pointers(tag) method for ordered arrays.
Find two elements in an ordered array whose sum equal to zero
*/
#include<iostream>
#include<cstring>

using namespace std;

#define  ARR_SIZE 10

bool isSumZero(int a[], int arrLen,int retArr[]);
void PrintArr(int arr[], int arrLen);

int main()
{
	int arr1[ARR_SIZE] = {-9,-6,-4,-2,-1,0,1,3,4,8};	
	int arrRet[2]={0};

	PrintArr(arr1,ARR_SIZE);
	if(isSumZero(arr1,ARR_SIZE,arrRet))
	{
		cout<<"index of inetegers: ";
		PrintArr(arrRet ,2 );	
		cout<<"inetegers: "<<arr1[arrRet[0]]<<" , "<<arr1[arrRet[1]]<<endl;	
	}
	else
		cout<<"no elements"<<endl;
	
	return 0;
}
/*print array values*/
void PrintArr(int arr[], int arrLen)
{
	if(arrLen==0)
		return ;
	
	cout <<arr[0];
	for(int i=1;i<arrLen;i++)
		cout <<","<<arr[i];
	cout<<endl;
}
/*
define two pointers(tags)
one of them is for left most element other is for right most element in the array.
move pointers to the middle until sum of values is zero
*/
bool isSumZero(int arr[],int arrLen,int retArr[])
{	
	int sum = 0;
	int left = 0;
	int right = arrLen -1;

	while(left<right)
	{
		//sum of left and right pointers value
		sum = arr[left] + arr[right];
		if(sum == 0)
		{
			retArr[0] = left;
			retArr[1] = right;
			return true;			
		}
		//move right pointer 1 step to the left
		else if(sum>0)
			right--;
		//move left pointer 1 step to the rigt 
		else
			left++;			
	}	

	return false;
}
