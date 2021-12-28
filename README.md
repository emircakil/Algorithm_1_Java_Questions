# randomQuestions

### Algorithm that calculate multiplication operation using the addition operation 
```java
  public static void main(String[] args) {
        
        int multiplier = 5;
        int multiplicand = 3;
        int sum = 0;
            
        for ( int i =1; i <= multiplier; i++){
        
            sum += multiplicand;
            
        
        }
     
        System.out.println(sum);
    }
```
### Algorithm that calculate divison operation using extraction operation.

```java
    int dividing = 10;
        int dividing2 = 2;
        int counter = 0; 
        
        while ( dividing > 0){
        
           dividing -= dividing2;
           counter++;
        
        }
        System.out.println(counter);
        
    }
```
### Algorithm that checks whether the sum of the three digits of a 3-digit number is equal to itself 
``` java
 public static void main(String[] args) {
       
        for ( int number = 100; number <1000; number++ ){
        
        int keep = number;
    
            int hundredsDigit = keep/100;
            keep = number - hundredsDigit*100; 
            
            int tensDigit = keep/10;
            keep = keep - tensDigit*10;
            
            int onesDigit = keep/1;
            keep = keep - onesDigit*1 ; 
            
        double hundreds = Math.pow(hundredsDigit,3);
        double tens = Math.pow(tensDigit, 3);
        double ones = Math.pow(onesDigit, 3);
        
        double sum = hundreds + tens + ones;
        
      
        if ( sum == number )
            System.out.println(number);
        
        }
    }
```

### Algorithm that finding perfect square numbers between of 10, 1000
```java
public static void main(String[] args) {
        
        for ( int i = 10 ; i <= 1000; i++){
        
            for ( int j = 4; j < 100; j++){
            
                int sqr = j*j;
                
                if ( sqr == i){
                
                    System.out.println(i);
                    
                }
                
            }
        
        }
     
    }
```
### Algorithm to find whether the entered number is a power of 5

```java
public static void main(String[] args) {
        
        Scanner s = new Scanner (System.in);
        
        int number = s.nextInt();
        
        if ( number % 5 == 0){
        
            System.out.println(number + " is power of 5");
        }
        else {
        
            System.out.println(number + " isn't power of 5");
        }
        
     
    }
```
### Algorithm that check friendly number to entered two numbers.
```java
public static void main(String[] args) {
        
        // friendly number = If two numbers are equal to the sum of their divisors excluding each other, these numbers are called friend numbers.
        
        Scanner s = new Scanner (System.in);
        
        int x = s.nextInt() , y = s.nextInt();
        int sumX =0, sumY =0;
     
        for ( int i = 1; i < x; i++){
        
            if ( x % i == 0){
        
                sumX += i;
         }
   
        }
        
        for ( int i = 1; i < y; i++){
        
            if ( y % i == 0){
            
                sumY += i;
            }
        }
        
        if ( sumX == y && sumY == x){
        
            System.out.println("They're friendly number.");
        }
        else {
        
            System.out.println("They aren't friendly number.");
        }
        
        
        
    }
```
### Algortihm that check abundant number or deficient number entered from keyboard.
```java
public static void main(String[] args) {
        
        // abundant number = the sum of its multipliers is bigger than itself
        // deficient number = the sum of its multipliers is less than itself
        Scanner s = new Scanner (System.in);
        
        int sum =0; 
        int number = s.nextInt();
        
        for ( int i =1 ; i < number; i++){
        
            if( number % i == 0){
                
                sum += i;
     
            } 
        }
     
        if ( sum > number){
        
            System.out.println(number + " is a abundant number.");
        }
        else if ( sum < number){
            
            System.out.println(number + " is a deficient number.");
        }
        else {
            System.out.println(number +"is a normal number.");
        }
        
    }
```
### Algorithm that 6 steps for finding random number of between 1 - 63 integer numbers. 

