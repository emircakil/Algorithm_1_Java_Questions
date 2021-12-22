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
### Algorithm 

