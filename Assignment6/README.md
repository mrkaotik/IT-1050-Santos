using System;

public class Person
{
	int age;
	string firstName;
	string lastName;
	Person spouse;
	
	string GetFullName (string first, string last)
	{
		string fullName = first + " " + last;
		return fullName;
	}
	
	void PrintNameAndAge()
	{
		Console.WriteLine(GetFullName(firstName, lastName));
		Console.WriteLine("Age " + age);
	}
	
		public static void Main()
	{
		int numberOfPeople= 0;
		int sumOfAllAges =0;
		//Console.WriteLine("Hello World!");
		Person person1 = new Person();
		Console.WriteLine("Enter Your First Name				:");
		string firstname = Console.ReadLine();
		person1.firstName = firstname; 
		Console.WriteLine("Enter Your Last Name				:");
		string lastname = Console.ReadLine();
		person1.lastName = lastname;
		Console.WriteLine("Enter Your Age				:");
		int age = Convert.ToInt32(Console.ReadLine());
		person1.age = age;
		numberOfPeople++;
		sumOfAllAges+= age;	
		
		bool maritalStatus= false; 
		int answer = 0;
		Console.WriteLine("Is the Person married? 1 for yes, 2 for no:");
		answer = Convert.ToInt32(Console.ReadLine());
		if ( answer	== 1)
		{
			maritalStatus = true;
		}
			
		if (maritalStatus == true)
		{
		Console.WriteLine("Enter Your Spouse's First Name				:");
		string spousefirstname = Console.ReadLine();		
		person1.spouse.firstName = spousefirstname;
		person1.spouse.lastName = lastname; 
		Console.WriteLine("Enter Your Spouse's Age				:");
		int spouseage = Convert.ToInt32(Console.ReadLine());
		person1.spouse.age = spouseage;
		person1.spouse.spouse = person1;
		numberOfPeople++;
		sumOfAllAges+= spouseage;	
		}
		else
		{
			person1.spouse = null;
		}

		Person person2 = new Person();
		Console.WriteLine("Enter Your First Name				:");
		string firstname2 = Console.ReadLine();
		person2.firstName = firstname2;
		Console.WriteLine("Enter Your Last Name				:");
		string lastname2 = Console.ReadLine();
		person2.lastName = lastname2;
		Console.WriteLine("Enter Your Age:");
		int age2 = Convert.ToInt32(Console.ReadLine());
		person2.age = age2;
		numberOfPeople++;
		sumOfAllAges+= age2;	

		 maritalStatus= false; 
		 answer = 0;
		Console.WriteLine("Is the Person married? 1 for yes, 2 for no:");
		answer = Convert.ToInt32(Console.ReadLine());
		if ( answer	== 1)
		{
			maritalStatus = true;
		}
			
		if (maritalStatus == true)
		{
		Console.WriteLine("Enter Your Spouse's First Name				:");
		string spousefirstname = Console.ReadLine();		
		person2.spouse.firstName = spousefirstname;
		person2.spouse.lastName = lastname; 
		Console.WriteLine("Enter Your Spouse's Age				:");
		int spouseage = Convert.ToInt32(Console.ReadLine());
		person2.spouse.age = spouseage;
		person2.spouse.spouse = person2;
		numberOfPeople++;
		sumOfAllAges+= spouseage;	
		}
		else
		{
				person1.spouse = null;
		}
			
		Console.WriteLine("Person 1: ");
		person1.PrintNameAndAge();
	
		Console.WriteLine("Person 1 Spouse: ");
		person1.spouse.PrintNameAndAge();
			
		Console.WriteLine("Person 2: ");
		person2.PrintNameAndAge();
			
		Console.WriteLine("Person 2 Spouse: ");
		person2.spouse.PrintNameAndAge();
			
		int averageAge = sumOfAllAges/numberOfPeople;
		Console.WriteLine("Average age: " + averageAge);
	}
}
