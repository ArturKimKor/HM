# HM
Home work


class Program
{
    static void Main()
    {
        int M = 1; 
        int N = 5; 

        string result = PrintNaturalNumbers(M, N);
        Console.WriteLine(result);
        
        M = 4;
        N = 8;

        result = PrintNaturalNumbers(M, N);
        Console.WriteLine(result);
    }

    static string PrintNaturalNumbers(int M, int N)
    {
        if (M > N)
            return "";

        if (M == N)
            return M.ToString();

        return M + ", " + PrintNaturalNumbers(M + 1, N);
    }
}






class Program
{
    static void Main()
    {
        int m = 2;
        int n = 3;

        int result = Ackermann(m, n);
        Console.WriteLine($"Ackermann({m}, {n}) = {result}");
    }

    static int Ackermann(int m, int n)
    {
        if (m == 0)
            return n + 1;
        else if (m > 0 && n == 0)
            return Ackermann(m - 1, 1);
        else if (m > 0 && n > 0)
            return Ackermann(m - 1, Ackermann(m, n - 1));
        else
            return -1; 
    }
}








class Program
{
    static void Main()
    {
        int[] array = { 1, 2, 5, 0, 10, 34 };

        PrintArrayReverse(array, array.Length - 1);
    }

    static void PrintArrayReverse(int[] array, int index)
    {
        if (index < 0)
            return;

        Console.Write(array[index] + " ");
        PrintArrayReverse(array, index - 1);
    }
}
