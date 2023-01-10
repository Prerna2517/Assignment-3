# Assignment-3
In this i use java language and written a source code of getting a length of a linked list.


class Length
{
	int value;
	Length next;
	Length(int d) { value = d; next = null; }
}


class MyList
{
	
	Length head;

	
	public void push(int new_data)
	{
		/* 1 & 2: Allocate the Node &
				Put in the data*/
		Length new_node = new Length(new_data);

		// 3. Make next of new Length as head
		new_node.next = head;

		// 4. Move the head to point to new Node
		head = new_node;
	}

	// Returns count of nodes in linked list
	public int getCount()
	{
		Length temp = head;
		int count = 0;
		while (temp != null)
		{
			count++;
			temp = temp.next;
		}
		return count;
	}

	// Driver code
	public static void main(String[] args)
	{
		// Start with the empty list
		MyList llist = new MyList();
		llist.push(1);
		llist.push(3);
		llist.push(1);
		llist.push(2);
		llist.push(1);

		System.out.println("Count of nodes is " +
							llist.getCount());
	}
}
