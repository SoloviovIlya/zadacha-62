//Напишите программу, которая заполнит спирально массив 4 на 4.
//Например, на выходе получается вот такой массив:
//01 02 03 04
//12 13 14 05
//11 16 15 06
//10 09 08 07

int[,] a = new int [4,4];

int s = 1;

for (int j =0; j<4; j++)

{

    a[0,j] = s;
    
    s++;
    
}

for (int i =1;i<4;i++)

{

    a[i,3] = s;
    
    s++;
    
}

for (int j = 2; j>-1;j--)

{

  a[3,j] = s;
  
  s++;
  
}

for (int i =2;i>0;i--)

{

    a[i,0] = s;
    
    s++;
    
}

for (int j =1;j<3;j++)

{

    a[1,j] = s;
    
    s++;
    
}

for(int j = 2;j>0;j--)

{

    a[2,j] = s;
    
    s++;
    
}

for (int j=0;j<4;j++)

{

    for (int i =0;i<4;i++)
    
    {
       Console.WriteLine(a[i,j]); 
    }
    
    Console.Write(Environment.NewLine + Environment.NewLine);
    
}

