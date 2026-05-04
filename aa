
class Program
{
    static void Main()
    {
        double[] data = {
            115, 182, 191, 31, 196, 1099, 5, 172, 10, 179,
            83, 21, 20, 21, 186, 177, 195, 193, 188, 199,
            62, 109, 105, 183, 110
        };

        int n = data.Length;

        Array.Sort(data);

       
        double sum = 0;
        for (int i = 0; i < n; i++)
            sum += data[i];

        double mean = sum / n;

        
        double median;
        if (n % 2 == 0)
            median = (data[n / 2] + data[n / 2 - 1]) / 2;
        else
            median = data[n / 2];

        double mode = data[0];
        int maxCount = 1;

        for (int i = 0; i < n; i++)
        {
            int count = 0;
            for (int j = 0; j < n; j++)
            {
                if (data[j] == data[i])
                    count++;
            }
            if (count > maxCount)
            {
                maxCount = count;
                mode = data[i];
            }
        }


        double variance = 0;
        for (int i = 0; i < n; i++)
            variance += Math.Pow(data[i] - mean, 2);

        variance /= n;

       
        double stdDev = Math.Sqrt(variance);

        
        double Q1 = data[n / 4];
        double Q2 = median;
        double Q3 = data[(3 * n) / 4];

        double P20 = data[(int)(0.2 * n)];
        double P50 = median;

        double range = data[n - 1] - data[0];

        
        double IQR = Q3 - Q1;

        
        double lower = Q1 - 1.5 * IQR;
        double upper = Q3 + 1.5 * IQR;

        
        Console.WriteLine("Mean = " + mean);
        Console.WriteLine("Mode = " + mode);
        Console.WriteLine("Median = " + median);
        Console.WriteLine("Variance = " + variance);
        Console.WriteLine("Standard Deviation = " + stdDev);
        Console.WriteLine("Q1 = " + Q1);
        Console.WriteLine("Q2 = " + Q2);
        Console.WriteLine("Q3 = " + Q3);
        Console.WriteLine("P20 = " + P20);
        Console.WriteLine("P50 = " + P50);
        Console.WriteLine("Range = " + range);
        Console.WriteLine("IQR = " + IQR);
        Console.WriteLine("Sum = " + sum);

        Console.WriteLine("\nOutliers:");
        for (int i = 0; i < n; i++)
        {
            if (data[i] < lower || data[i] > upper)
                Console.WriteLine(data[i]);
        }
    }
}
