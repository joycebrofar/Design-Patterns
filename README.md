The Strategy pattern allows developers to define a family of algorithms, put each of them into a separate class, and make their objects interchangeable. 
Use NetBeans to create a Java program that implements this design pattern. Name your project TestStrategy.

1. Create an interface named Payment. An interface is a group of related methods with empty bodies. Classes that implement an interface must use the methods of that interface.
2. Create a void method for your interface named pay. It should be public and with a double parameter named amount. Interface methods come with semicolons instead of a pair of curly brackets.
3. Create a class named Online that implements the interface you created earlier. In this class, declare two (2) private String variables named email and password.
4. Add two (2) String parameters to the constructor of this class. Follow the names of your variables earlier.
5. Insert the following statements into your constructor. 

this.email = email;
this.password = password;


6. Use the pay method from the interface. Copy the code below.
public void pay (double amount) {
  System.out.println("Paid using online account: " + amount)

  
7. Add another class named Mobile that also implements the same interface. Declare two private variables named number (String) and pin (int).
8. Add two (2) parameters to the constructor of this class. Follow the names and types of your variables in the previous step.
9. Insert two (2) this statements into your constructor. Refer to the sample in Step 5. 
10. Use the pay method again but edit the display message. Refer to the sample in Step 6. 
11. Add a class named Cart. Declare a private double variable named amount.
12. Add a double parameter to its constructor. Then, write a this statement similar to the sample in Step 6.
13. Add a pay method. Copy the code below for its content.


public void pay(Payment mode) {

  mode.pay(amount);

}

  
14. Use the public class named TestStrategy to execute your Strategy pattern implementation. In its main method, instantiate a Cart object named cart. Copy the code below.
Cart cart = new Cart(1512.75);

cart.pay(new Online("mark.reyes@gmail.com", "Wasd8456!")); 

cart = new Cart(375.25);



15. Add a statement that uses the mobile payment mode. Refer to the second statement in the sample above.


Sample Output:

Paid using online account: 1512.75

Paid using mobile wallet: 375.25 


  
