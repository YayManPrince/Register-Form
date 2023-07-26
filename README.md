using System.Collections;
using System.Threading.Tasks;
using System.Text;
using System;

namespace Register
{
    /*creaing a Register Form, that will require the user to enter their
     name, last name, email, and require them to create a password */
     
    class RegisterF
    {
        public static void Main(string[] args)
        {
            //promting the user for the register
            
            Console.WriteLine("Please Enter Your First Name: ");
            string fName = Console.ReadLine(); //name saved
            Console.WriteLine("Please Enter Your Last Name: ");
            string sName = Console.ReadLine(); //last name saved
            Console.WriteLine("Please Enter Your Email: ");
            string mail = Console.ReadLine();// email saved
            Console.WriteLine("please create password: ");
            string passWord = Console.ReadLine(); //password saved
            Console.WriteLine("Confirm password: ");
            string cPassWord = Console.ReadLine(); //password confirmation saved

            /*using a conditional statement to compare the password 
              and the confirm password */
            if (cPassWord == passWord)
            {
                Console.WriteLine("Password Confirmed! ");

            }
            else
            {
                /* using a while loop to allow the program to 
                 continue to prompt the user for the correct password,
                without not having to start over the program */ 
                while (cPassWord != passWord)
                {
                    Console.WriteLine("Password does not match");
                    Console.WriteLine("Confirm password: ");
                    cPassWord = Console.ReadLine();
                }
                Console.WriteLine("Password Confirmed!");
            }
            //promts the user to see the details that they entered 
            Console.WriteLine("\n Enter 'Y' to view details and any other key to exit");
            string ans = Console.ReadLine();//saves user answer(ans)
            
            /*based on the user answer we use the if statement to show the user their details
             or continue to close the program */
            if (ans == "Y" || ans == "y")
            {
                Console.WriteLine(fName + " " + sName);//displays Name and last name
                Console.WriteLine(mail);//displays the email
                //using a subsring to display only part of the password for 'security'
                Console.WriteLine("****" + cPassWord.Substring(3));
            }
            else
            {
                Console.WriteLine("Exit");
            }
            
        }
    }
}
