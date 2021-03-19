using System;
					
public class Program
{
	public static void Main()
	{
		//double//
		double science = 89.8;
		double math = 78.8;
		double english = 90;
		double average = (science + math + english)/ (3);
		
		Console.WriteLine("your average is: " + average);
		//int//
		int a = 5;
		int b = 9;
		int c =7;
		int total = a + b - c;
	
Console.WriteLine("total = " + total);
		// string//
		string city = "Strongsville";
		string state = "Ohio";
		string address = (city + state);
		Console.WriteLine("Your address is: "  + address);
		
		//bool//
		bool summerIsHot = true;
		bool winterIsWarm = false;
		bool pool = summerIsHot;
		
		Console.WriteLine("pool is for hot weather " + pool);
		
					  
	}
}