```java
 public static void main(String[] args) {
        
        Scanner s = new Scanner ( System.in);
        
        int number = s.nextInt();
 
        int floor = 1 , ceiling = 63;
        int keep; 
        
        
         if ( number > 62 || number < 2 ){
        
            System.out.println("Please select number between of 1 and 63");
            System.exit(0);
        }
        
        for ( int i =1; i <= 6; i++){
        
            keep =(ceiling + floor)/2;
            
            System.out.println("keep =" + keep);
           
        
            if ( keep == number ){
            
                System.out.println("I finded number = " + number);
                System.exit(0);
            }
            else if ( number > keep ){
            
                floor = keep;
                System.out.println("Bigger than " + keep);
            }
            else {
            
                ceiling = keep;
                System.out.println("Less than");
            }
            
        }
        
     
    }
```

### Algrotihm that decimal convert to binary number.

```java
 public static void main(String[] args) {
        
        Scanner s = new Scanner(System.in);
        
        int number = s.nextInt();
        int keep = number;
        
        int counter = 0 ;
        
        while ( keep > 0 ){
            keep /= 2;
            counter++;
        }
        
        int binary [] = new int [counter];
        
        
        for ( int i = counter-1; i >= 0; i--){
        
        keep = number % 2;
        number /= 2;
        
        
         if ( keep == 0){
            
            binary[i] = 0;
            
         }
        
         else {
            
            binary[i] = 1;
             
         }
            
        }
    
        for ( int i =0 ; i < binary.length; i++){
        
            System.out.print(binary[i]);
        }
        
    }
```
### Algortihm that binary number convert to decimal number

```java
public static void main(String[] args) {
     
        Scanner s = new Scanner ( System.in);
        
        double counter =0;
        String binary = s.next();
        double pwr;
        int sum =0;
        
        for ( int i = binary.length()-1 ; i >= 0; i--){
        
            char no = binary.charAt(i);
            
            if ( no == '1' ){
            
                pwr = Math.pow(2, counter);
                sum += pwr;
            
            }
            else {
            
            }
            counter++;
        
        }
        System.out.println(sum);
        
    }
```

### Algorithm that finding t time of an airplane accelerates smoothly for 15 minutes and its speed becomes 480 km/h. Then at constant speed for 20 min. It goes and slows down smoothly for 15 minutes, and its speed becomes zero.

```java
public static void main(String[] args) {
     
        Scanner s = new Scanner ( System.in );
        
        int t = s.nextInt();
        int plane = 0;
        int list[] = new int [51];
        list[0] = 0;
                
        for (int i = 1 ; i <= 15; i++){
        
            plane += 32;
            list[i] = plane;
        }
        for ( int i = 16; i <= 35; i++){
            plane += 0;
            list[i] = plane;
        }
        
        for ( int i= 36; i < 50; i++){
        
            plane -= 32;
            list[i] = plane;
        }
        
        
        if ( t < 0 || t > 50){
        
            System.out.println("Plane is standing");
        
        }
        else {
            
            System.out.println("Plane's speed = " + list[t]);
        }
        
    }
```
###  Algorithm that check number original number or not of 4 digit numbers

```java
public static void main(String[] args) {
     
        // original number = square of sum of its digits first two digits and last two digits equals its number
        
       
        int firstDigits , lastDigits, keep , sum;
        double pwr;
       
        
        for ( int i =1000 ; i <10000; i++){
 
        keep = i ;  
        
        firstDigits = i /100;
        
        keep -= (firstDigits*100);
        
        lastDigits = keep;
        
        sum = firstDigits + lastDigits;
        
        pwr = Math.pow(sum , 2);
        
        
            if ( pwr == i){
        
                System.out.println(i);
            }
        
        }

    }
```
### Algrorithm that check smith number or not of 4 digit numbers 

```java
public static void main(String[] args) {
        
        // smith number = If the sum of the digits of a non-prime integer greater than 1 is equal to the sum of the digits of all prime numbers in that spelling when the number is written by factoring the prime.
        
        int thousands , hundreds, tens, ones;
        int keep ;
        int sum = 0 , sum2 = 0;
        
        for ( int i = 1000; i < 10000; i++){
        
            keep = i;
            
            thousands = i / 1000;
            i -= thousands*1000;
            
            hundreds =  i / 100;
            i -= hundreds*100;
            
            tens = i / 10;
            i -= tens*10;
            
            ones = i/1;
            
            sum += (thousands + hundreds + tens + ones);
           
            
            i = keep;
            
         
           for( int j = 2 ; j < i ; ){
            
                if ( keep % j == 0){
                
                sum2 += j;
                keep /= j;
    
                }
                else {
                    
                    j++;
                    
                }
              
            }
            
             if ( sum == sum2){
                System.out.println(i);
        
            }
             sum = 0;
             sum2 = 0;
    
            }
   
        }
```

