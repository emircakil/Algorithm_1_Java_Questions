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
### Algorithm that check friendlt number to entered two numbers.
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

