Task 01) Run the following code:

void countDown(int num)

 {

      if (num == 0) // test

                  System.out.println("Blastoff!");

       else {
         if (num % 2 ==0) {
                  System.out.println(num);

                    countDown(num-1); // recursive call

             } 

}

what is the output of this code?    ...
                                    ... 
                                    ...
                                    ...
                                    ...
                                    Blastoff!
- modify it so that it prints only the even numbers. 

- what is the time complexity of this algorithm and why? It is O(n) because the function is called recursively n times.
-------------------------------------------------------------------------

Task 02) Run the following code:

static int gcd(int x, int y) {

      if (x == y) //base case

             return x;

       else if (x > y) {
         return gcd(x - y, y);

     }
        else { 

             return gcd(x, y - x);
     }
}

what is the output of this code? 6

- modify it to find the gcd using subtraction instead of %.
  -------------------------------------------------------------------------

  Task 03) Run the following code:


int fib(int n)

{

       if (n <= 0) // base case

            return 0;

      else if (n == 1) // base case

             return 1;

       else

             return fib(n – 1) + fib(n – 2);

}

what is the time complexity of this algorithm and why? It is O(n^2) because n is the input parameter. Because the function calls itself twice. 
----------------------------------------------------------------------------------

Write a function that prints "Hello World" n times recursively. 

void helloWorld(int n) { 
    if (n > 0) { 
        System.out.println("Hello World"); 
        helloWorld(n - 1);
    }  
} 

Write a function that returns the sum of all numbers between n1 and n2 that are multiples of 7 using recursion.

int sumMultiplesOf7(int n1, int n2){
    if (n1 > n2) {
        return 0; 
    }
    
   else if (n1 % 7 == 0) { 
     return n1 + sumMultiplesOf7(n1 + 7, n2); 
     }
     else {
        return sumMultiplesOf7(n1 + (7 - n1 % 7), n2);
      }
  } 

  Write a function that implements the binary search algorithm recursively.

int binarySearch(int[] arr, int left, int right, int target) { 
    if (left > right) { 
        return -1;
    }
    int mid = left + (right - left) / 2;
    if (arr[mid] == target) {
        return mid;
    } else if (arr[mid] < target) {
        return binarySearch(arr, mid + 1, right, target);
    } 
        else {
          return binarySearch(arr, left, mid - 1, target);
    }
}