###  Algorithm that finding biggest of number's digits.

```java
 public static void main(String[] args) {
        
        Scanner s = new Scanner (System.in);
        
        int number = s.nextInt();
        
        System.out.println("Biggest digit of number = " + biggest(number));
    
    }
    
    public static int biggest ( int x){
    
    int digit = 0;
    int sum = 0;
    int keep = x;
    
    
        while ( x > 0){
        
         digit++;
         x /= 10;
    }
    
         x = keep;
    
    int list [] = new int [digit];
    
    int big = list[0];
    
        for ( int i =0 ; i < digit; i++){
    
            list[i] = x % 10;
    
            x /= 10;
            
            if ( big < list[i]){
                
                big = list[i];
                
            }
       
    }
    
    return big;
    
    }
```

### Algorithm that degree convert to radian and grad.
```java
// 180 degree = pi radyan = 200grad
    
    public static void main(String[] args) {
     
        Scanner s = new Scanner (System.in);
        
        double degree = s.nextInt();
        
        System.out.println(degree + " degree = " +convert (degree)[0] + " radian = " + convert(degree)[1] + " grad" );
    }
    
    public static double[] convert (double x){
    
        double radian = x / 180;
        double grad = (10 * x) / 9;
        
        double [] list = {radian, grad};
        
        return list;
        
    }
```
### Algorithm that calculate series of 1+ x / 1! + x^2 / 2! + x^3 / 3! ... n and x entering from keyboard
``` java
public static void main(String[] args) {
        
        Scanner s = new Scanner ( System.in);
        
        System.out.println("Please enter the x value");
        
        double number1 = s.nextInt();
        
        System.out.println("Please enter the n value");
        
        double number2 = s.nextInt();
        
        System.out.println( calculate( number1 , number2 ));
    }
    
    public static double calculate ( double x , double n){
    
    double factorial = 1 ;
    double sum = 1;
    double pwr, keep;
    
    
    for ( int i = 1; i <= n ; i++){
    
        pwr = Math.pow( x , i);
        
        for ( int f = 1; f <= i; f++){
        
        factorial *= f;
        
        }
        
    keep = pwr / factorial;  
    sum += keep;
        
    factorial = 1 ;    
    
    
    }
    
    return sum;
    
    }
```

### Algorithm that calculate series of 1-1 / 3+1 / 5-1 / 7+1 / 9-1 / .... / n +- 1  n enter from keyboard
``` java
public static void main(String[] args) {
        
        Scanner s = new Scanner (System.in);
        
        System.out.println("Please enter the n value");
        
        int number = s.nextInt();
        
        if ( number % 2 == 0){
        
            System.out.println("Please enter the odd number. ");
            System.exit(1);
        }
        
        System.out.println( calculate (number));
     
    }
    
    public static double calculate ( int x){
    
    double sum =0 ;
    
    for ( int i = 1; i <= x; i += 4){
    
        sum += (i -1);
    
    }
    for ( int i = 3; i <= x; i += 4){
    
        sum += (i+1);
    } 
    
    
    return sum;
    } 
```

### Algorithm that calculate series of 1 - x^2  / 2! + x^4 / 4! - x^6 / 6! + x^8 / 8! / ...  +- x^n / n!  n enter form keyboard

