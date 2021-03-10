using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace cracking_the_coding_intvw_oop
{
    class Calculator
    {
        public void RunCalculator()
        {
            string[] operatori = new string[4] { "+","-","*","/"};
            string typeOperator;
            int no1, no2;
            int rezultat;
            string restartCheck;

            //tipul operatorului
            Console.WriteLine("Alege tipul operatiei : +, -, *, /");
            typeOperator = GetOperator(operatori);

            Console.WriteLine("no1");
            no1 = GetCalcNum();
            Console.WriteLine("no2");
            no2 = GetCalcNum();

            rezultat = Calculate(no1, no1, typeOperator);

            Console.WriteLine("rezultatul e {0}. Scrie yes daca vrei sa continui", rezultat);
            restartCheck = Console.ReadLine();
            if (restartCheck == "yes")
            {
                RunCalculator();
            }
            else
            {
                Environment.Exit(0);
            }
        }
       
        public string GetOperator(string[] oper)
        {
            string type = Console.ReadLine();
            while (!oper.Contains(type))
            {
                Console.WriteLine("operatorul tb sa fie valid");
                type = Console.ReadLine();
            }
            return type;
        }
                 
        private int GetCalcNum()
        {
            int num;
            bool parseCheck = int.TryParse(Console.ReadLine(), out num);
            while (!parseCheck)
            {
                Console.WriteLine("incearca sa introduci un nr ");
                parseCheck = int.TryParse(Console.ReadLine(), out num);
            }
            return num;

        }
        public int Calculate(int no1,int no2,string type)
        {
            int result;
            if (type == "+")
            {
                result = no1 + no2;
                return result;
            }
            else if (type == "-")
            {
                result = no1 - no2;
                return result;
            }
            else if (type == "*")
            {
                result = no1 * no2;
                return result;
            }
            else if (type == "/")
            {
                result = no1 / no2;
                return result;
            }
            return -1;
        }
    }
   
}
