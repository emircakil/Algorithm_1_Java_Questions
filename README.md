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
   public static void main(String[] args) {
   
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
### Strings are entered from keyboard. The method that converts these strings to 10 4-letter words.

```java

    public static void main(String[] args) {

        char c[] = new char[40];

        sideBySide(c);
    }

    public static void sideBySide(char c[]) {

        Scanner s = new Scanner(System.in);

        int charCounter = 0;

        for (;;) {

            String word = s.next();

            for (int i = 0; i < word.length(); i++) {

                if (word.charAt(i) != ' ') {

                    c[charCounter] = word.charAt(i);

                    charCounter++;

                    if (charCounter >= 40) {

                        print(c);
                        System.exit(1);
                    }
                }
            }
        }
    }

    public static void print(char c[]) {

        int counter = 0;

        for (;;) {

            for (int j = 0; j < 4; j++) {

                System.out.print(c[counter]);

                counter++;

                if (counter == 40) {

                    System.out.println(" ");
                    System.exit(0);
                }
            }
            
            System.out.print(" ");
        }
    }
```

### Creating 100 8-letter passaword using English alphabet with lower case and 0-9 numbers.

```java
public static void main(String[] args) {

        String list[] = new String[100];

        elements(list);

        print(list);
    }

    public static String[] elements(String[] x) {

        Random r = new Random();

        int trueOrFalse;
        int keepNum;
        int rndChar;
        char keepChar;

        String keep = "";

        for (int j = 0; j < x.length; j++) {

            for (int i = 0; i < 8; i++) {

                trueOrFalse = r.nextInt(2);
                keepNum = r.nextInt(10);
                rndChar = r.nextInt(123 - 97) + 97;
                keepChar = ((char) rndChar);

                if (trueOrFalse == 0) {

                    keep += keepChar;
                } else {
                    keep += keepNum;
                }
            }

            x[j] = keep;
            keep = "";

        }

        return x;
    }
```
### Algorithm that check symmetrical or not of matrix.

```java

public static void main(String[] args) {

        int list[][] = {{1, 3, 3, 3, 1},
                        {2, 5, 5, 5, 2},
                        {1, 3, 3, 3, 1}};

        boolean c = check(list);

        print(c);
    }

    public static boolean check(int x[][]) {

        boolean condition = true;

        for (int i = 0; i < x.length; i++) {

            for (int f = 0, l = x[0].length - 1; f < x[0].length; f++, l--) {

                if (x[i][f] != x[i][l]) {

                    condition = false;
                }

            }
        }

        for (int s = 0, f = x.length - 1; s < x.length; s++, f--) {

            for (int i = 0; i < x[0].length; i++) {

                if (x[s][i] != x[f][i]) {

                    condition = false;
                }
            }
        }

        return condition;
    }

    public static void print(boolean condition) {

        if (condition == true) {

            System.out.println("Matrix is symmetrical");
        } else {

            System.out.println("Matrinx isn't symmetrical");
        }

    }
```

### Write a method that returns the sum of two integers that comes as a parameter

```java
    
    public static int sum (int x , int y){
    
        return (x+y);
   
    
    }
    
    public static void main(String[] args) {
        
        Scanner s  = new Scanner(System.in);
        
        int number1 = s.nextInt();
        int number2 = s.nextInt();
        
        System.out.println(sum(number1,number2));
        
        
        
    }
    
}
```

### Write method that returns the power of one integer other integer that comes as a parameter

```java
public class question2 {
    
    public static int pwr (int x , int y) {
    
        int c = (int) Math.pow(x,y);
        
    return c;
    
    
    }
    
    
    public static void main(String[] args){
    
        Scanner s = new Scanner(System.in);
        
        System.out.println("Please write one number.");
        int number1 = s.nextInt();
        System.out.println("Please write power of number.");
        int number2 = s.nextInt();
        
        System.out.println("Result = " + pwr(number1,number2));
    }
}
```
### Write method show your name until number n that comes as a parameter

```java
public static void show(int x){
    
    for ( int i = 1 ; i <= x; i++){
    
        System.out.println("Emirhan Aydin Cakil");
    
    }
    
    
    }
    
    public static void main(String[] args){
    
        Scanner s= new Scanner(System.in);
        
        int number = s.nextInt();
        
        show(number);
    
    }
 ```
 ### Write method that return the how much digits of integer that comes as a parameter
```java
 public static int digit ( int x){
    
        int counter =0;
        
        while ( x > 0){
        
            counter++;
            
            x /= 10;
        
        }
    
    return counter;
    
        
    }
    
    public static void main(String[] args) {
        
        Scanner s = new Scanner (System.in);
        
        int number = s.nextInt();
        
        System.out.println(digit(number));
        
    }

```
### Write method that return what equals is nth of fibonacci sequence that comes as a paramter

```java
ublic static int fibonacci ( int x){
    
        int a = 1;
        int b = 1; 
        int c =0;
        
        if ( x == 1 &&  x == 2){
            return 1;
        }
        
        
        for ( int i = 3 ; i <= x ; i++){
        
         c = a + b;
         a = b;
         b = c;
        
        
        }
    
    return c;
    
    
    }
    
    public static void main(String[] args){
    
    Scanner s = new Scanner(System.in);
    
    int n = s.nextInt();
    
    System.out.println(fibonacci(n));
    
    }
```

### Write a method that return the factorial of integer that comes to it as a paramter

```java
public static int factorial (int x){
    
    int fct =1 ;
    
        for ( int i =1 ; i <= x; i++){
        
        fct *= i;
        
        }
    
    return fct;
    
    
    
    }
    
    
    
    public static void main(String[] args) {
       
        Scanner s = new Scanner(System.in);
        
        int number = s.nextInt();
        
       System.out.println( factorial(number));
        
    }
```

### Write method that return sum of all integer integer entered from keyboard that comes to is as parameter
```java
public static int sumOfAll (int x){
    
    int sum = 0; 
    
        for ( int i = 1; i < x ; i++){
        
        sum += i;
        
        
        
        }
    
        return sum;
    }
    
    public static void main(String[] args) {
        
        Scanner s = new Scanner (System.in);
        
        int number = s.nextInt();
        
       System.out.println( sumOfAll(number) );
    }
```

### Write a method that return finding bigger of two integer that comes to it as parameter
```java
public static int bigger ( int x , int y){
    
        int big =0;
        
    if ( x > y){
        
        big =x;
    
    }
    else{
    
        big = y;
    }
    
    return big;
    
    
    }
    
    public static void main(String[] args) {
        
        System.out.println(bigger (4,5));
        
    }
```

### Write method that return finding lower case in a string that comes to it as parameter
```java
public static int lowerCase ( String x){
    
    int counter = 0;
    
    for ( int i =0 ;  i < x.length(); i++){
    
        if ( x.charAt(i) >= 'a' && x.charAt(i) <= 'z'){
        
        counter++;
        
        }
    
    }
    
    return counter;
    
    }
    
    public static void main(String[] args) {
        
        String word = "Emirhan Aydin Cakil";
        
        System.out.println(lowerCase(word));
    }
```
### Write method that return lower cases converting to upper cases and upper cases converting to lower cases of a string that comes to it as parameter

```java
 public static String convert ( String x){
    
        String nw = "";
        
        for ( int i =0 ; i < x.length(); i++){
     
            if ( x.charAt(i) >= 'a' && x.charAt(i) <= 'z'){
            
                char c = x.charAt(i);
                String word = String.valueOf(c);
                nw += word.toUpperCase();
            }
            else {
                char c = x.charAt(i);
                String word = String.valueOf(c);
                nw += word.toLowerCase();
            }
        
    
        }
    return nw;
    
    }
    
    public static void main(String[] args) {
        
        String sentence = "eMIRHAN aYDIN cAKIL";
        
        System.out.println(convert(sentence));
        
    }
```

### Write method that return finding how much "aa" terms of a string that comes to it as parameter
```java
public static int findAA ( String x ){
    
    int counter =0 ;
    
    for ( int i = 0 ; i < x.length()-1; i++){
    
        if ( x.charAt(i) == 'a' && x.charAt(i+1) == 'a' ){
        
            counter++;
        }
    
    }
    
    return counter;
    
    }
    
    
    public static void main(String[] args) {
        
        
        String word = "aa bb cc aa ee dd aaa";
        
        System.out.println(findAA(word));
    }
    
```

### Write method that return finding bigger of length of two string that comes to it as parameter

```java
public static boolean biggerOfStrings(String x , String y ){
     
    if ( x.length() > y.length()){
    
        return true;
    
    }
    
    return false;
    
    }
    
    public static void main(String[] args) {
        
        String sentence1 = "Emirhan Aydin Cakil";
        String sentence2 = "Emirhan Aydin";
        
        boolean condition = biggerOfStrings(sentence1, sentence2);
        
        if ( condition == true){
        
                System.out.println("String 1 bigger than String 2");
        }
        else {
                System.out.println("String 1 smaller than String 2");
        }
        
    }
```

### Write metod that return how much word of a string that comes to it as parameter
```java
public static int wordCount ( String x ){
    
        int counter = 1 ;
        
        for ( int i =0 ; i < x.length(); i++){
        
            if ( x.charAt(i) == ' ' ){
            
                counter++;
            
            }
        
        
        }
        
    return counter;
    
    }
    
    
    public static void main(String[] args) {
        
        String sentence = "Emirhan Aydin Cakil";
        
       System.out.println( wordCount(sentence) );
        
    }
```

### Write metod that return finding whether 'a' terms in a string that comes to it as parameter
```java
public static boolean findA ( String x ){
    
    
        
        for ( int i = 0; i < x.length(); i++){
        
            if ( x.charAt(i) == 'a'){
            
                return true;
            }
        
        
        }
    return false;
    
    
    }
    
    public static void main(String[] args) {
        
        Scanner s = new Scanner(System.in);
        
        String sentence = s.nextLine();
        
        boolean condition = findA(sentence);
        
        if ( condition == true){
        
            System.out.println("String has character a");
        
        }
        else {
        
            System.out.println("String hasn't character a");
        }
```

### Write method that return whether polindrome or not that comes to it as parameter
```java

public static boolean polindromeCheck ( String x ) {
    
       
        
        for ( int i = 0 , j = x.length()-1 ; i < x.length() ; i++ , j--){
        
          
            
                if ( x.charAt(i) != x.charAt(j)){
                    
                    return false;
                
                }
    
        }
        
        return true;
           
    }
    
    
    public static void main(String[] args) {
        
        Scanner s = new Scanner (System.in);
        
        String word = s.next();
        
        boolean a = polindromeCheck(word);
        
        if ( a == false){
        
                System.out.println("String isn't a polindrome");
        }
        else {
                System.out.println("String is a polindrome");
        }
        
    }
```

### Write metod that return sum of array of integer that comes to it as parameter
```java

public static int sumOfArray(int []x){
    
        int top = 0 ;
        
        for ( int i = 0 ; i < x.length; i++){
        
            top += i;
        
        }
    
        return top;
    
    }
    
    
    public static void main(String[] args) {
        
        int list [] = {1,2,3,4,5,6,7,8,9,10};
        
       System.out.println( sumOfArray(list) );
        
    }
    
```

###  Write method that return indis of lowest integer of the integer array that comes to it as parameter
```java
 public static int findLowest ( int x []){
    
        int smallest = x[0];
        int index = 0;
        
        for ( int i =0 ; i< x.length; i++){
        
            if ( smallest > x[i]){
            
                smallest = x[i];
                index = i+1;
            }
        }
    
        return index;
    
    }
    
    public static void main(String[] args) {
        
        int list [] = { 10 ,1 , 20, -10 , 30};
        
        System.out.println("index of smallest element =" +findLowest(list));
        
    }
```
### Write metod that return checikng whether elements serial of integer array that comes to it as parameter
```java

public static boolean checkSerial ( int [] x){
    
        for ( int i = 0 ; i < x.length-1 ; i++ ){
        
            if ( x[i] > x[i+1]){
        
            return false;
        }
        
        }
    
    return true;
    
    }
    
    public static void main(String[] args) {
        
        Scanner s= new Scanner ( System.in);
        
        int list [] = new int[5];
        
        for ( int i = 0 ; i < list.length; i++){
        
        list[i] = s.nextInt();
        }
        
        boolean condition = checkSerial(list);
        
        if ( condition == true){
        
            System.out.println("Array is an serial array");
        }
        else {
            System.out.println("Array isn't an serial array");
        }
```
### Write metod that return plus one to all elements of integer array that comes to it as paramaeter

```java
public static int[] plusOne(int[] x){
    
        for ( int i =0 ; i < x.length; i++){
        
            x[i]++;
        }
    
        return x;
    }
    
    public static void main(String[] args) {
        
        int [] list = {10, 20, 30, 40, 50, 60 ,70, 80 , 90 ,100};
        
        list = plusOne(list);
        
        for ( int i =0 ; i < list.length; i++){
        
            System.out.println(list[i]);
        }
        
    }
```

### Write method that return index of longest string of string array that comes to it as a parameter
```java
 public static int findLongest(String [] x){
    
        int length = x[0].length();
        int index = 0;
        
        
        for (int i = 0 ; i < x.length; i++){
            
           
             if ( length < x[i].length()){
                 
                 index =i;
             
            }
        
        }
    
        return index;
    }
    
    public static void main(String[] args){
    
    String list[] = {"Emirhan" , "Aydin", "Cakil"};
    
        System.out.println("indis of longest string = " + findLongest(list) );
    
    }
 ```
 ### Write method that return second largest number of integer array that comes to it as a parameter
 ```java
  public static int find ( int[] x){
    
        
        int keep;
        
        for (int i =0 ; i < x.length; i++){
        
            for ( int j = i+1 ; j < x.length; j++){
        if ( x[i] < x[j]){
            
            keep = x[i];
            x[i] = x[j];
            x[j] = keep;
            
        
                    
                    }
            }
            
        }
        
        return x[1];
    
    }
    
    public static void main(String[] args) {
        
        Scanner s= new Scanner (System.in);
        
        int [] list= new int [5];
        
        for ( int i = 0 ; i < list.length; i++){
        
            list[i] = s.nextInt();
        }
        
       System.out.println( "En buyuk 2. eleman =" + find (list) );
        
        
    }
 ```
 
 ### Write method that return finding smallest and biggest elements of integer array that comes to it as a parameter
 ```java
  public static int[] find ( int[] x){
    
        int smallest = x[0], biggest = x[0];
        int [] rtrn = new int[2];
        
        for ( int i =0 ; i < x.length; i++){
        
            if ( biggest < x[i]){
            
                biggest = x[i];
            }
            if ( smallest > x[i]){
            
                smallest = x[i];
                
            }
        }
        
        rtrn[0] = biggest;
        rtrn[1] = smallest;
        
        return rtrn;
    
    }
    
    
    public static void main(String[] args) {
        
        Scanner s = new Scanner(System.in);
        
        int list [] = new int [5];
        
        
        for ( int i = 0 ; i < list.length; i++){
        
            list[i] = s.nextInt();
        
        }
        System.out.println("Biggest element of array = " + find(list)[0]);
        System.out.println("Lowest element of arrat = " + find(list)[1]);
        
        
    }
 ```
 ###  Write method that returns calculate average of midterm and final exams of two arrays that comes to it as a parameter
 
 ```java
   public static int [] calculateAverage ( int []x , int []y){
    
        int [] averages = new int [3];
        
        for ( int i =0; i < averages.length; i++){
        
            averages[i] = ((x[i]*40 )+ (y[i]*60))/100;
        
        }
    
        return averages;
    }
    
    public static void main(String[] args) {
        
        int midterms [] = {15 , 58 , 50};
        int f1nals [] = { 100 , 50, 8};
        
        for ( int i =0 ; i < midterms.length; i++){
        
            System.out.println(calculateAverage ( midterms, f1nals)[i]);
            
        
        }
    }
```
###  write method that returns finding biggest element of double dimensional array that comes to it as a parameter
###                                that returns index of biggest element
###                               that returns sum of each rows                               
```java
 public static int biggest( int x [][]){
    
        int big = x[0][0];
    
        for ( int i =0 ; i < x.length; i++){
            for ( int j = 0 ; j < x[0].length; j++ ){
            
                if ( x[i][j] > big){
                
                    big = x[i][j];
                
                }
            
            
            }
        }
      
        
        return big;
    
    }
    
    public static int[] index ( int x[][]){
        
        int big = x[0][0];
        int index1 =0, index2=0;
        int ind [] = new int [2];
        
        for ( int i =0 ; i < x.length; i++){
            for ( int j = 0 ; j < x[0].length; j++ ){
            
                if ( x[i][j] > big){
                
                    big = x[i][j];
                    index1 = i;
                    index2 = j;
                }
            
            
            }
        }
       ind [0] = index1;
       ind [1] = index2;
        
        return ind;
    
    }
    
    public static int[] sumOfRows (int x[][]){
    
        int sum = 0 ;
        int sumRows [] = new int[2];
        
        for ( int i = 0 ; i < x.length; i++){
            for ( int j = 0; j < x[0].length; j++){
            
                sum += x[i][j];
                sumRows [i] = sum;
            }
            sum =0;
        
        }
        
        return sumRows;
    
    }
    
    
    
    public static void main(String[] args) {
        
        Scanner s = new Scanner ( System.in );
        
        int twoDimensional[][] = new int [2][2];
        
        for ( int  i = 0 ; i < twoDimensional.length; i++ ){
        
            for ( int j = 0 ; j < twoDimensional[0].length; j++){
            
            twoDimensional[i][j] = s.nextInt();
            
            }
        }
        
        System.out.println("Biggest element of double dimensional array =" + biggest(twoDimensional) );
        System.out.println("Index of biggest element of double dimensional array =" + index(twoDimensional)[0] + " " +index(twoDimensional)[1]);
        
        for ( int i = 0 ; i < 2; i++){
            
        System.out.println("Sum of "+ i +". rows of double dimensional array =" + sumOfRows(twoDimensional)[i]);
        
        }
    
    }
 ```
 ### Write method this return longest string of double dimensional array that comes to it as a parameter
 ```java
 public static String longest ( String x [][]){
    
        int lng = x[0][0].length(); 
        String word = "";
        
        for ( int i = 0 ; i < x.length; i++){
        
            for ( int j = 0 ; j < x[0].length; j++){
            
                if ( lng < x[i][j].length()){
                
                    lng = x[i][j].length();
                    word = x[i][j];
                }
            
            
            }
        
        }
    
        return word;
    
    
    }
    
    public static void main(String[] args) {
        
        String str [][] = { {"Emirhan" , "Aydin" , "Cakil"},
                            {"Wesley", "Benjamin", "Sneijder"},
                            {"Sokrates" , "Platon" , "Descardes"}}; 
        
        System.out.println(longest(str));
    }
 ```
 ### Write method that return sum of 3x3 matrix that comes to it as a parameter
 ```java
  public static int sumOfMatrix ( int x [][]){
    
        int sum = 0; 
        
        for ( int i = 0 ; i < x.length; i++){
            
            for ( int j= 0 ; j < x[0].length; j++){
            
                sum += x[i][j];
            
            }
        }
    
        return sum;
    
    }
    
    
    
    public static void main(String[] args) {
        
        Scanner s = new Scanner (System.in);
        
        int matrix[][] = new int [3][3];
        
        for ( int i = 0 ; i < matrix.length; i++){
        
            for ( int j = 0 ; j < matrix[0].length; j++){
            
            matrix [i][j] = s.nextInt();
            }
        }
        System.out.println( sumOfMatrix(matrix));
        
    }
 ```
 ### Write method that return shifting one right of integer array that comes to it as a parameter 
 ```java
  
    public static int[] shifting ( int x[] ){
    
        int keep;
       
        
        keep = x[9];
        
        for ( int i =x.length-1; i > 0; i--){
        
            x[i] = x[i-1];
           
        }
    
        x[0] = keep;
      
        return x;
    
    }
    
    public static void main(String[] args) {
        
        int [] list = {10, 20, 30, 40, 50, 60, 70, 80, 90, 100};
        
        int [] list2 = shifting(list);
        
      for ( int i =0; i < list2.length; i++){
        
            System.out.print( list2[i] + " ");
        }
        
    }
 ```
 ###  Write method that return sum of two arrays with 10 elemenst that comes to it as a parameter
 
 ```java
 public static int sumOfArrays ( int x[], int y[]){
    
        int sum = 0;
        
        for ( int i =0 ; i < x.length; i++){
        
            for ( int j = 0; j < y.length; j++){
            
             sum += x[i] + y[j];
            
            
            }
        
        
        }
    
        return sum;
    
    }
    
    
    public static void main(String[] args) {
        
        int [] list1 = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
        int [] list2 = {10 , 20, 30, 40, 50, 60, 70, 80, 90, 100};
            
            System.out.println( sumOfArrays(list1, list2));
        
    }
 ```
 ### Write method that returns check whether prime number or not that comes to it as a parameter
 ```java
 public static boolean check ( int x){
    
        for ( int i = 2 ; i < x; i++){
        
           if ( x % i == 0){
           
               return false;
           }
        
        }
    return true;
    
    }
    
    public static void main(String[] args) {
        
        Scanner s = new Scanner(System.in);
        
        int number = s.nextInt();
        
        boolean condition = check(number);
        
        if ( condition == true ){
        
                System.out.println("Number is a prime number");
        }
        else {
                System.out.println("Number isn't a prime number");
        }
        
        
    }
```
### Write method that return calculate average of odd numbers of a integer array that comes to it as a parameter 
```java
public static double averageOdd ( int []x) {
    
        double avg , counter = 0 , sum =0;
        
        
        for ( int i =0; i < x.length; i++){
        
            if ( x[i] % 2 != 0){
                
                sum += x[i];
                counter++;
            
            }
        
        }
        
        if ( counter == 0){
            return 0;
        }
        else {
            
          avg = sum/counter;
       
        }
    
        return avg;
    }
    
    public static void main(String[] args) {
        
        int list[] = { 1,2,3,4,5,6,7,8,9,10};
        
        System.out.println( averageOdd(list));
        
    }
```

### Write method that returns finding longest word and indexs this of a double dimension array that comes to it as a parameter
```java
public static String[] find ( String[][] x){
    
        String lngst = x[0][0];
        int longest  = x[0][0].length(), indexA = 0, indexB = 0 ;
        
        for ( int i =0; i < x.length; i++){
            
            for ( int j =0; j< x[0].length; j++){
            
            if ( longest < x[i][j].length() ){
            
                longest = x[i][j].length();
                lngst = x[i][j];
                indexA = i;
                indexB = j;
                
            }
      
            }
        
        }
        String i = String.valueOf(indexA);  
        String j = String.valueOf(indexB);
        
        String finded [] = {lngst, i, j};
    
        return finded;
    }
    
    public static void main(String[] args) {
        
        
        
        Scanner s = new Scanner(System.in);
        
        String list [][] = new String[2][2];
        
        for ( int i = 0; i < list.length; i++){
        
            for ( int j = 0 ; j < list[0].length; j++){
            
            list[i][j] = s.next();
            
            }
        }
        
        System.out.println("Longest String = " + find(list)[0] + " Indis =" + find(list)[1] + ", " + find(list)[2]);
    }
 ```
 
 ###   Recursive method that prints your name on your screen 5 times.

```java


    public static void main(String[] args) {
        
        String name = "Emirhan Aydin Cakil";
                
        print (name , 5 );        
    }
    
    public static int print ( String name, int x){
    
        if ( x == 0){
            
            return 0;
        }
        
        System.out.println(name);
        
        return print (name , --x);
    
    }

```

###  Recursive method that sum of between integers of 1 - 5.

```java

  public static void main(String[] args) {
        
        System.out.println(sum(5));
        
    }
    
    public static int sum ( int x ){
    
        if ( x == 1){
            
            return 1;
        }
        
        return x + sum( --x);
    }
```

###  Recursive method that sum of integers divisible of 7 between of 1 to 100.

```java
 public static void main(String[] args) {
        
        System.out.println( sum (100) );
    }
    
    public static int sum ( int x ){
    
        if ( x == 0){
        
            return 0;
        }
        
        if ( x % 7 == 0){
            
            return x + sum (--x);
        }
        
        return sum (--x);
    }

```

### Same index and same value of two integer arrays.
    
   ##### a) Recursive method that prints this values on your screen.

   ##### b) Recursive method that sum of this values.

   ##### c) Recursive method that finding how much this values.

```java

public static void main(String[] args) {
        
        int arrayA []= {10, 20, 30, 40, 50, 60, 70, 80, 90, 100};
        
        int arrayB []= {10, 23, 9 , 40, 32, 90, 70, 1, 20, 100};
        
       print ( arrayA, arrayB , 0);
       
     
    }
    
    public static int print ( int x [], int y[], int i ){
    
        if ( i == x.length){
            
              System.out.println("Sum of sames = " + calculate ( x, y , 0));
              System.out.println("Number of sames = " + counter ( x, y , 0 , 0));
            
            System.exit(0);
    }
    
        if ( x[i] == y[i]){
        
            System.out.println(x[i]);
        }
        
        return print ( x, y, ++i);
    }
    
    public static int calculate (int x[], int y [], int i){
    
        if ( i == x.length){
   
            return 0;        
        }
        
        if ( x[i] == y[i]){
        
           return  x[i] + calculate (x , y , ++i);
            
        }
        return calculate (x, y , ++i);
    }
    
    public static int counter (int x[], int y[], int i , int counter){
    
        if ( i == x.length){
        
            return counter;
        }
        
        if ( x[i] == y[i]){
            
            return counter ( x, y, ++i, ++counter);
            
        }
        
        return counter ( x, y, ++i, counter);
    
    }
```


### Recursive method that calculate factorial that comes to as parameter.

```java
 public static void main(String[] args) {
        
        Scanner s = new Scanner ( System.in );
        
        int number = s.nextInt();
        
        System.out.println( factorial(number) );
        
    }
    
    public static int factorial ( int x){
    
        if ( x == 1){
        
            return 1;
        }
    
        return x * factorial ( --x );
    }


```

### Recursive method that finding how many digits of number.

```java

public static void main(String[] args) {
        
        Scanner s = new Scanner ( System.in );
        
        int number = s.nextInt();
        
        System.out.println( digit ( number , 0) );
        
    }
    
    public static int digit ( int x, int counter ){
    
        if ( x== 0 ){
        
            return counter;
        }
        x /= 10;
        return digit (x , ++counter);
    }
```    

### Recursive mathod that calculate power of coming two number from keyboard.

```java

 public static void main(String[] args) {
        
        Scanner s = new Scanner (System.in);
        
        int base = s.nextInt();
        
        int pwr = s.nextInt();
        
        System.out.println(calculate ( base, pwr));
    }
    
    public static int calculate ( int x , int y ){
    
        if ( y == 1){
        
            return x;
        }
        
        return x * calculate ( x, --y);
    }
```
### Recursive method that finding value of fibonacci elements.

```java
public static void main(String[] args) {
        
        Scanner s = new Scanner (System.in);
        
        int number = s.nextInt();
        
        System.out.println(fibonacci (number));
    }
    
    public static int fibonacci ( int x ){
    
    if ( x == 1 || x == 2){
    
        return 1;
    }
    
    return fibonacci (x-2) + fibonacci (x-1);
    }


```

### Recursive method that finding biggest element of integer array.

```java

public static void main(String[] args) {
        
        int [] list = { 9, 101, 10, 23, 24, 1, 11, 3, 4};
        
        System.out.println("index of biggest element = " + find(list , 0 , list[0] , 0) );
        
    }
    
    public static int find ( int x[] , int i , int biggest , int index){
    
        if ( i == x.length){
        
            return index+1;
        }
        
        if ( biggest < x[i]){
            
            biggest = x[i];
            index = i;
        }
        
        return find ( x , ++i, biggest, index);
    }
```

### Recursive method that checking series or not of integer array.

```java

  public static void main(String[] args) {
        
        
        int list[] = new int [5];
        
        elements ( list);
        
        if ( check(list , 0) == 1 ){ 
        
            System.out.println("Array isn't a series");
        }
        
        else {
        
            System.out.println("Array is a series");
        }
    }
    
    public static int [] elements (int []x){
    
        Scanner s = new Scanner (System.in);
        
        for ( int i =0 ; i < x.length; i++){
        
            x[i] = s.nextInt();
        }
        
        return x;
    
    }
    
    public static int check ( int x[], int i ){
    
        if ( i == x.length-1){
        
            return 0;
        }
        
        if ( x[i+1] > x[i]){
        
            return check (x, ++i);
        }
        
        return 1;
    }
```

### Recursive method that check symmetrical or not of a array.

```java

public static void main(String[] args) {
        
        int list[] = new int [5];
        
        elements ( list);
        
       if ( check (list , 0, list.length-1) == 0 ){
       
           System.out.println("List is symmetrical");
       }
       else {
           
           System.out.println("List isn't symmetrical");
        }
    }
    
    public static int[] elements( int x[]){
           
        Scanner s = new Scanner (System.in);
        
        for (int i = 0 ; i < x.length; i++){
        
            x[i] = s.nextInt();
        }
        
        return x;
    }
    
    
    public static int check ( int x[] , int i , int j){
    
        if ( i == x.length-1){
        
            return 0;
        }
        
        if ( x[i] != x[j] ){
        
            return 1;
        }
        
        return check ( x, ++i, --j);
    }

```

###  Recursive method that finding how many positive integer of integer array has.

```java

 public static void main(String[] args) {
        
        int list []= {1, -1, 2, -2, 3, -3, 4, -4, 5, -5};
        
        System.out.println("Number of positives = " + find (list , 0 , 0));
        
    }
    
    public static int find ( int x[], int i, int counter){
    
        if ( i == x.length){
        
            return counter;
        }
        
        if ( x[i] > 0) {
        
            return find (x, ++i , ++counter);
        }
        
        return find ( x, ++i , counter);
    }
```

### Recursive method that finding how many lower case of string array has.

```java

public static void main(String[] args) {
        
        String [] sentence =  {"Emirhan", "Aydin", "Cakil"};
        
        System.out.println("Number of lower cases = " + find (sentence , 0 , 0 , 0));
        
    }
    
    public static int find ( String x [], int i, int j, int counter ){
    
        if ( i == x.length){
        
            return counter;
        }
        
        if ( j == x[i].length()){
            
            return find (x, ++i, 0, counter);
        }
        
        
        if ( x[i].charAt(j) >= 'a' && x[i].charAt(j) <= 'z'){
        
            return find (x, i, ++j, ++counter);
        }
        else {
            return find (x, i, ++j, counter);
        }
    }
```

### Recursive method that reverses elements of an array.

```java
public static void main(String[] args) {
        
        String list []= {"Emirhan", "Aydin" , "Cakil"};
        
        String keep = "";
        
        reverse ( list , keep , 0 , list.length-1);
    }
    
    public static int reverse (String [] x , String keep,  int i , int j){
    
        if ( i == x.length/2 ){
        
            print (x);
            return 0;
        }
        
        keep = x[j];
        x[j] = x[i];
        x[i] = keep;
        
        return reverse ( x, keep , ++i, --j);
    }
    
    public static void print ( String []x){
    
        for ( int i = 0 ; i < x.length; i++){
        
            System.out.println(x[i]);
        }
    }
```

### Recursive method that reverses string.

```java
public static void main(String[] args) {
        
        Scanner s = new Scanner (System.in);
        
        String rev = "";
        
        String sentence = s.nextLine();
        
        System.out.println(reverse (sentence , rev ,sentence.length()-1 ) );
    }
    
    public static String reverse (String x ,String y, int i ){
    
        if ( i == -1){
            
            return y;
        }
        
        y += x.charAt(i);
      
        return reverse ( x, y , --i);
    }
```

### Strings are entered from keyboard. The method that converts these strings to 10 sentences with 4 words.

```java

 public static void main(String[] args) {

        String list[] = new String[40];

        elements(list);

    }

    public static void elements(String x[]) {

        Scanner s = new Scanner(System.in);

        int i = 0;

        for (;;) {

            x[i] = s.next();
            i++;

            if (i == x.length) {

                print(x);
                System.exit(1);

            }

        }

    }

    public static void print(String x[]) {

        Random r = new Random();

        int rnd;
        int names;

        int counter = 0;
        int finishCounter = 0;

        while (finishCounter < 10) {

            rnd = r.nextInt(4) + 1;
            

            for (int i = 0; i < rnd; i++) {

                names = r.nextInt (40)+1;
                System.out.print(x[names] + " ");
                
            }
            finishCounter++;
            System.out.println(" ");

        }

        System.exit(0);
    }
```

### Creating with using recursive method 100 8-letter passaword using English alphabet with lower case and 0-9 numbers.

```java
public static void main(String[] args) {

        String list[] = new String[100];
        String none = "";
        Random r = new Random();

        create(list, 0, 0, none, r);

        print(list, 0);
    }

    public static String[] create(String x[], int i, int j, String keep, Random r) {

        if (j == x.length) {

            return x;
        }
        if (i < 8) {

            if (condition(0, r) == 0) {

                keep += rndNum(0, r);
            } else {
                keep += rndChar((char) 0, 0, r);
            }

            return create(x, ++i, j, keep, r);

        } else {
    
            x[j] = keep;
            keep = "";
            return create(x, 0, ++j, keep, r);
        }

    }

    public static char rndChar(char keepC, int rnd, Random r) {

        rnd = r.nextInt(123 - 97) + 97;
        keepC = ((char) rnd);

        return keepC;
    }

    public static int rndNum(int keepNum, Random r) {

        keepNum = r.nextInt(10);

        return keepNum;
    }

    public static int condition(int trueOrFalse, Random r) {

        trueOrFalse = r.nextInt(2);

        return trueOrFalse;
    }

    public static int print(String[] x, int i) {

        if (i == x.length) {

            System.exit(0);
        }

        System.out.println((i + 1) + " " + x[i]);

        return print(x, ++i);
    }


```


### 100 strings are entered from the keyboard and these strings are combined. 20 words with 5 letters are randomly generated from these 100 strings. algorithm that prints the equal of these 20 words to the screen.

```java
public static void main(String[] args) {

        String longString = "";

        longString = elements(longString);

        elementsOfList(longString);
    }

    public static String elements(String x) {

        Scanner s = new Scanner(System.in);

        for (int i = 0; i < 100; i++) {

            x += s.next();
        }

        return x;
    }

    public static void elementsOfList(String x) {

        Random r = new Random();

        String list[] = new String[20];
        String keep = "";

        int rnd;

        for (int i = 0; i < list.length; i++) {

            rnd = r.nextInt(x.length() - 4);

            for (int j = rnd; j < rnd + 5; j++) {

                keep += x.charAt(j);
            }
            list[i] = keep;
            keep = "";
        }
        allPrint(list);
        check(list);
    }

    public static void allPrint(String[] x) {

    // that method generated for checking list.
 
        for (int i = 0; i < x.length; i++) {

            System.out.println(x[i]);
        }
    }

    public static void check(String[] x) {

        for (int i = 0; i < x.length; i++) {

            for (int j = i + 1; j < x.length; j++) {

                if (x[i].equals(x[j])) {

                    System.out.println("same elements of random list =" + x[i]);
                }
            }
        }
    }
```