```java

   //              this series calcutaing of cos(x)

 public static void main(String[] args) {
        
        Scanner s = new Scanner (System.in);
        
        System.out.println("Please enter x value");
        double number = s.nextDouble();
        System.out.println("Please enter n value");
        double number2 = s.nextDouble();
        
        System.out.println( calculate (number , number2));
    }
    
    public static double calculate ( double x, double n){
    
    double sum = 1; 
    double factorial = 1;
    double pwr, keep;
    
    for ( int i = 2; i <= n; i += 4 ){
    
        pwr = Math.pow( x , i);
        
        for ( int f = 1; f <= n; f++){
        
            factorial *= f;
        }
        
        keep = pwr/factorial;
        factorial =1;
        
    sum -= keep;
    
    
    }
    
    for ( int i = 4; i <= n; i += 4){
    
        pwr = Math.pow( x, i );
        
        for ( int f= 1; f <= n; f++){
        
            factorial *= f;
        
        }
        
        keep = pwr/factorial;
        factorial =1; 
        
        sum += keep;
    
    }
    
    return sum;
```

### Algorithm that calclate  ∑ (1/i! + i/ (n-i)!. n enter from keyboard.

```java
public static void main(String[] args) {
        
        Scanner s = new Scanner (System.in);
        
        double n = s.nextDouble();
        double sum =0; 
        double keep;
        double factorial =1 ;
        double factorial2 = 1;
        
        for ( int i = 1; i <= n; i++){
        
         for ( int f = 1; f <= i ; f++){
         
             factorial *= f;
         }
         for ( int f = 1; f < (n-i); f++){
         
             factorial2 *= f;
         }
         
         keep = (1/factorial) + ( i / factorial2 );
         sum += keep;
         factorial =1;
         factorial2 = 1;
        
        
        }
        System.out.println(sum);
  
    }
```

### Algorithm that writing backwards of a word.

```java
    public static void main(String[] args) {
        
        Scanner s = new Scanner (System.in);
     
        String word = s.next();
        
        String turn = writeBackwards(word);
        System.out.println( turn);
    }
    
    public static String writeBackwards ( String x){
    
    String y = "" ;

    for ( int i =x.length()-1 ; i >= 0; i--){
    
        y += x.charAt(i);
        
    }
    
    return y;
    
    }
```
### There is an array with N elements. Algorithm that places the numbers entered from the keyboard into the array, one from the beginning and one from the end.

```java
 public static void main(String[] args) {
     
        Scanner s = new Scanner (System.in);
        System.out.println("Please enter the array's length");
        int x = s.nextInt();
        String [] list = new String[x];
        int lng = list.length;
       
    for ( int i = 0 , j = list.length-1; i < lng/2  ; i++, j--){
    
        list[i] = s.next();
        list[j] = s.next();
     
    }
    
    if ( lng % 2 == 1){
    
        System.out.println("Please enter middle and last value");
        list[lng/2] = s.next();
    
    }
    
    for ( int i =0; i < list.length; i++){
    
        System.out.print(list[i] + " ");
    }
        
    }
```
### Algorithm that gives the following output
```java

/*
    computer
    omputerc
    mputerco
    .
    .
    .
    computer
*/

    public static void main(String[] args) {
        
        String word = "computer";
        
        char c [] = convert(word);
        
        swiftAndWrite(c);
        
    }
        
        public static void swiftAndWrite(char c[]){
            
        for ( int i =0 ; i < c.length;i++){
    
              System.out.print(c[i] + " ");
        
        }
        System.out.println(" ");
            
            char keep = c[0];
        
        for ( int j =0 ; j < c.length; j++){ 
           
           keep = c[0];
           
        for ( int i = 0; i < c.length-1; i++){
            
           c[i] = c[i+1];
           
       }
        
       c[c.length-1] = keep;
       
        for ( int i =0 ; i < c.length; i++){
            
            System.out.print(c[i] + " ");
        }
        
       System.out.println("");
     
       }

    }
            

    public static char[] convert (String x){
    
    char c [] = new char [x.length()];
    
    for ( int i =0 ; i < x.length(); i++){
    
    c[i] = x.charAt(i);
    
    }
    return c;

    }

```

