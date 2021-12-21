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
        
        Scanner s = new Scanner(System.in);
       
        for ( int number = 100; number <1000; number++ ){
        
      //  int number = s.nextInt();
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

###

