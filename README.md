Arylst
======
import java.io.*;
import java.util.*;

class Arylst
{
	static int read_int()throws IOException
	{
	    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		String text = br.readLine();
		int in = Integer.parseInt(text);
		return in;
	}
	
	static String read_string()throws IOException
	{
	    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		String text = br.readLine();
		return text;
	}
	
    public static void main(String[] args)
	{
		try
		{
			int i;
		    List <String> ary = new ArrayList <String> ();
			do
			{
				System.out.println("Select the task");
				System.out.println("\t1. add_item \n\t2.remove_item \n\t3.return_size \n\t4.check_item \n\t5.clear_item \n\t6.display_all \n\t7.exit");
				i = read_int();
			
				switch(i)
				{
					case 1:
						System.out.println("Enter the item to be added\t:");
						ary.add(read_string());
						System.out.println("Item entered!");
						continue;
						
					case 2:
						System.out.println("Enter the item to be removed\t:");
						ary.remove(read_string());
						System.out.println("Item removed!");
						continue;
						
					case 3:
						System.out.println("Size of arraylist\t:" + ary.size());
						continue;
						
					case 4:
						System.out.println("Enter the item to be checked\t:");
						System.out.println(ary.contains(read_string())? "Item is available" : "Item is not available");
						continue;
						
					case 5:
						ary.clear();
						System.out.println("Arraylist has been emptied!");
						continue;
						
					case 6:
						System.out.println("List of items in the array");
						Iterator itr = ary.iterator();
						while(itr.hasNext())
						{
							System.out.println(itr.next());
						}
						continue;
						
					default:
						System.out.println(" Enter values from 1 to 7 ");
						continue;
						
				}
			}while(i != 7);
		}
		
		catch(IOException e1)
		{
			e1.printStackTrace();
		}
		
		catch(Exception e2)
		{
			e2.printStackTrace();
		}
	}
}
			