###  Algotihm that sorts an int array from largest to smallest.
```java
public static int[] input(int x[]){
    
        Scanner s = new Scanner (System.in);
        
        for ( int i = 0; i < x.length; i++){
        
        x[i] = s.nextInt();
        
        }
        toSort(x);
        return x;
        
    }
    
    
    public static void toSort(int x[]){
        
        int keep; 
        
        for ( int i =0 ; i < x.length;i++){
        
            for ( int j = i+1; j < x.length; j++){
                
                if ( x[j] > x[i]){
                
                keep = x[i];
                x[i] = x[j];
                x[j] = keep;
                
                }
                
            }
        
        }
        output(x);
        
    } 
    
    
    public static void output (int x[]){
    
        for ( int i = 0; i < x.length; i++){
        
            System.out.print(x[i] + " ");
        }
    }
    
    
    public static void main(String[] args) {
        
        int [] list = new int[10];
        list = input(list);
    
    }

```

###  Algortihm that sum of two binary number
```java
public static double[] convertDecimal ( String x, String y){
   
   int sumX = 0, sumY = 0;
   double decimal[] = new double[2]; 
    
    for ( int i =0, j = x.length()-1; i < x.length(); i++, j--){
    
        if ( x.charAt(i) == '1' ){
        
            sumX += Math.pow(2 , j);
            
        }
        
    }
    for ( int i =0 , j = y.length()-1; i < y.length(); i++, j--){
    
        if ( y.charAt(i) == '1'){
            
            sumY += Math.pow(2 , j);
        }
    }
    
    decimal[0] = sumX;
    decimal[1] = sumY;
    
    convertBinary(sumX+sumY);
    
    return decimal;
    }
    
    public static void convertBinary(int x){
    
    int counter = 0;
    int keep = x;
        
    while ( keep > 0 ){
    
        keep /= 2;
        counter++;
    }
    
    char bnry [] = new char [counter];
    keep = x;
    
    for ( int i =0; i < bnry.length; i++){
    
        keep = x % 2;
        x /= 2;
        
        if ( keep == 0 ){
        
            bnry[i] = '0';
        }
        else {
            bnry[i] = '1';
        }
    }
    
    output(bnry);
    
    }
    
    public static void output( char x[]){
    
    for ( int i =x.length-1; i >=0; i--){
    
        System.out.print(x[i] + " ");
    
    }
    }

    public static void main(String[] args) {
        
        String twentyThree = "10111";
        String nine = "1001";
        
        convertDecimal(twentyThree , nine);
    }

```

### Algorithm that shifts it back to the beginning by removing the ones other than the first written number of the repeated numbers in a 7-element number array with the element values given.

```java 
public static void main(String[] args) {
        
        int list [] = {10 , 20, 30, 40 , 30 , 20 , 50};
        
        swift(list);
        
    }

    public static int[] swift ( int x[] ){
    
    int keep , counter=0;
        
    for ( int i = 0; i < x.length; i++){
        
        for ( int j = i+1; j < x.length; j++){
      
            
            if ( x[i] == x[j]){
                
                keep = x[j];
                        
                for (int s = j; s >counter; s--){
   
                    x[s] = x[s-1];
                }
                
                x[counter] = keep;
                counter++;
            }
        }
    }
    
    output(x);
    
    return x;
    }
    
    public static void output ( int x[]){
    
        for ( int i =0; i < x.length; i++ ){
        
            System.out.println(x[i]);
        }
    
    }
    
```

### Algorithm that finding how much one digit, how much two digit, how much three digit of number array

```java
public static void main(String[] args) {
        
        int list [] = { 10 , 100, 1, 200, 20};
        
        find(list);
        
    }
    
    public static int [] find ( int x[]){
        
    int counter =0, keep;  
    int digits [] = new int [x.length];
        for ( int i = 0; i < x.length; i++){
            
            keep = x[i];
            
            while ( x[i] > 0){
            
            x[i] /= 10;
            counter++;
            
            }
            
        digits[i] = counter;
        counter = 0;
        x[i] = keep;
        }
        output(digits);
        return digits;
    }
    public static void output (int x[]){
    
        for ( int i =0; i < x.length; i++){
        
            System.out.println(" Digit of element " + (i+1) + " = " + x[i] );
        }
    
    }
```

### Half of the sum of the 1st and 2nd elements of a 10-element array is the first element of another array, and half of the sum of the 3rd and 4th elements is the 2nd element.

