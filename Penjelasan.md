# 5 Macam Time Complexity

1. O(1) | Constant Time
   ```
   #include <iostream>
   #define a 5

   int main() 
   {
       int total = 0;
       int array[a] = {1, 2, 3, 4, 5};
	
       std::cout << total;

       return 0;
   }
2. O(log n) | Logarithmic Time


3. O(n) | Linear Time
   ```
   #include <iostream>
   #define a 5

   int main() 
   {
        int total = 0;
        int array[a] = {1, 2, 3, 4, 5};
	
        for(int i = 0; i < a; i++)
        {
             total += array[i];
        }
	
        std::cout << total;
	
        return 0;
   }
4. O(n²) | Quadratic Time


5. O(2^n) | Exponential Time

