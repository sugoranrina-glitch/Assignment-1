# Assignment-1
/******************************************************************************

                            Online C# Compiler.
                Code, Compile, Run and Debug C# program online.
Write your code in this editor and press "Run" button to execute it.

*******************************************************************************/

using System;

namespace Assignment1
{
    // Student Class
    class Student
    {
        // Attributes
        public string studentID;
        public string name;
        public string course;

        // Constructor
        public Student(string studentID, string name, string course)
        {
            this.studentID = studentID;
            this.name = name;
            this.course = course;
        }

        // Method to display student info
        public void DisplayInfo()
        {
            Console.WriteLine("Student ID: " + studentID);
            Console.WriteLine("Name: " + name);
            Console.WriteLine("Course: " + course);
            Console.WriteLine();
        }
    }

    // BankAccount Class
    class BankAccount
    {
        // Private attributes
        private string accountNumber;
        private string accountHolder;
        private double balance;

        // Constructor
        public BankAccount(string accountNumber, string accountHolder, double balance)
        {
            this.accountNumber = accountNumber;
            this.accountHolder = accountHolder;
            this.balance = balance;
        }

        // Deposit method
        public void Deposit(double amount)
        {
            balance += amount;
            Console.WriteLine("Deposited: " + amount);
        }

        // Withdraw method
        public void Withdraw(double amount)
        {
            if (amount <= balance)
            {
                balance -= amount;
                Console.WriteLine("Withdrawn: " + amount);
            }
            else
            {
                Console.WriteLine("Insufficient balance. Withdrawal denied.");
            }
        }

        // Display balance method
        public void DisplayBalance()
        {
            Console.WriteLine("Current Balance: " + balance);
            Console.WriteLine();
        }
    }

    // Main Program
    class Program
    {
        static void Main(string[] args)
        {
            // Create Student objects
            Student student1 = new Student("2024302831", "Jhon mark Lupeña", "BS Electronic Mechanical Technology");
            Student student2 = new Student("2022308647", "Rina Sugoran", "BS Information Technology");

            // Display student information
            student1.DisplayInfo();
            Console.WriteLine("------------");
            student2.DisplayInfo();


            // Create BankAccount object
            BankAccount account = new BankAccount("123456789", "Jhon mark gwapo", 5000);

            // Perform transactions
            account.Deposit(0);
            account.Withdraw(2000);
            account.DisplayBalance();

            Console.ReadLine();
        }
    }
}
