# Ex.No:3(D)    INTERFACE 

## QUESTION:

You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.


 Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".


## AIM:

To write a Java program that uses an interface WeatherBot to predict weather conditions using different bot classes SunBot and RainBo

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an interface WeatherBot with a method predict(int temperature).
4. Create a class SunBot that implements WeatherBot and returns "HOT" if temperature > 30, otherwise "MODERATE".
5. Create another class RainBot that implements WeatherBot and returns "COLD" if temperature < 20, otherwise "WARM".
6. In the main method, read the temperature and bot type from the user using Scanner, and create the appropriate bot object.
7. Call the predict() method using the object and display the prediction.





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Venkat Ramana S B
RegisterNumber:  212224060296
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

interface WeatherBot {
    String predict(int temperature);
}

class SunBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature > 30) {
            return "HOT";
        } else {
            return "MODERATE";
        }
    }
}

class RainBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature < 20) {
            return "COLD";
        } else {
            return "WARM";
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int temperature = sc.nextInt();
        int botType = sc.nextInt();

        WeatherBot bot;

        if (botType == 1) {
            bot = new SunBot();
        } else {
            bot = new RainBot();
        }

        System.out.println(bot.predict(temperature));
    }
}
```





## OUTPUT:

<img width="560" height="176" alt="image" src="https://github.com/user-attachments/assets/5cfb5d68-64b4-42a6-8a28-216713210ba3" />

## RESULT:

The Java program was executed successfully.
The appropriate bot (SunBot or RainBot) predicted the weather condition based on the given temperature and displayed the result.
