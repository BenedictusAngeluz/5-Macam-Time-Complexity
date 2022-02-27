# 5 Macam Time Complexity

1. O(1) | Constant Time
   #include <stdio.h>
   #define a 5

   main()
   {
	    int total = 0;
    	int array[a] = {1, 2, 3, 4, 5};
	
	    printf("%d", total);
    }
    
2. O(log n) | Logarithmic Time


3. O(n) | Linear Time
   #include <stdio.h>
   #define a 5

   main()
   {
	    int total = 0;
	    int array[a] = {1, 2, 3, 4, 5};
	
	    for(int i = 0; i < a; i++)
	    {
		      total += array[i];
	    }
	
	 printf("%d", total);
   }
  
4. O(n²) | Quadratic Time


5. O(2^n) | Exponential Time

