# 5 Macam Time Complexity

##### Berikut adalah contoh 5 macam time complexity dalam bahasa C++

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
   ```
   #include <iostream>
   
   void pengurut_nomor();
   void pencari_nomor();
   int nomor[5] = {2, 5, 3, 1, 4};
   int cariNomor;

   int main()
   {
        std::cout << "Nomor : ";
        for(int i = 0; i < 5; i++)
        {
             std::cout << nomor[i];
        }
        std::cout << std::endl;
    
        std::cout << "Masukkan nomor yang ingin dicari : ";
        std::cin >> cariNomor;
    
        std::cout << "Nomor setelah diurutkan : ";
        pengurut_nomor();
        for(int x = 0; x < 5; x++)
        {
            std::cout << nomor[x];
        }
        std::cout << std::endl;
    
        pencari_nomor();
    
        return 0;
   }

   void pengurut_nomor()
   {
        int  i, banding, j, x;

        for(i = 0; i < 5; i++)
        {
             banding = i;
             for(j = i + 1; j < 5; j++)
             {
                  if(nomor[j] < nomor[banding])
                  {
                       banding = j;
                  }
             }
             x = nomor[i];
             nomor[i]  = nomor[banding];
             nomor[banding] = x;
        }
   }

   void pencari_nomor()
   {
        int awal, akhir, tengah, nomorDicari = 0;
      
        awal = 0;
        akhir = 5;
      
        while (nomorDicari == 0 && awal <= akhir)
        {
             tengah = (awal + akhir) / 2;
             if(nomor[tengah] == cariNomor)
             {
                  nomorDicari = 1;
                  break;
             }
             else if(nomor[tengah] < cariNomor)
             {
                  awal = tengah + 1;
             }
             else
             {
                  akhir = tengah - 1;
             }
        }

        if(nomorDicari == 1)
        {
             std::cout << "Nomor ditemukan pada urutan ke-" << tengah + 1 << std::endl;
        }
        else
        {
             std::cout << "Nomor tidak ditemukan";
        }
   }
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
   ```
   #include <iostream>
   #define n 5

   int main() 
   {
        int total = 0;
        int array[n] = {1, 2, 3, 4, 5};
	
        for(int i = 0; i < n; i++)
        {
             for(int j = 0; j < i; j++)
             {
                  total++;
             }
        }
	
        std::cout << total;
	
        return 0;
   }
5. O(2^n) | Exponential Time
   ```
   #include <iostream>

   long int faktorial(int x);

   int main()
   {
	    int r, hasil;
	
	    std::cout << "MENGHITUNG NILAI FAKTORIAL" << std::endl;
	    std::cout << std::endl;

	    std::cout << "Masukan Nilai = ";
	    std::cin >> r;
	
	    hasil = faktorial(r);
	    std::cout << "Faktorial " << r << "! = " << hasil;
   }

   long int faktorial(int x)
   {
	    if (x==1)
	    {
		  return(x);
	    }
	    else
        {
		  return(x * faktorial(x - 1));
        }
   }