```java

public static void main(String[] args) {
        
        int list [] = new int [10];

        elementsOfList(list);
        
    }
    
    public static int[] elementsOfList (int x[]){
    
        Scanner s = new Scanner(System.in);
        
        for ( int i =0; i < x.length; i++ ){
        
            x[i] = s.nextInt();
        }
        
        sumAndAssign(x);
        
        return x;
    }
    
    public static void sumAndAssign ( int x[]){
        
        int sum =0;
        int lastArray [] = new int[x.length/2];
    
    for ( int i =0 , j = 1, c =0;  i < x.length; i += 2, j +=2, c++ ){
        
        sum += (x[i] + x[j])/2;
        
        lastArray[c] = sum;
        
        sum = 0;
    }
        
        output(lastArray);
    }
    
    public static void output ( int x[]){
    
    for ( int i =0; i < x.length; i++){
        
            System.out.println(x[i]);
        }
    
    }

```

###    Algorithm that gives the transpose of a square matrix of type [2x2].

```java
 public static void main(String[] args) {
        
        String list[][] = { {"Emirhan" , "Cakil"}, {"Computer" , "Science"} };
        
        output(list);
        
    }
    
    public static String[][] output (String x[][]){
    
        for ( int i =0; i < x.length; i++){
        
            for ( int j =0; j < x[0].length; j++){
            
                System.out.print(x[j][i] + " ");
            
            }
            System.out.println("");
        }
        
        return x;
    }


```
### Algorithm that sum of two matrix

```java
public static void main(String[] args) {
  
    int matrix1 [][] = {{1,2,3},{4,5,6},{7,8,9}};
    int matrix2 [][] = {{1,2,3},{4,5,6},{7,8,9}};

    sumOfMatrixs(matrix1, matrix2);
    
    }
    
    public static int[][] sumOfMatrixs ( int x[][] , int y[][]){
    
        int sums [][] = new int[3][3];
        
        for ( int i =0; i < x.length; i++){
        
            for (int j =0; j < x[0].length; j++){
            
                sums[i][j] = (x[i][j] + y[i][j]); 
            }
        }
        output(sums);
        
        return sums;
    
    }
    
    public static void output ( int x [][] ){
    
        for (int i =0; i < x.length; i++){
        
            for ( int j =0; j< x[0].length; j++){
                
                System.out.print(x[i][j] + " ");
            
            }
            System.out.println("");
        }
    
    }
```


### Algorithm that convert two dimensional array to one dimensional array

```java
public static void main(String[] args) {
        
        int matrix[][] = {{1,2,3},{4,5,6}};
        
        convert(matrix);
    }
    
    public static int[] convert(int x [][]){
    
        int lng = (x.length * x[0].length);
        
        int counter =0;
        
        int single[] = new int [lng];
    
        for ( int i =0; i < x.length; i++){
        
            for ( int j = 0; j < x[0].length; j++){

                 single[counter] = x[i][j];
                 counter++;
            }
        }
        output(single);
        
        return single;
    }
    
    public static void output( int x[]){
    
        for (int i =0; i < x.length; i++){
        
            System.out.println(x[i]);
        }
    }
```

### Algorihm that finding number index of an integer array with sequantial search.

```java

public static void main(String[] args) {
        
        int list [] = { 10, 20, 30 ,40 , 50 ,60 ,70 , 80 ,90 ,100};
        
        output( find(list) );
    }
    
    public static int find( int x[]){
    
        Scanner s = new Scanner(System.in);
        
        int f = s.nextInt();
        
        for ( int i =0; i < x.length; i++){
        
            if ( f == x[i]){
            
                return (i+1);
            
            }
           
        }
        
        return 0;
    }
    
    public static void output( int x){
    
        if ( x== 0){
            System.out.println("Array doesn't have this element");
        }
        else {
            System.out.println("array has element index of " + x);
        }
    }
```

### Algorithm that find number of an integer array with binary search.  

