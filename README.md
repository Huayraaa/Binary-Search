//Binary-Search

public static int rank(int[] array, int k)
{
	int front = 0, rear = array.length - 1;
		
	while(front <= rear)
	{
		int mid = front + (rear - front) / 2;
		if(k > array[mid]) front = mid + 1;
		else if(k < array[mid]) rear = mid -1;
		else return mid;
	}
	return -1;
}
