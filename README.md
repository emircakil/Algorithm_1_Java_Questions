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

### 






