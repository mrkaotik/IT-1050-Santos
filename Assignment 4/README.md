using System;
					
public class Program
{
	public static void Main()
	{

		Console.WriteLine("Enter value for w");
		int w = Int32.Parse(Console.ReadLine());
		
		Console.WriteLine("Enter value for x");
		int x = Int32.Parse(Console.ReadLine());
		
		Console.WriteLine("Enter value for y");
		int y = Int32.Parse(Console.ReadLine());
		
		Console.WriteLine("Enter value for z");
		int z = Int32.Parse(Console.ReadLine());
		
		int total = w *(y + z);
		
		Console.WriteLine("Your total is " + total);
	}
}