```java
public static void main(String[] args) {
        
        int list [] = {1 , 10, 5, 8 , 6 , 5, 3, 2, 1, 20};
        
        convertSeries(list);    
        }
    
    public static int[] convertSeries( int x[]){
    
        int keep;
        
        for ( int i =0; i < x.length; i++){
        
            for ( int j = i+1; j < x.length; j++){
            
                if ( x[i] < x[j]){
                
                    keep = x[i];
                    x[i] = x[j];
                    x[j] = keep;
                }
            }
        }
        
        check(x);
        return x;
    }
    
    public static void check (int x [] ){
    
        Scanner s = new Scanner (System.in);
        
        int f = s.nextInt();
        
        boolean condition = true;
        
        for ( int i = 0; i < x.length; i++ ){
   
            if ( f == x[i]){
            
                condition = false;
            }
        }
        
        if ( condition == false){
        
            find(x,f);
        }
        else {
            output(-1);
        }
        }
        
       public static void find (int x[], int f){
  
        boolean condition = false;
                
        int floor = 0, ceiling = x.length, counter =0;
        int keep ;
    
        for ( int i =0 ; i < x.length; i++){
            
            keep = (floor+ceiling)/2;
            
            if ( f < x[keep]){
                
                floor = keep;
                counter++;
            }
            else if ( f > x[keep]){
                
                ceiling = keep;
                counter++;
            }
            else {
                condition = true;
            }
        
        
        }
        
        if ( condition == true){
            
             output(counter);
        }
        
        }  
    
    
    public static void output( int x){
    
        if ( x == -1){
            System.out.println("This number doesn`t have array");
        }
        else {
        System.out.println("Number finding try of " + (x+1));
        }
    }

```

### Write algorithm of selection sort.

```java
public static void main(String[] args) {
        
        int list [] = new int[10];
        
        input(list);
    }
    
    public static int[] input(int x[]){
    
        Scanner s = new Scanner(System.in);
        
        for( int i =0; i < x.length; i++){
        
            x[i] = s.nextInt();
        }
        selectionSort(x);
        
        return x;
    }
    
    public static void selectionSort ( int x[] ){
    
        int keep ;
        
        for ( int i = 0 ; i < x.length; i++){
        
            for ( int j = i+1; j < x.length; j++ ){
            
                if ( x[i] < x[j]){
                    
                    keep = x[i];
                    x[i] = x[j];
                    x[j] = keep;
                
                }
            }
        }
        
        output(x);
    }
    public static void output( int x []){
        
        for ( int i =0 ; i < x.length; i++){
        
            System.out.print(x[i] + " ");
        }
    
    }
```
### Write algorithm of bubble sort.

```java
public static void main(String[] args) {
        
        int x [] = new int [10];
        
        input(x);
    }
    
    public static int[] input( int x[]){
    
        Scanner s = new Scanner(System.in);
        
        for( int i = 0; i< x.length; i++){
        
            x[i] = s.nextInt();
        
        }
        bubble(x);
        
        return x;
    }
    
    public static void bubble(int x[]){
        
        int keep;
    
    for ( int i =0; i < x.length;i++){
    
        for ( int j = 0; j < x.length-1; j++){
        
            if ( x[j] > x[j+1] ){
            
                keep = x[j];
                x[j] = x[j+1];
                x[j+1] = keep;
            }
        }
    }
    
        output(x);
    }
    
    public static void output(int x[]){
    
        for ( int i =0; i< x.length; i++){
        
            System.out.print(x[i] + " ");
        }
    }

```

### Write algorithm of insertion sort.
```java
 public static void main(String[] args) {
        
        int list [] = { 10, 4, 7, 9, 11, 15, 3, 2}; 
        
        insertionSort(list);
    }
    
    public static int[] insertionSort(int x[]){
        
        int keep;
        
        for ( int i = 1; i < x.length; i++ ){
    
            for ( int j = 0; j < i; j++ ){
            
                if ( x[i] < x[j]){
                
                    keep = x[i];
                    x[i] = x[j];
                    x[j] = keep;
                }
            }
    
    }
        output(x);
        return x;
    }
    public static void output(int x[]){
    
        for ( int i =0; i < x.length; i++){
            
            System.out.println(x[i]);
        }
    }
```




