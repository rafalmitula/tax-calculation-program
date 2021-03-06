# TaxCalculationProgram 

## Table of contents


* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)
* [Description](#description)
* [Inspiration](#inspiration)


## General info

This is a console application which calculates the amount of 23% tax. User can choose between two options: the gross price and the net price. Moreover this applications shows separently the net amount, the gross amount and the tax amount.

## Technologies 
* Java 13

## Setup 
This is a console apllication, however it should be started on at least JDK 12 after cloning project to IDE.

## Description 
### class Main{}

In the **Main class{}**, above the **main(String[] args)** method are located three project's arguments: the **Scanner scanner**, **boolean shouldContinue** and the **Methods methods**. All mentioned arguments have a private modifier due to the encapsulation. Moreover these arguments have also a static modifier due to possibility of using them in this class. 

At the beginning when the program runs, user receives a welcome message. User is also asked to choose options from 1 to 3. 
**Scanner scanner** reads the input data from the user. Next the variable **int userChoice** retrieves the number. The **switch(userChoice)** depends on the mentioned **int userChoice** number entered by the user. 

In this porgram the person who wants to calculate the tax can choose 3 options using the **switch(userChoice)** function: 
* **case 1->**	Calculate the 23% tax from the net price.
* **case 2->**	Calculate the 23% tax from the gross price.
* **case 3->**	Terminate the program.

The calculations in the **case 1** and in the **case 2** are performed by functions located in the **Methods class**. These operations are possible due to the mentioned encapsulation. The **Methods metody** run methods, which are located in the **Methods{} class**.

The **case 3** is performed by **boolean shouldContinue**. Implicitly this variable is encapsulated and setted for **true**, so changing it to **false**, terminates the program.

The **switch(userChoice)** has a **default** option to protect from the user’s invalid number input. If user inputs the wrong number, he/she will receive a message and he/she will have an opprtunity to do this again by the **scanner.nextInt();**.

The **switch(userChoice)** is also in **try/catch** block to catch the exception if user inputs invalid data (becuase the **default** option protects only from the incorrect number input). If the user inputs the incorrect data he/she will receive a message and he/she will have a chance to do this again by the **scanner.next()**;.

This porgram is also located in the **while(shouldContinue)** loop to provide the constant running.

The **boolean shouldContinue** serves to continuing the **while(shouldContinue)** loop and to terminating the application when user will choose the **case 3** in the **switch(userChoice)**.

Above the loop aside from the mentioned **Scanner scanner** and the  **boolean shouldContinu**e  there is also the **Methods metody** .


### class Methods{}

In  this application in **Methods{} class** there are two methods: **calculateNet()** and **calculateGross()**.

* **calculateNet()**

The **calculateNet()** method runs when user chooses the **case 1** in the **switch(userChoice)** in the **main(String[] args)** method.  


In this method **Scanner scnNet** scans an input data from the user, calculate and display: the net amount – **double amountCn**, the tax amount- **double amountVatCn**, the gross amount - **double amountGrossCn**. What is more, in this method the mentioned doubles (**amountCn**, **amountVatCn**, **amountGrossCn**) are rounded to 2 decimal places.


The whole **calculateNet()** method is in the **try/catch** block to protect from the user’s input mistakes (inputting data or wrong numbers). In the **catch** block there is a message for the user and the **calculateNet()** method, so when he inputs wrong number or data, he/she will have opportunity to enter the amount again.

* **calculateGross()**

The **calculateGross()** method runs when user chooses **case 2** in **switch(userChoice)** in **main(String[] args)** method.  


In this method **Scanner scnBrutto** scans an input data from the user, calculate and display: the net amount – **double amountCg**, the tax amount- **double amountVatCg**, the gross amount - **double amountBruttoCb**. What is more, in this method the mentioned doubles (**amountCg**, **amountVatCg**, **amountGrossCg**) are rounded to 2 decimal places.


The whole **calculateGross()** method is in the **try/catch** block to protect from the user’s input mistakes (inputting data or wrong numbers). In the **catch** block there is a message for the user and the **calculateGross()** method, so when he inputs wrong number or data, he/she will have opportunity to enter the amount again.


## Inspiration

The **while** loop with the **boolean shouldContinue** and the **swithch(userChoice)** is inspired by the YouTube channel „Jak nauczyć się programowania” - video „Java- podstawy w 2h”. (https://www.youtube.com/watch?v=6G19kFcVXTo).


